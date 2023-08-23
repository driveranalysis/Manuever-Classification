# Manuever-Classification and Pre-Processing
This codebase contains the main scripts used to load, transform and analyze the various driving datasets related to our FYP - Driver Scoring System.

## Problem Statement
With the advancements in technology in the mobility sector, such as self-driving cars, it is important to not forget, that while we are taking a step towards the futuristic world of popular media (read: cyberpunk), the rollout of these technologies would not be uniform given that there are countries that still don't have good road infrastructures, etc. And so it is imperative that we tackle the problems associated with Mobility, and do so in a manner that requires minimal intervention and redesign of existing systems, such that we can implement it in countries like Pakistan. As it stands, the two major problems associated with Mobility are Fuel Efficiency and Exposure to risk.

## Solution
The solution that we have designed is a Driver Scoring System. It is based on the fact that both of these problems of mobility are majorly caused by the human use of technology, rather than the limitations of technology itself. To put it into context, around 90% of road accidents are caused due to human errors, and based on the driving style, fuel efficiency can vary by about 30%. This correlation between driving style and fuel efficiency/risk validates our idea that if we develop a system that can quantify driving behavior and convey it to the driver in a way that enables and motivates change, then we could reduce accidents and increase mileage.

Our solution is designed to have minimal intervention in the current way of driving, so as to ensure that our solution could be easily adopted and incorporated into the user flow. It is implemented using a 3+1 module system, where the first three modules; Data Collection, Motion Tracking, and Maneuver Classification are the enabling modules, which will feed into the fourth module i.e. driver scoring.

The data for a single trip is collected from the IMU and GPS units of the user’s smartphone. This is then processed to calculate a high-accuracy lane-level mapping of the trajectory of the vehicle, using the motion tracking module, and various predefined maneuvers that occur during the trip are classified using the maneuver classification module. The output from both of these modules is then used to calculate multiple driving scores
for various metrics, and a complete overall driving score.

![image](https://github.com/driveranalysis/Manuever-Classification/assets/29225983/dd43a707-eb65-43b2-afdb-f2067264f7ad)

This section focuses on Maneuver Classification

## Example
Our Maneuver Classification process relies on the fact that each Maneuver (e.g. Aggressive Right Turn, Acceleration, etc.) showcases a distinct pattern in the combined view of the Accelerometer, Gyroscope, and Magnetometer. And so depending on our definition of the magnitude and timeframe that we look at, we can easily identify these maneuvers from a pre-processed dataset.

![image](https://github.com/driveranalysis/Manuever-Classification/assets/29225983/aa81609d-d241-490d-973d-ca342bb1ee9b)


[p5]: <https://p5.readthedocs.io/en/latest/install.html>
[splash]: <https://raw.githubusercontent.com/mazy1998/MancalaAI/master/scr1.png>
