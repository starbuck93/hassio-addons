# Home Assistant Add-on: Christmas Community

## How to Use

Christmas Community is a web application for managing Christmas wishlists for your family or community.

### Initial Setup

1. **First Visit**: When you first visit Christmas Community, you'll be prompted to create an admin account.
2. **Add Family Members**: Once logged in as admin, you can add other family members to the system.
3. **Create Wishlists**: Each family member can create their own wishlist with items they want for Christmas.

### Managing Wishlists

- **Add Items**: Users can add items to their wishlist by providing a URL from supported websites or by manually entering item details.
- **Product Data**: The application automatically fetches product information including images, descriptions, and prices from supported websites.
- **Privacy**: Each user controls who can see their wishlist items.

### Features

#### Table vs Card View
- **Table View** (default): Items are displayed in a clean, organized table format
- **Card View**: Legacy format showing items as cards (set `table: false` in configuration)

#### Single List Mode
When `single_list` is enabled, only the admin account's wishlist is accessible. This is useful for:
- Wedding registries
- Birthday lists
- Baby showers
- Any situation where you want a single shared list

#### Public Lists
When `lists_public` is enabled, anyone can view wishlists without logging in. This is useful for sharing lists with extended family or friends.

#### Profile Pictures
Users can upload profile pictures to personalize their accounts. The feature can be disabled by setting `pfp: false`.

### Supported Websites

Christmas Community can automatically fetch product data from many popular websites including:
- Amazon
- Walmart
- Target
- Best Buy
- And many more!

For a complete list of supported sites, visit the "Supported Sites" page within the application.

### Languages

Christmas Community supports multiple languages. Available languages include:
- English (US)
- English (UK)
- French
- German
- Spanish
- Dutch
- And more!

### Theming

Choose from various themes using the `bulmaswatch` option. Popular themes include:
- default
- darkly
- flatly
- superhero
- And many more!

Visit https://jenil.github.io/bulmaswatch for a complete list of available themes.

## Configuration Options

### Core Settings

| Option | Description | Default |
|--------|-------------|---------|
| `site_title` | Site name in title and navigation | "Christmas Community" |
| `short_title` | Short name for mobile/home screen | "Christmas" |
| `port` | Web interface port | 80 |
| `root_url` | Root URL path | "/" |

### Database Settings

| Option | Description | Default |
|--------|-------------|---------|
| `db_prefix` | Database directory path | "/data/dbs/" |
| `db_log_file` | Database log file location | "/dev/null" |

### Feature Toggles

| Option | Description | Default |
|--------|-------------|---------|
| `table` | Use table view instead of cards | true |
| `single_list` | Only admin account's list accessible | false |
| `lists_public` | Allow viewing without login | false |
| `markdown` | Allow Markdown in item notes | false |
| `pfp` | Enable profile pictures | true |
| `update_check` | Check for application updates | true |

### Styling & Language

| Option | Description | Default |
|--------|-------------|---------|
| `bulmaswatch` | Theme name | "default" |
| `language` | Interface language | "en-US" |

## Troubleshooting

### Common Issues

**Application won't start**
- Check the logs in Home Assistant (Settings → System → Logs → Christmas Community)
- Ensure all required ports are available
- Verify the database directory has proper permissions

**Can't access the web interface**
- Make sure the port isn't already in use by another addon
- Check your Home Assistant network configuration
- Try accessing with your Home Assistant's IP address instead of hostname

**Database issues**
- The database is stored in `/data/dbs/` within the addon
- If you encounter corruption, you may need to delete the database files and start fresh
- Always backup your data before making changes

**Profile picture uploads not working**
- Ensure `pfp` is set to `true` in configuration
- Check that the upload directory has write permissions
- Verify the `upload_pfp_max_size` limit isn't too small for your images

### Getting Help

1. **Check the logs**: Home Assistant → Settings → System → Logs → Christmas Community
2. **Review configuration**: Ensure all options are set correctly for your use case
3. **Search existing issues**: Check GitHub for similar problems
4. **Create an issue**: If you can't find a solution, create an issue on GitHub

## Advanced Configuration

### Custom CSS

You can add custom CSS by mounting a file to `/usr/src/app/src/static/css/custom.css` within the container. In the addon configuration:

```yaml
# In your addon's config
custom_css: "custom.css"
```

Then mount your CSS file in the addon's configuration.

### Environment Variables

The addon supports additional environment variables that aren't exposed in the UI. These can be set by advanced users who need specific functionality.

### Backup and Restore

The addon's data is stored in the `/data` directory. To backup:
1. Stop the addon
2. Copy the `/addon_configs/christmas-community-addon` directory
3. Restart the addon

To restore:
1. Stop the addon
2. Restore the backup to `/addon_configs/christmas-community-addon`
3. Restart the addon

## Development

This addon is based on the Christmas Community project by Wingysam. For development information, visit:
https://github.com/wingysam/Christmas-Community

For addon-specific development:
https://github.com/starbuck93/hassio-addons
