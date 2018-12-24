---
layout: post
title: Tango Sentio
name: 2018-05-12-tangosentio

tags: [hardware, software]

images:
  - 2018-05-12-tangosentio1.jpg
  - 2018-05-12-tangosentio2.jpg
  - 2018-05-12-tangosentio3.jpg
  - 2018-05-12-tangosentio4.jpg

links:
  - Source Code: https://github.com/jsayles/tangosentio
  - Adafruit Feather M0 Express: https://www.adafruit.com/product/3403
  - BNO055 9-DOF Absolute Orientation Sensor: https://www.adafruit.com/product/2472

---

Name derived from Latin tango: touching, and sentio: seeing.  No, I don't
speak Latin but I can google until I find something that sounds interesting enough.

Tango Sentio is a 3D Scanner Glove using the Bosch BNO055 Absolute Orientation
9-DOF sensor. The device straps to your middle finger and scans an object as you
move your hand across it. The scan is then imported in to Rhinoceros and
multiple scans can be combined to create a full 3D model.

At the time of this posting I haven't completed the software to prove/disprove
if this concept will work.  Accelerometers are not a good way to calculate position
although a number of factors make me think we can overcome the shortcomings. First,
each pass starts at a known location (0,0,0) and a go pretty quickly
so the degradation of accuracy over time is minimized.  Second, the resulting
line is loaded in to the 3D modeling software where Katie can assess it and
let me know if I need to redo the pass.  Efficient, no, but that's not the point
here.

I originally used Circuit Python but without interrupts I was too
limited to do everything I wanted to do.  I switched to an arduino client and
moved all calculations in to a server app written in Python.  
