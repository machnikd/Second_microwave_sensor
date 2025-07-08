# Second_microwave_sensor
"This is a project I am currently working on as part of my master's thesis. The sensor is designed to measure the electrical permittivity of objects passing through it, which allows, for example, the measurement of the moisture content of rapeseed grains — this will be its main application."

## Project Report - The full project report will be created after the initial tests are completed.
### Electronics and Telecommunications - Master's thesis
### Author: Damian Machnik
### Date: 8th June 2025

## Table of contents
1. [Project Description and Objectives](#project-description-and-objectives)
   
   1.1. [Project Goal](#project-goal)
   
   1.2. [Project Assumptions](#project-assumptions)

   1.3. [Symulation environment](#symulation-environment)
  
2. [Project results](#project-results)
   
   1.1. [Balun](#Balun) 
   
4. [What will be done](#What-will-be-done)

## Project description and objectives

### Project goal
Rapeseed moisture content is one of the key physicochemical parameters of the seeds, because of its importance for ensuring optimal conditions for seed storage, as well as for determining the time of harvesting.  Measurement techniques usually use a large sample of seeds (in the case of capacitance meters e.g., 100 g). Therefore, the obtained result is an average value representative for the tested sample, but does not give the range of moisture of single seeds in a given batch of material.The system utilizes multiple measurements of a complex reflection coefficient that correspond to different positions and orientations of a seed under test along the sensor.

### Project assumptions
The sensor was fabricated on Rogers RO4003C laminate (εr = 3.38, tanδ = 0.003), with a substrate thickness of 0.51 mm and copper thickness of 17.5 μm, due to its stable dielectric parameters as a function of frequency and mechanical strength.
The active part of the sensor will consist of coupled lines arranged one above the other, into which a differential signal will be introduced.The differences between the returning signal and the reference signal will be analyzed, and based on them, information about the electrical permittivity (moisture content) of the rapeseed grain will be determined.
The sensor should be as broadband as possible and matched at a center frequency of 5.8 GHz.


### Symulation environment 
The Balun simulations were carried out using the AWR Cadence simulation software, while the simulations of the coupled lines were performed in HFSS due to the need for 3D analysis.


## Project results

### Balun 
The Balun design was implemented using a Wilkinson power divider and a Schiffman phase shifter. These structures were designed to have a sufficiently wide bandwidth around 5.8 GHz.

Two-stage Wilkinson power divider:
