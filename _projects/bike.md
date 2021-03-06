---
layout: post
title: Bike Photobooth
img: "assets/img/projects/bike/bike_splash.jpg"
tags: [Embedded, Bicycles, Photography]
---
<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/bike/IMG_5574.jpg"/></p>

This project combines my hobbies of cycling and photography. The aim of this project is to reliably capture action shots of cyclists by automating.

The photobooth works by placing a pressure plate in the path of a cyclist. When the cyclist rides over the plate, an Arduino triggers a Canon Rebel XSi's shutter. The camera's focal length and lighting needs have previously been set by taking test shots on-location.

The pressure plate is made with a force sensitive resistor (FSR) pad that has been ruggedized by sandwiching it between pieces of Ikea's flexible cutting board. The FSR varies between ~1M Ohm when unloaded to ~250 Ohm when loaded with mass of 10kg or greater. The sensor is places between ground and an Arduino input with it's internal 20k Ohm pull-up enabled. The resistor divider created pulls the input high when unloaded and low when loaded.

<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/bike/plate.jpg"/></p>
  
The Rebel XSi uses a Tip, Ring, Sleeve (TRS) plug as it's remote shutter port. The signals on the TRS plug are as follows: Shutter on the tip, Focus on the ring, and Ground on the sleeve. The remote shutter circuit is shown below.

<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/bike/remoteshutter.png"/></p>

This project could easily be accomplished without a microcontroller, but the Arduino allows more flexibility in that it can allow multiple pictures, with variable timing between them, to be taken and for multiple remote flashes to be added to the system.

Below are some more shots taken from the first day of testing.

<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/bike/IMG_5578.jpg"/></p>

<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/bike/IMG_5580.jpg"/></p>
  
<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/bike/IMG_5581.jpg"/></p>