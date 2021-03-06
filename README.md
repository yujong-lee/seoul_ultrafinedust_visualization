# Seoul_Ultrafine dust_Visualization
Seoul Ultrafine-dust Visualization using Open data.

## Overview
This is simple visualization of Ultrafine-dust in Seoul. Data used for this project is measured through Smart Seoul City Data Sensor (S-DoT) installed in 850 locations in Seoul.
* Ultrafine dust, Fine dust
* Temperature
* Humidity
* Illumination
* Noise
* Vibration
* Ultraviolet light
* Wind speed
* Wind direction
* Etc 

The above items were measured, but I focused on Ultrafine dust only. 

Dust data is measured using a simple measuring instrument (grade 2). So it does not indicate the accurate air pollution level. Although, it's enough to identify changes over time and visualize.

## Process
I followed these steps.
1. Get raw CSV data file.
2. Remove unnecessary columns and rename ids.
3. Rearrange data, get median value from 850 data of each hour, and write CSV file using perl script.
5. Check CSV file and append first row. (because 00:00 data of first day is empty)
6. Processing reads final CSV and visualize it.
7. Done.

## Example
Image below is visualization of data from April and May in 2020. 

* One small square represents specific hour of a day. Darker square means higher dust value.
* Each dust value used to set grayscale is median value of 850 datas.
* Last line of April image is empty because April has only 30 days. 
* Maximum (median)dust value is 98.34230769 in April, and 119.9310345 in May. 
* **Values 63.75 and above were all painted pure black.**

<img src="https://github.com/yujong-lee/seoul_ultrafinedust_visualization/blob/master/example.png" width="110%"></img> 

## Acknowledgments
* Perl module [Parse::CSV](https://metacpan.org/pod/Parse::CSV) was a great help in carrying out this project.
* This project is based on the Seoul IoT city data, and the results are not related to the city.

본 자료는 [서울시 IoT도시데이터 자료](http://data.seoul.go.kr/dataList/OA-15969/S/1/datasetView.do#)를 활용한 것이며, 연구 결과는 서울시와 관련 없음을 밝힙니다.
