# Home Assistant Add-on: Christmas Community

_Christmas lists for communities - Web app for your family's Christmas shopping_

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg

## About

Christmas Community is a web application that allows your family to create and share Christmas wishlists. This addon brings the full Christmas Community experience to your Home Assistant instance.

## Features

- **Family Wishlists**: Create and manage Christmas lists for your entire family
- **Product Integration**: Automatic product data fetching from supported websites
- **Profile Pictures**: Upload and manage profile pictures for family members
- **Multiple Languages**: Support for multiple languages
- **Responsive Design**: Works great on desktop and mobile devices
- **Guest Access**: Optional guest mode for viewing lists without accounts

## Installation

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fstarbuck93%2Fhassio-addons)

1. Navigate in your Home Assistant frontend to **Settings** → **Add-ons** → **Add-on Store**
2. Click the **⋮** menu and select **Repositories**
3. Add this repository URL: `https://github.com/starbuck93/hassio-addons`
4. The Christmas Community addon should now appear in the store
5. Click on Christmas Community, then click **Install**
6. Configure the addon options as needed
7. Start the addon

## Configuration

### Option: `site_title`
The name of the site displayed in the title and navigation bar.

### Option: `short_title`
Used when shared to home screen.

### Option: `port`
Port number for the web interface (default: 80).

### Option: `table`
Set to `true` for table view, `false` for legacy card view (default: true).

### Option: `single_list`
Set to `true` to only allow the admin account's list (for weddings, birthdays, etc.).

### Option: `lists_public`
Set to `true` to allow viewing wishlists without logging in.

### Option: `markdown`
Allow Markdown in item notes (default: false).

### Option: `pfp`
Enable profile pictures feature (default: true).

### Option: `bulmaswatch`
Theme from https://jenil.github.io/bulmaswatch (default: "default").

### Option: `language`
Interface language (default: "en-US").

## Accessing Christmas Community

Once the addon is running, you can access Christmas Community at:
`http://homeassistant.local:80` (or your configured port)

If you're accessing from outside your network, use:
`http://YOUR_HA_IP:80` (or your configured port)

## Setup

1. Visit the Christmas Community web interface
2. Create an admin account on first visit
3. Start adding family members and wishlists!

## Data Storage

All data is stored in the `/data` directory within the addon, which is persistent across addon updates and restarts.

## Support

For issues with the Christmas Community application itself, please visit:
https://github.com/wingysam/Christmas-Community

For issues with this Home Assistant addon, please visit:
https://github.com/starbuck93/hassio-addons

## License

This addon is licensed under the AGPL-3.0 license, same as the Christmas Community application.
