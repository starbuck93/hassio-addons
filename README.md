# Home Assistant Add-ons Repository

This repository contains Home Assistant add-ons that I've built for applications I wanted to run on my Home Assistant OS instance. Currently featuring the Christmas Community addon for managing family wishlists.

Add-on documentation: <https://developers.home-assistant.io/docs/add-ons>

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fstarbuck93%2Fhassio-addons)

## Add-ons

This repository contains the following add-ons

### [Christmas Community](./christmas-community-addon/)

![Supports aarch64 Architecture][aarch64-shield]
![Supports amd64 Architecture][amd64-shield]
![Supports armhf Architecture][armhf-shield]
![Supports armv7 Architecture][armv7-shield]
![Supports i386 Architecture][i386-shield]

_Christmas lists for communities - Web app for your family's Christmas shopping. Full-featured wishlist management with automatic product data fetching from supported websites._

<!--

Notes for developing addons in this repository:
- While developing, comment out the 'image' key from 'christmas-community-addon/config.yaml' to make the supervisor build the addon locally
  - Remember to uncomment this when you're ready to publish builds.
- When you merge to the 'main' branch of your repository a new build will be triggered.
  - Make sure you adjust the 'version' key in 'christmas-community-addon/config.yaml' when you do that.
  - Make sure you update 'christmas-community-addon/CHANGELOG.md' when you do that.
  - The first time this runs you might need to adjust the image configuration on github container registry to make it public
  - You may also need to adjust the github Actions configuration (Settings > Actions > General > Workflow > Read & Write)
- The 'image' key in 'christmas-community-addon/config.yaml' should point to your username: ghcr.io/starbuck93/{arch}-addon-christmas-community
- All URLs and references should point to your repository: https://github.com/starbuck93/hassio-addons
- Share your repository on the forums https://community.home-assistant.io/c/projects/9
- Add more awesome addons for applications you want to run on Home Assistant OS!
-->

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
