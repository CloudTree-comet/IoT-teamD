# IoT Automated Pet Care Solution

**An innovative IoT-based system designed to revolutionize pet care through intelligent feeding automation and comprehensive health monitoring.**

---

## 🐾 Project Overview

This project delivers a cutting-edge automated pet care solution that combines Internet of Things (IoT) technology with smart pet management. Our system ensures your furry friends receive consistent care while providing valuable insights into their health and eating habits.

##  Key Features

###  **Feeding Automation**
- **Consistent Care**: Ensures pets are fed regularly and on time, every time
- **Hands-Free Operation**: Eliminates the need for manual feeding schedules
- **Travel-Friendly**: Provides reliable meal delivery even when owners are away

###  **Scheduled Feeding**
- **Smart Scheduling**: Automated meal times tailored to your pet's needs
- **Customizable Portions**: Adjustable feeding times and portion sizes
- **Pre-Programmed Routines**: Set-and-forget feeding schedules

###  **Weight Monitoring**
- **Consumption Tracking**: Monitors food intake for optimal health management
- **Pattern Recognition**: Analyzes eating habits and behavioral patterns
- **Early Detection**: Identifies potential health issues through consumption data analysis


---

##  Update History
- Complete overall circuit design : 2025-11-06
- Remove buzzer, expand LCD, add 4 buttons : 2025-11-10

---

## Hardware Configuration
- ESP32 Development Board
- 20x4 LCD (I2C)
- 4 buttons (red/green/blue 2)
- RTC DS1307 (Watch Module)
- HX711 + Load Cell (Weight Sensor)
- Servo motor (air inlet opening and closing)

## User Interface
- Red button: Main screen ↔ Slot screen toggle
- Green button: Set mode (time → minutes → weight → save)
- Blue UP button: Slot selection up, setting value up
- Breakdown button: Slot selection down, reduced settings

## Catering Management System
- 3 feeding slots: Time, minute and weight can be set respectively
- Save slot: set value is stored in memory
- Slots displayed: Slots set in "08:30,500g" format

## automatic feeding function
- Time check: check current time with RTC
- Automatic feeding start: 180° rotation of servomotor at set time (air inlet open)
- Weight-based termination: 0° rotation of servomotor when target weight is reached (fastener closed)

## LCD Display
- Main screen: Current time, feed weight, next feeding time
- Slot screen: 3 slot status (set/empty)
- Setting Screen: Time/Minute/Weight Setting Interface
- School meal progress screen: Show status during school meal

## Monitoring Features
- Real-Time Weighing: Current Feed Weighing With Load Cells
- Tracking Meal Progress: Current Status Against Target Weight
- Serial log: Output all operational situations to the serial monitor

---

## the present problem
- Load cell not measured properly
- Servo motor made me go back to 0 degrees if only the current weight is properly measured, I think it's a weight calibration issue
- You have not created the ability to transfer these data (feed intake) to the web or elsewhere

**The flickering screen is due to an RTC update, so you don't have to worry **
