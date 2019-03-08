---
layout: post
title: Valentine's Day Photobooth
img: "assets/img/projects/valentines/valentines_splash.png"
tags: [Embedded]
---
<p align="center">
  <img src="https://raw.githubusercontent.com/teefs/teefs.github.io/master/assets/img/projects/valentines/310.png"/></p>
A quick little project that I cooked up for Valentine's day 2016. An old laptop, Arduino, computer monitor and printer were used to make the photobooth.

A python script running on the laptop takes an HD webcam, overlays a Valentine's day filter, and displays it to the user. Users can take a photo and then save or discard it by interacting with pushbuttons in the photobooth. The pushbuttons are connected to an Arduino that registers button pushes then communicates with the python script over USB.

When a photo is taken, the python script displays it to the user and if the user chooses to save it the python script calls a print utility so the user can get a physical photo on nice photo paper.