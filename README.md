# Škoda Home Assistant Integration

This addon to HomeAssistant packages the `SkodaLnxCmd - Škoda Linux Terminal application`.

The application provide caching and rate limiting in order to keep within the 20 req/hour limitation of the public API.

The Application uses the [MyŠkoda Public API](https://public.api.connect.skoda-auto.cz/docs) (released early fall 2026), in order for this application to work you have to generate an API key via the `MySkoda app`.


# Beta version

While the application works, this "Home Assistant install repository" is under development.

* [x] Charging on/off `v0.1`
* [x] Implement a HomeAssistant repo (for GUI install in HA) `v0.1.x`
* [ ] Stabilize REST API towards HA `v0.2` (MVP production)

Until the API is stabilized some names may change.

![HA app preview](https://github.com/mem76/skodaLnxCmd/blob/master/imgs/Home_Assitant_Skoda_Public_API.png)

