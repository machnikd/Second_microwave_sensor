# Second_microwave_sensor - The full project report will be created after the initial tests are completed.
This is a project I am currently working on as part of my master's thesis. The sensor is designed to measure the electrical permittivity of objects passing through it, which allows, for example, the measurement of the moisture content of rapeseed grains — this will be its main application.

## Project Report
### Electronics and Telecommunications - Master's thesis
### Author: Damian Machnik
### Date: 8th June 2025

## Table of contents
1. [Project Description and Objectives](#project-description-and-objectives)
   
   1.1. [Project Goal](#project-goal)
   
   1.2. [Project Assumptions](#project-assumptions)

   1.3. [Symulation environment](#symulation-environment)
  
2. [Project results](#project-results)
   
   2.1. [Balun](#Balun)
   
   2.2. [Vertical differential coupled pair](#Vertical-differential-coupled-pair)

   2.3. [Fabricated device](#fabricated-device)
   
3. [Measurements](#Measurements)

   3.1. [Modyfications](#Modyfications)

## Project description and objectives

### Project goal
Rapeseed moisture content is one of the key physicochemical parameters of the seeds, because of its importance for ensuring optimal conditions for seed storage, as well as for determining the time of harvesting.  Measurement techniques usually use a large sample of seeds (in the case of capacitance meters e.g., 100 g). Therefore, the obtained result is an average value representative for the tested sample, but does not give the range of moisture of single seeds in a given batch of material. The project is a prototype of a sensor and a method of measuring moisture content of individual rapeseeds. The system utilizes multiple measurements of a complex reflection coefficient.

### Project assumptions
The sensor was fabricated on Rogers RO4003C laminate (εr = 3.38, tanδ = 0.003), with a substrate thickness of 0.51 mm and copper thickness of 17.5 μm, due to its stable dielectric parameters as a function of frequency and mechanical strength.
The active part of the sensor will consist of coupled lines arranged one above the other, into which a differential signal will be introduced.The differences between the returning signal and the reference signal will be analyzed, and based on them, information about the electrical permittivity (moisture content) of the rapeseed grain will be determined.
The sensor should be as broadband as possible and matched at a center frequency of 5.8 GHz.

### Symulation environment 
The Balun simulations were carried out using the AWR Cadence simulation software, while the simulations of the coupled lines were performed in HFSS due to the need for 3D analysis.


## Project results

### Balun 
The Balun design was implemented using a Wilkinson power divider and a Schiffman phase shifter. These structures were designed to have a sufficiently wide bandwidth around 5.8 GHz.

To achieve a wider bandwidth, a two-stage Wilkinson power divider had to be implemented:

![Wilkinson](images/Wilkinson.jpg)
![Wilk_char](images/Wilk_char.jpg)

To achieve a 180° phase shift between signals over a wide bandwidth, it was necessary to design a special Schiffman phase shifter structure based on the First and Second Phase Periods in a Coupled Line (the phase shift is marked in pink):

![schiffman](images/schiffman.jpg)
![schiffman_char](images/schiffman_char.jpg)

After connecting and designing the outputs, the entire structure of Balun is presented as follows:

![Balun](images/Balun.jpg)
![Balun_char](images/Balun_char.jpg)

### Vertical differential coupled pair
The simulation investigated the impact of various parameters of two coupled lines, including:
- the width and length of the transmission lines,
- the line tapering,
- the length of the connection to the Balun,
- the ground plane cutout in the Balun,
- the spacing between the lines,
- as well as other minor parameters.
- 
Between these lines, the moisture content of rapeseed will be measured.
The final design and characteristics of the lines are presented as follows:

![lines](images/lines.jpg)



### Fabricated device
Both the Balun and the coupled lines were fabricated using laser printing, and after preliminary testing with a spectrum analyzer, they were connected together using soldered joints.
To avoid unwanted damage and destruction of soldered connections, a casing was created using a 3D printer.
The entire construction is presented as follows:

![sens_s](images/sens_s.jpeg)
![sens_d](images/sens_d.jpeg)

The sensor exhibits considerable losses, primarily due to radiation from the coupled lines. The S parameters of the senor is presented as follows: 

![Sens_S_param](images/Sens_S_param.jpg)

The results of measurements conducted with a glass and a metal sphere moving over the sensor are presented below:

![glass_meas](images/glass_meas.jpg)
![Met_meas](images/Met_meas.jpg)


It can be observed that the influence of objects moving between the coupled lines increases with their electrical permittivity. 

Moist grains exhibit higher electrical permittivity, which is reflected in the sensor response as shown above. In this way, the moisture content of the grain will be determined.

## Measurements

### Modyfications
To enable repeated measurements of rapeseed without the need for human intervention, a system with circular lines was proposed (eliminating the problem of inserting a seed once it passes through the structure). The seed rotates inside the sensor, while the measurement system collects reflection-coefficient data. To set the seed in motion, pressurized air is used and injected in the appropriate direction.

The sensor and its measuring system are shown below:

![sensor_plus_msystem](images/sensor_plus_msystem.jpg)

The entire system during measurements looks as follows:

![sens_measurent](images/sens_measurent.jpg)

