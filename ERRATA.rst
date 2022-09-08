######
Errata
######

These are corrections of errors found in the book `Develop your own Bluetooth Low Energy Applications for Raspberry Pi, ESP32 and nRF52 with Python, Arduino and Zephyr <https://koen.vervloesem.eu/books/develop-your-own-bluetooth-low-energy-applications/>`_ only after its publication:

**********
Everywhere
**********

* In Zephyr 3.1.0 all includes have been moved to the new prefix ``<zephyr/...>``. For instance, a line ``#include <bluetooth/bluetooth.h>`` in the book's Zephyr code should now be ``#include <zephyr/bluetooth/bluetooth.h>``. This is fixed in the code in this repository.

************************************************
Chapter 3: Broadcasting data with advertisements
************************************************

* page 53: Bleak 0.15.0 has added support for passive scanning in the BlueZ backend. So now you can also use the ``scanner = BleakScanner(scanning_mode="passive")`` example in your Python code on Linux if you want your scanner to just listen to advertising packets without sending a ``SCAN_REQ`` packet. This requires BlueZ >= 5.56 and Linux kernel >= 5.10. Note that Bleak still doesn't support passive scanning on macOS.
* page 74: The calculation "200 256 = 56 dBm" should be "200 - 256 = -56 dBm".
* page 77: The sentence beginning with "if you look up its definition" should start with a capital letter: "If you look up its definition".
* page 78: The sentence "The ``BT_LE_ADV_PARAM`` macro is another helper macro:" shouldn't be in the code block, but on a normal line, referring to the rest of the code block.

******************************************
Chapter 7: Reverse engineering BLE devices
******************************************

* page 229: The sentence "Fill a pixel for each LED o that you want to light up on the display." should be "Fill a pixel for each LED that you want to light up on the display."
