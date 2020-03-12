---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default

---

# PyonAir PCB

Grove connectors are an increasingly popular standard in the hobbyist electronics ecosystem.  The plug-and-play connectors make attaching and swapping a wide range of modules easy and fast, with no need to resolder joints.

Arduino and Raspberry Pi already support Grove connector shields but none have yet been released for the Pycom system. Therefore, we designed our own expansion board PCB, which fits onto the LoPy4 board.

The PCB contains:

* 2 I2C sockets \(Temperature sensor & RTC\)
* 3 UART sockets \(2x PM sensor & GPS\)
* Pins for USB data
* A transistor circuits for controlling power to the PM sensors
* A transistor circuit for controlling power to the GPS receiver
* Micro SD slot
* User button
* Power input connectors \(Barrel, JST or screw terminal\)
* [Voltage regulator](voltage-regulator.md)

You can view the schematic in the [Wiring section](../../../tutorial/wiring/) of our guide and [Eagle files](../../../extra-info/resources/pcb-files.md#eagle-files) are included in the Extra Info section.

![](../../../.gitbook/assets/pcb-top-diagonal.jpg)
