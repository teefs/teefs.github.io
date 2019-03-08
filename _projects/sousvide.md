---
layout: post
title: Sous Vide Machine
img: "assets/img/projects/sousvide/steak_splash.jpg"
tags: [Embedded, Cooking]
---
<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/sousvide/steak.jpg"/></p>
The goal of this project is to make really great steaks. Sous-vide is a method for cooking in which food is placed in pouches and submerged in a gentle water bath. The water bath is kept at a regulated temperature to ensure that the food is not overcooked. If you want to cook a perfect rare steak, you would set the water bath temperature to 53 Celsius[1] let the steak come up to temperature and tenderize then sear the exterior. Until recently, sous-vide has been mostly done with DIY solutions, and I thought this would be a fun project to take on. The project was written in C for use with a TI MSP432P4111 Launchpad in bare-metal. Also used were a temperature sensor, immersion water heater, and water pump.

Project code can be found [here](https://github.com/teefs/sous_vide), and it provides a good overview for how the MSP432 devices are used in this project. A high-level descripton for the machine is below:

The user, using buttons, selects the temperature of the water bath and starts the machine. The Launchpad's LCD screen displays the set-point temperature and current temperature of the water bath, and the screen blinks/ stays solid to indicate the machine is off/ on. When the machine is running a PID controller is initialized and its output is recomputed every minute. The output of the PID controller is fed to the MSP432's PWM module which controls the turning on and off of the immersion heater. The PID controller and the immersion heater switching happens slowly since water is a large thermal mass and has a large time constant.