HackRF Library for Android
==========================

This repository is a ported version of Michael Ossmann's libhackrf
([https://github.com/mossmann/hackrf/tree/master/host/libhackrf]
(https://github.com/mossmann/hackrf/tree/master/host/libhackrf))
library to work with Android 3.1+.



![hackrf_android](https://pbs.twimg.com/media/BzHt03EIIAEXTvN.jpg:large)

(photo by Dennis Mantz)

See [http://tech.mantz-it.com](http://tech.mantz-it.com) and @dennismantz for updates.


Implemented Features
--------------------
* Open HackRF (including the USB permission request)
* Reading Board ID from HackRF
* Reading Version from HackRF
* Reading Part ID and Serial Number from HackRF
* Setting Sample Rate of HackRF
* Setting Frequency of HackRF
* Setting Baseband Filter Width of HackRF
* Compute Baseband Filter Width for given Sample Rate
* Setting VGA Gain (Rx/Tx) of HackRF
* Setting LNA Gain of HackRF
* Setting Amplifier of HackRF
* Setting Antenna Port Power of HackRF
* Setting Transceiver Mode of HackRF
* Receiving from the HackRF using a BlockingQueue
* Transmitting to the HackRF using a BlockingQueue
* Get Transmission statistics
* Example App that shows how to use the library


Testet Devices
--------------

|    Device    | Does it work? | Tested sample rate with example app |     Tester    |
|:------------:|:-------------:|:-----------------------------------:|:-------------:|
| Nexus 7 2012 |      yes      | ~ 2 Msps, Filewriter is too slow.   | Dennis Mantz  |
| Nexus 7 2013 |      yes      | 15 Msps                             | @kx3companion |
| Nexus 5      |      yes      | 15 Msps                             | Dennis Mantz  |
| Moto G       |      yes      | ~ 2 Msps                            | @kx3companion |

Known Issues
------------
* USB connection is too slow for Sample Rates >15 Msps (testet on Nexus 7)
* FileWriter in example app is too slow. Only works for ~ 2 Msps on old devices.
* Not much testing so far...


Installation / Usage
--------------------
To build the library and the example app by using Eclipse + ADT plugin:
* Create new Android project from existing sources: directory hackrf_android/
* Create new Android project from existing sources: directory hackrf_android/examples/

If you want to use the library in your own app, just copy the bin/hackrf_android.jar
file into your project and include it as a library. See the example project to
learn how to use the library.

The hackrf_android.jar and the HackRF_Test.apk files are also in this repository
so that they can be used without building them. But they won't be synched to the
latest code base all the time.

A short howto to get started can be found on this blog post:
[http://tech.mantz-it.com/2014/10/hackrfandroid-using-hackrf-with-android.html]
(http://tech.mantz-it.com/2014/10/hackrfandroid-using-hackrf-with-android.html)


License
-------
This library is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public
License as published by the Free Software Foundation; either
version 2 of the License, or (at your option) any later version.
[http://www.gnu.org/licenses/gpl.html](http://www.gnu.org/licenses/gpl.html) GPL version 2 or higher

principal author: Dennis Mantz <dennis.mantzgooglemail.com>

principal author of libhackrf: Michael Ossmann <mikeossmann.com>
