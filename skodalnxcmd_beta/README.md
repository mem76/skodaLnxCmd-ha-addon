# Home Assistant MyŠkoda Integration (2026 version)

In September 2026 the new Škoda API was released to the public.

This Home Assistant app uses a middleware application that handles 
the communications to Škoda's API and implements caching with due to the low rate limit (20 req/hour).

You need the MyŠkoda app in order to generate keys.

![](https://github.com/mem76/skodaLnxCmd/raw/master/imgs/Home_Assitant_Skoda_Public_API.png)

## Support

### Upcoming support:

* [x] Charging on/off `v0.1`
* [x] Implement a HomeAssistant repo (for GUI install in HA) `v0.1.x`
* [x] Stabilize REST api towards HA `v0.2`
* [x] Update MyŠkoda API version from 1.0 to 1.1 `v0.2.x`
* [x] AC on/off (EVs) `v0.3`
* [ ] Heater on/off (ICE cars) `v0.4`
* [ ] Fan on/off (ICE cars) `v0.5`
* [ ] Add "slow charge toggle" (limit to 8A)". `v0.6`
* [ ] Enable using "current temp" for AC/heat `v0.7`
* [ ] Reduce log noise during API outages `v0.8`
* [ ] Implement data from ICE and hybrid cars.
* [ ] Better fallback if 12V battery is low.
* [ ] Enable auto population (no need for editing config file) `v1.0`
* [ ] Create documentation for people with multiple cars.

### What is not supported.

#### Editing charge modes

While Škoda's API supports changing the charging profile, this will not be implemented in this integration. The reason
is that charging profile intended use is for situation when the car does not have a "smart home" connection. A user of
Home Assignment will set up HA to start/stop charging according to power usage and energy prices making this function
redundant.

This API exposes the current charging profile in order enable HA to test "is car at home" in order to prevent HA to stop
charging while charging on a public charger.

#### Camp mode

Škoda vehicles has **no support** for camp mode. There is a "hack" in the MyŠkoda app that starts the AC multiple times.
You can set up camp the same hack an automation that checks a timer counting down.
```
if {timer is running} && {Skoda AC is off}; then
  turn on AC
fi
```

## Help needed

I only have access to an EV, and can therefor not test the code on ICEV, PHEV and HEV. Please test
and [report issues](https://github.com/mem76/skodaLnxCmd-ha-addon).
