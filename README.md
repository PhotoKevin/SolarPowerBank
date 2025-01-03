# SolarPowerBank
Solar charged power bank

This is a replacement for one I had cobbled together using some ready made boards. The redesign is intended to
address two major areas:

* Airline compatible. Commercial units tend to be all-in-one. You can't separate the battery pack from the solar
panel. This is a problem since you can't put LIon batteries in checked luggage. This unit is designed to be
separate from the panel.
* Fast charge. The old one could only do 500mA charging.  The idea is to keep a battery charging all day and
be able to quick charge a phone.
* Designed to go in a box. If you build something from pre-made boards such as those from AdaFruit, the connectors
are all on the board. This is set up to use "panel mount" connectors.

## Hardware design
The design works around two integrated circuits. A Texas Instruments BQ25185 and an iSmartWare SW2303.

### BQ25185
The TI BQ25185 is a multi-chemistry battery charging controller. The key feature for this application is that it's solar compatible. Solar panels will shut down if you try to draw too much current from them. This can lead to an infinite start/stop cycle which is inefficient and will reduce battery life. [Datasheet](http://www.ti.com/lit/ds/symlink/bq51050b.pdf)

### SW2303
The iSmartWare SW2303 is a fast USB charging module. [Datasheet](http://www.ismartware.cn/upload/goods/20220721/202207211507542921.pdf)
