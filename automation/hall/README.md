# Automations, automations everywhere, and all the brains did hurt

Documentation: [automation](https://home-assistant.io/docs/automation/)

## The hall

The hall is entirely internal, there's no windows to the outside, and all the doors are solid (no glazing). Upstairs that's not normally a big deal, because the doors tend to be open during the day. Downstairs there's a whole three doors, and no direct path for light other than through the vestibule door. Because of this, there's a [Hue compatible RGB+CCT strip](https://www.howtogeek.com/361560/how-to-make-your-own-philips-hue-lightstrips-for-cheap/) at the front of the hall, along the width of the vestibule wall at the ceiling.

Oh, except at Christmas, when we'll want the Christmas light string controlled by the Z-Wave socket to come on instead.

The decision is controlled by an input select for the season/holiday, and a couple of scripts.

### hall-lights-off-departure.yaml

We leave, turn the light off.

### hall-lights-off.yaml

Triggered by:

* Bedtime
* The sun rising enough
* Enough sunlight (in the living room, waiting for the latest Hank multi-sensor to be released to market)

### hall-lights-on.yaml

This one is more complicated, it triggers when:

* Anybody comes home
* The sun sets below 5 degrees
* It gets dark (in the living room)
* We wake up

As long as the following conditions are met, the light will turn on:

* Dark or the sun is below 5 degrees
* We're not all asleep or somebody just came home
* Somebody is home
