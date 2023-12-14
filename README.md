# Sound-Reactive-Infinity-Mirror
**Sound reactive Infinity Mirror and VU meter**

For both displays, I used WS2815 adressable leds.
This type of LED, needs 12VDC power supply. The Data pin can be connected directly (or thru a 220ohm resistor to protect the data pin) to an Arduino board or ESP WiFi module, using a GPIO (3V to 5V) pin.

Using “auto-reshaping tech.” the data signal is regenerated on each led, so you just need to be sure that you have a “clean” signal, connected to the first led only.
You can connect max 1024 leds in a row in order to obtain 30fps refresh rate.
Power consumption of each led is 0.3W (when the color is White = RGB > fully ON), so keep an eye on the led strip length and inject power at every 5-10m (GND must be common).

The Android app and Arduino source code which is open source, was written/adapted by [“Cine-Lights”](https://www.youtube.com/channel/UCOG6Bi2kvpDa1c8gHWZI5CQ/videos) – Thanks!!!
Check his youtube page for more interesting displays, Arduino sketch and HowTo’s.

- This is my first project with adressable leds: https://youtu.be/yMKHycFAHX4
- and here is the second one with BT HC-06 module and a button: https://youtu.be/949kpGuPM74

For the infinity mirror project I used a picture/photo frame from IKEA, model RIBBA 50x50cm and 116pcs – WS2815 leds.
Here is a picture about [infinity mirror components](https://i1.wp.com/makezine.com/wp-content/uploads/2015/03/infinitymirror_v2.jpg). (Makezine project [link](https://makezine.com/projects/easy-mega-infinity-mirror/))
Start attaching the leds exactly in the middle of the inner wooden frame, starting from a corner.

For the LED strips (I used 1m aluminum bar + 58 leds connected to an XLR male connector) you can use any rigid aluminum bars, which can be found usually in any bigger stores. Use additional thin, transparent double adhesive tape for attaching the leds to the wood frame / aluminum bars. The adhesive layer from the led strips are very poor quality.
Both projects are equipped with sensitive ADMP401 – MEMS microphones, connected directly to an analog input.
Only Arduino Nano boards was used here. Both have the AREF pin connected to 3.3V.
You can download the slightly modified Arduino sketches from here:
1) Infinity Mirror – [Vu_infinity_mirror.zip](https://github.com/cyberelectronics/Sound-Reactive-Infinity-Mirror/blob/main/Docu/Vu_infinity_mirror.zip)
2) VU meter – [Bluetooth_VUmeter.zip](https://github.com/cyberelectronics/Sound-Reactive-Infinity-Mirror/blob/main/Docu/Bluetooth_VUmeter.zip)

Connections:
LED Data pin > D6
Microphone > A5
Button > D4
BT HC06 = BTRX > D11 (thru level shifter or voltage divider) and BTTX > D10
