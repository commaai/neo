neo
=====

<b>NOTE: The NEO is deprecated. Check out the <a href="https://comma.ai/shop/products/eon-gold-dashcam-devkit">EON</a> for the future</b>

<img src="https://github.com/commaai/neo/blob/master/neo.png">

The neo is an open source robotics research platform. It is powered by a OnePlus 3 smartphone and an [STM32F205](http://www.st.com/en/microcontrollers/stm32f2x5.html?querycriteria=productId=LN1433)-based CAN interface board, in a 3d-printed housing with active cooling.

The neo platform includes [NEOS](https://github.com/commaai/eon-neos), a stripped down Android ROM designed for robustness and to get out of the way of your software. It also provides a modern linux environment for easy development.

Why
------

You cannot get a higher performance embedded processor than what's shipping in modern smartphones. They also come with an impressive array of sensors and radios, and are very low cost.

For some background see the work of [Android Based Robots](http://www.socsci.uci.edu/~jkrichma/ABR/abr_background.html).

Build
------

The neo is designed to be very easy to construct. You need to be able to shop online and use a soldering iron.

There is a **[very detailed guide](https://github.com/commaai/neo/raw/master/guide.pdf)** with instructions on what to order and how to build a neo.

to build a neo, 6 orders must be placed from the following sources:
- digikey
- mcmaster
- shapeways
- oshpark
- amazon
- oneplus

The total cost is about $700.


Directory structure
------

- board -- EagleCAD schematic, board, and library files
- parts -- csv bill of materials
- case -- stl files for 3d printing


Licensing
------

neo research platform is released under the MIT license.

**THIS IS ALPHA QUALITY SOFTWARE FOR RESEARCH PURPOSES ONLY. THIS IS NOT A PRODUCT.
YOU ARE RESPONSIBLE FOR COMPLYING WITH LOCAL LAWS AND REGULATIONS.
NO WARRANTY EXPRESSED OR IMPLIED.**
