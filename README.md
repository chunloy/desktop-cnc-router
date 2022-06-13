# Desktop CNC Router

![Completed build](https://user-images.githubusercontent.com/101907461/173199412-cda32b4c-4a96-4f4e-9c13-d15074b31326.jpeg)

## Introduction

As the title suggests, this README is about my creation process of a desktop CNC router. First, I'll discuss why I decided to build this and the process that went into its construction. This project challenged me to learn different workflow patterns in new CAD software (Fusion 360) and design principles related to 3D printing. I had a lot of fun throughout this process and hope this project inspires you to tinker with your creations. 

The motivation for this project stems from my passion for microcontrollers. Previously my prototypes relied on many jumper wires and breadboards, which were not appealing. I needed a way to make custom circuit boards so my devices could be more compact. Additionally, I wanted the option to work with other materials such as acrylic, wood, and aluminum. All of this sounds like a job for a CNC! But what does CNC mean? CNC stands for *computer numerical control* and refers to any machining tool whose motion is controlled by a computer. 3D printing is an example of a CNC.

Entry-level CNCs are becoming quite popular among the hobbyist community, but there are two problems:

1. the working volume is too small for the price
2. the frame is not rigid enough to machine harder materials (metals)

Introducing my very own custom-built CNC router! The foundation of this machine relies upon steel tubing for the frame, custom 3D printed parts for joints, linear guides (trucks), and a tool head mount. In addition, I designed this machine to support additive and subtractive manufacturing processes such as 3D printing, milling, and laser cutting. For milling, I will be using a Makita compact router. Beyond this, the working volume is customizable simply by changing the lengths of the tubing.

## Some Specs

### Size:
* Machine footprint: 32.5in x 28in x  16in
* Working footprint: 17.75in x 13in x 3.25in

### Mechanical:
* 8mm bearings 
* X/Y axes:
  * 16T GT2 pulleys 
  * 20T GT2 idlers
  * 10mm GT2 belts
* Z axis:
  * T8 leadscrew and nut (4 start, 2mm pitch, 8mm/rev)
  * 5mm to 8mm coupler

### Control:
* X/Y axes: 4x NEMA 17 stepper motors (two motors per axis connected in series)
* Z axis: 1x NEMA 17 stepper motor
* BIGTREETECH SKR Pro v1.2 control board
* 3x TMC2209 silent stepper drivers
* Power supply

### Firmware:
* A highly modified version of Marlin (v2.0.9.2) commonly used for 3D printing


## 3D Printed Parts
![All Parts](https://user-images.githubusercontent.com/101907461/173199451-f69baf74-a273-4926-ae92-d8a026a406b6.jpeg)

Each part was modelled in Fusion 360 and designed to eliminate the need for support material. All components were printed on an Ender 3 Pro with an infill ranging from 50%-70% using standard PLA filament. The total printing time for this project exceeded 200 hours due to the number of parts required. Below are some timelapses for this project. Enjoy!

*Note: Timelapses were recorded using a Raspberry Pi Zero 2 and a V1.2 Pi Cam. Adding a microcontroller to control and monitor my 3D printer from my computer was entirely unnecessary for this project, but it was so worth it!*

![Corner Clamp](https://user-images.githubusercontent.com/101907461/173200221-dbace96f-fda9-4c0a-9e75-737fbe668859.gif)

![Trucks](https://user-images.githubusercontent.com/101907461/173200427-d1020b83-f579-41f8-9204-99e1c090c365.gif)

![Z Core](https://user-images.githubusercontent.com/101907461/173200385-c04da978-d328-40c5-ae69-8d98b155f2ae.gif)


## The Build
The total build time for this machine was approximately 20 hours, with most of the time spent making adjustments to ensure proper alignment and engagement between moving and mating components.


### The Feet & Bottom Clamps
![A5F1A762-33D5-4341-9016-7E24A2C5A2BA_1_105_c](https://user-images.githubusercontent.com/101907461/173201833-ea858c31-22a7-4038-b8d9-248c2d399597.jpeg)



### Trucks & Motor
![75F4B961-A491-4A60-92C0-F64122977AA4_1_105_c](https://user-images.githubusercontent.com/101907461/173201902-c9a6ab77-8769-4918-a4a6-eae3f06b97ae.jpeg)


![B3527891-3A84-4063-95D1-094345EC5985_1_105_c](https://user-images.githubusercontent.com/101907461/173201905-706d7772-d1cb-4863-a349-c0f540b5ae8d.jpeg)



### The Core
![A9A1C5E1-FFBC-4B91-8319-85EFFDDCF40C_1_105_c](https://user-images.githubusercontent.com/101907461/173201935-a5f376e5-09ad-44d7-8ace-835d6afb7384.jpeg)



### Completed Assembly
![77958E04-E4F3-4A5C-9B24-DC7824D32903_1_105_c](https://user-images.githubusercontent.com/101907461/173201980-783f0dd8-830c-48ab-bb18-981d21827e49.jpeg)


## Upcoming Work
So far, the machine is built and is functional. However, there are a few pending items:
1. Motor calibration to ensure precise motion
2. Designing and 3D printing enclosures for the control board, screen and emergency stop
3. Implementing a web interface to control and monitor the machine using a computer

