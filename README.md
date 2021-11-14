# T-Beam-Helium
Helium Network mapper using the TTGO T-Beam

This is based on the helium/longfi-arduino repo here https://github.com/helium/longfi-arduino/tree/master/TTGO-TBeam-Tracker. Follow the setup in that readme, then look here for any additional changes/customizations in this version.

This is intended to be used with the V1.1 TTGO T-Beam that comes with meshtastic installed by default (example https://www.aliexpress.com/item/4001178678568.html).

## Changes to Setup
This section will list any changes from the default setup linked above.

- In the decoder, you must use `decoded.accuracy` rather than `decoded.hdop` or it will be denied by the mapper API.
- If using v2 or higher of the ESP boards library then you must add `#define hal_init LMICHAL_init` to your `lmic_project.config.h` or you will get compilation errors. See https://github.com/mcci-catena/arduino-lmic/issues/714.
