# Škoda Home Assistant Integration

This addon to HomeAssistant packages the `SkodaLnxCmd - Škoda Linux Terminal application`.

The application provide caching and rate limiting in order to keep within the 20 req/hour limitation of the public API.

The Application uses the [MyŠkoda Public API](https://public.api.connect.skoda-auto.cz/docs) (released early fall 2026), in order for this application to work you have to generate an API key via the `MySkoda app`.

![HA app preview](https://github.com/mem76/skodaLnxCmd/blob/master/imgs/Home_Assitant_Skoda_Public_API.png)

# Install

To install this HA app, add this repository to HA: `https://github.com/mem76/skodaLnxCmd-ha-addon`

[![Open your Home Assistant instance and show the add app repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fmem76%2FskodaLnxCmd-ha-addon)

[Documentation: Installing a third-party app repository](https://www.home-assistant.io/common-tasks/os/#installing-a-third-party-app-repository)

To set up you need:
* Your cars VIN
* An API key (from the phone APP)
* Security PIN from the phone APP
