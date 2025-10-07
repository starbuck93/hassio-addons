# https://developers.home-assistant.io/docs/add-ons/configuration#add-on-dockerfile
ARG BUILD_FROM
FROM $BUILD_FROM

# Execute during the build of the image
ARG TEMPIO_VERSION BUILD_ARCH
RUN \
    curl -sSLf -o /usr/bin/tempio \
    "https://github.com/home-assistant/tempio/releases/download/${TEMPIO_VERSION}/tempio_${BUILD_ARCH}"

# Install Node.js 20 and required dependencies
RUN \
    apk add --no-cache \
        nodejs \
        npm \
        curl

# Create app user and directories
RUN \
    addgroup -g 1000 app \
    && adduser -D -u 1000 -G app app

# Set work directory
WORKDIR /opt/app

# Copy application source
COPY christmas-community/src/ ./

# Install dependencies and build the application
RUN \
    npm install --silent && \
    npm run build && \
    rm -rf node_modules && \
    npm install --production --silent

# Create data directories
RUN \
    mkdir -p /data/dbs /data/uploads \
    && chown -R app:app /opt/app /data

# Copy runtime scripts
COPY rootfs/ /

# Make scripts executable
RUN \
    chmod +x /etc/services.d/christmas-community/run \
    && chmod +x /etc/services.d/christmas-community/finish

# Health check
HEALTHCHECK --interval=30s --timeout=10s --start-period=5s --retries=3 \
    CMD curl -f http://localhost:80/ || exit 1

# Switch to app user
USER app
