Kalman Filter and Plot
=============
Overview
simple kalman filter by c++. You can also use matlibplot(python plot tool) in c++.
it's good to start from this to learn KF

## Description
Kalman.cpp(hpp) is kalman filter lib
matlibplotcpp.h is plot tool
kalman-test.cpp is kind of main.cpp. get the sensor data and call kalmanfilter and plot

## Demo
![Screenshot from 2019-11-24 21-46-29](https://user-images.githubusercontent.com/45687080/69494896-31eb2000-0f04-11ea-951e-9304ab4f59ab.png)

## Requirement
c++ 11
I tried ubuntu16.04(virtual box) or ubuntu18.04
python2.7(if you have pyhton3, take care not to find python3. there is conflic)
matliplot

## Usage

## Install
```
$apt install install python2.7
$apt-get install python-matplotlib
$git clone https://github.com/yokosyun/KF.git
$cd KF
$mkdir build
$cd build
$cmake ..
$make
$./kalman-test

```

##error
when you cmake .. and you got error. it means cmake find python3. make sure it use python2.7
```
undefined reference to `PyString_FromString'
```

