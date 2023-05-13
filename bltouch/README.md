# Stock Chiron + bltouch

### Connecting the bltouch
I was originally going to just use the Raspberry pi for the bltouch but that didn't work since software pullups on the rpi can't be done in klipper and I didn't want to create a physical pullup

I decided to use the raspberry pi for the bltouch SIGNAL-IN and use the connection for the stock bed probe to carry the Z-OUT signal

I removed some strand of CAT-5E wire I had laying around, threaded it through the drag-chain and then attached it to the cable outside the drag-chain with some electrical tape. 3 wires are needed (2 can work, it seems to work fine without ground to the RPI but that does not seem like a great idea)

If you plan on using the same pinout you firs need to configure the Raspberry Pi as a secondary MCU [link](https://www.klipper3d.org/RPi_microcontroller.html)

I also snipped the end of the stock Z-probe connector and connected it to the plug on the hotend


Pinout:
| Bltouch color | bltouch function | connects to |
| --------      |    --------      | --------    |
| Brown         |    GND           | RPI-GND     |
| Red           |    VCC           | RPI-3,3V    |
| Yellow        |  SIGNAL-IN       | RPI-GPIO27  |
| White         |  Z-OUT           | Stock probe red wire |
| Black         |  GND             | Stock probe black wire |



# Attaching the BLtouch

To attach the BL-touch to my chiron I used a [mount design from thingiverse](https://thingiverse.com/thing:4677134) by user mabag

### Bonus: raspberry pi mount
I needed a place for the raspberry pi, so I remixed some designs and made a mount for it [thingiverse link](https://www.thingiverse.com/thing:6023394)

