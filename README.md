UCSB Dining Hall Data Science Project
==========

Abstract
==========
The goal of this project is to quantify trends from dining common camera data and give an accurate prediction of the number of people at each of the three locations (Carillo, DLG, and Ortega) and its relative popularity at a given time. This is accomplished through the dining cams API pulling images via the UCSB mealtime project, the ImageAI library and yolov3 model performing image detection on the images, and then using pandas and matplotlib to analyze the output data from a CSV. 

Contributors 
==========
-   Alex Lai
-   Matt Luckenbihl
-   Roy Luengas

Motivation
==========
Frustrated of waiting in long lines at dining halls? Wouldn't you like to know when they are less busy?
<img src='https://github.com/dining-hall-warriors/dining-hall-ds/blob/master/figure-markdown/93d1c681483b130b5f1c72ed2cbadb2b.jpg'>      

We do too.                                                                                                                          
                                                                                                                               
Dependencies
=============
ImageAI
https://github.com/OlafenwaMoses/ImageAI

Pandas Library

YoloV3 (place in dining-hall-ds directory):
https://github.com/OlafenwaMoses/ImageAI/releases/download/1.0/yolo.h5

Image acquisition is thanks to the UCSB Mealtime project by Tim Nguyen:
https://github.com/timothydnguyen/ucsb-mealtime

Methodology
==========
Objective: Informing students about the relative popularity of each dining hall.
First, the UCSB Mealtime library pulls images from the cameras of Carillo, DLG, and Ortega dining halls.
Next, our script uses ImageAI and the Yolo model to count the number of people in a frame, and outputs
this data to a CSV. Now we can use statistical analysis to compare the current count of humans to a 
moving average, and find correlations between popularity and other factors.

<img src = 'https://github.com/dining-hall-warriors/dining-hall-ds/blob/master/figure-markdown/c021219T195554new.jpg'>


Graphing Data
=============
This is a scatterplot of some of our data from 20:00 to 20:25 military time, so 8:00 to 8:25 pm in UCSB dining halls:

<img src ='https://github.com/dining-hall-warriors/dining-hall-ds/blob/master/figure-markdown/scatter.png'>

A better way to see the data is a histogram that plots the variable of time with people as the weights.

<img src ='https://github.com/dining-hall-warriors/dining-hall-ds/blob/master/figure-markdown/Histogram.png'>

Future Work
=============
-   Method to track individuals to tell who is leaving or entering in order to improve data accuracy (foviated vision)
-   Create web interface that shows live relative popularity and predicted people in line
-   Explore correlations between popularity and weather, day/time, menu items, etc.
