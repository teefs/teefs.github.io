---
layout: post
title: Bike Photobooth
img: "assets/img/projects/bike/IMG_5574.jpg"
tags: [Embedded, Bicycles, Photography]
---
![image]({{ site.baseurl }}/{{ page.img }})
This project combines my hobbies of cycling and photography. The aim of this project is to reliably capture action shots of cyclists by automating.

The photobooth works by placing a pressure plate in the path of a cyclist. When the cyclist rides over the plate, an Arduino triggers a Canon Rebel XSi's shutter. The camera's focal length and lighting needs have previously been set by taking test shots on-location.

The pressure plate is made with a force sensitive resistor (FSR) pad that has been ruggedized by sandwiching it between pieces of Ikea's flexible cutting board. The FSR varies between ~1M Ohm when unloaded to ~250 Ohm when loaded with mass of 10kg or greater.

The sensor is places between ground and an Arduino input with it's internal 20k Ohm pull-up enabled. The resistor divider created pulls the input high when unloaded and low when loaded.

The Rebel XSi uses a 2.5mm phone jack, also called a Tip, Ring, Sleeve (TRS) plug, as it's remote shutter port. The signals on the TRS plug are as follows: Shutter on the tip, Focus on the ring, and Ground on the sleeve. A remote shutter acts as a switch to ground on of the two signals to auto-focus the camera or actuate the shutter.

The remote shutter functionality is accomplished with an N-channel MOSFET. The Arduino and camera are common grounded, and the FET's gate is triggered by an Arduino output. When the FET is conducting, it connects the sleeve and tip of the TRS plug.

This project could easily be accomplished without the Arduino by powering the resistor divider in the pressure plate circuit with say a 9V battery, and then triggering the shutter circuit's NMOS directly. The Arduino, however, allows for easy extension of functionality. In the future the photobooth could be reconfigured to use external flashes or a camera that uses a Bluetooth or IR based remote shutter control. The Arduino will allow easy setting of flash delay or connecting to the camera's remote shutter.