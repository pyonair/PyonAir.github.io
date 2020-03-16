# GPS Receiver module

This Grove - GPS module uses a SIM28 and serial communication configuration. It features 22 tracking / 66 acquisition channel GPS receiver. The sensitivity of tracking and acquisition both reach up to -160dBm.

[GPS Datasheet (PDF) ](/assets/documents/e-1612-ub_datasheets_sheet-1.pdf)

| Interface | Supply voltage |
| :--- | :--- |
| Digital | 3.3 V |

![](/assets/hardware/gps/grove-gps.jpg)

__This module will need an antenna to be connected before use. \(This should come with the board from most suppliers.\)__

## Current suppliers

| Company | Price |
| :--- | :--- |
| [Seeed Studio](https://www.seeedstudio.com/Grove-GPS-p-959.html) | $23.50 |
| [CPC Farnell](https://cpc.farnell.com/seeed-studio/113020003/grove-sensor-gps-receiver/dp/MK00323?ost=grove+gps&ddkey=https%3Aen-CPC%2FCPC_United_Kingdom%2Fsearch) | £27.59 |

## Example code

1. Download MicropyGPS library: [https://github.com/inmcm/micropyGPS/blob/master/micropyGPS.py](https://github.com/inmcm/micropyGPS/blob/master/micropyGPS.py)
2. Add the file "micropyGPS.py" to the "lib" folder in your current project.
3. Copy the code below into a new "main.py" file in the same project.
4. Connect GPS module to board and check pin assignment matches. \(Line 13\)
5. Upload to board via USB.

_Code to receive & interpret current GPS information_

```text
#GPS reader
import pycom
import time

from machine import Pin
from machine import UART

from micropyGPS import MicropyGPS
my_gps = MicropyGPS()

# Setup the connection to your GPS here
# Baudrate is 9600bps, with the standard 8 bits, 1 stop bit, no parity
uart = UART(1, baudrate=9600, pins=('P10','P11')) #Tx, Rx

# Basic UART --> terminal printer, use to test your GPS module
while True:
    my_sentence = (str(uart.readline()))[1:]
    print(my_sentence)
    print(type(my_sentence))

    for x in my_sentence:
        my_gps.update(x)

    time.sleep(1)
    print("Latitude: ", my_gps.latitude)
    print("Longitude: ", my_gps.longitude)
    print("Course: ", my_gps.course)
    print("Altitude: ", my_gps.altitude)
    print("Geoid height: ", my_gps.geoid_height)
    print("Date: ", my_gps.date)
    print("No. of satellites: ", my_gps.satellites_in_use)

```
