# Sendspin tinkering on the Esparagus Loud and Louder

I've been playing a lot with the Sonocotta [Loud](https://www.tindie.com/products/sonocotta/loud-esparagus-media-center/) and [Louder](https://www.tindie.com/products/sonocotta/louder-esparagus-media-center/).

This repo has some tweaked files for how I've been using them with [sendspin](https://www.sendspin-audio.com/) and [Music Assistant](https://www.music-assistant.io/).
I have set up the displays to show track information, and I use [IR remotes](https://www.aliexpress.com/item/1005006464481647.html) from AliExpress to control them.

This also requires PR 12126 for _disabling_ the display, as there's a bug in how an optional package that extends a YAML node is (not) included.
Or remove the `pkg_display` node if you're not using it.

Tweaks:

- Boosted CPU speed when displays are in operation
- Boosted SPI and I2S bus speeds
- Debug components enabled (if needed)
- Splash screen
- Clock on idle
- Track information when playing
- Keep sendspin sensors hidden from HA to save clutter
- Some new defaults in 2026.1 enabled
- Slight display delay on stream start to prioritise audio
