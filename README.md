# Seeing the Streets: Urban Junction Classification in Real-Time

This repository contains the code and data pipeline for the thesis **"Seeing the Streets: Urban Junction Classification Through Real-Time Computer Vision and ML Techniques"** by Marya Nabil Mufti. The project proposes a lightweight and scalable system that leverages real-time object detection and machine learning to classify traffic junctions based on behavioral patterns, supporting more informed urban planning decisions.

## Project Overview

The pipeline includes:
- Live video stream processing from YouTube
- Object detection using YOLOv8 (Ultralytics)
- Feature extraction (e.g. vehicle counts, ratios)
- Junction clustering using K-Means
- Classification using a Random Forest model
- Urban planning recommendations based on results

## Morning / Night Runs Code for Data Collection
- Install the following packages: 
!pip install ultralytics yt-dlp opencv-python pandas numpy matplotlib
- switch out the live stream links for your choice of live streams
- set the time interval to your desired time capture
- run and find the finished collected CSV's for your junctions, as well as captured images with bounding boxes for each junction

## Data Analysis Script
- Once data is collected, upload all the CSV's to your google drive
- Install the following packages:
  !pip install ultralytics opencv-python pandas numpy
- Use the Re-running section to re-process any troubled junctions using one of the captued images. Fine tune for more accurate object detection
- Load all data from Google Drive, confirm number of CSV's to upload (71, representing CSV for morning and night for 1 week for each junction, minus the troubled junction that only used 4 CSV's to represent morning and night activity for weekday and weekend)
- enter 'yes' to confirm upload
- Run following chunks to cluster and produce data anlysis charts. Human intervention for clustering reccomended based on Shilloutte scores / nature of the data.
- Run following chunks for pre-proccesing, clustering, validation, and testing. Edit junction categories/recomendations as seen fit for respective project
- Test a new junction to see how well it categorizes based on your training data set, and evaluate results as necessary. It is encouraged to test the new live stream over a longer period of time, including both morning and night, to best understand its traffic activity.

## Notes
- All code was run using Google Colab.

- YOLOv8 was used via the Ultralytics API.

- All detection outputs are based on the COCO classes, with 6 selected classes for this project: person, bicycle, car, motorcycle, bus, and truck.
