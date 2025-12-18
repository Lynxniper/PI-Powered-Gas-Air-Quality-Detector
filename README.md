# PI-Powered-Gas-Air-Quality-Detector

Overview: 
This project implements a gas leak and smoke detection system using a Raspberry Pi Pico, MQ-6 gas sensor, and MQ-135 air-quality sensor. The system monitors LPG gas leaks, smoke, and hazardous fumes, compares them to calibrated thresholds, and activates alarms to warn residents. It is designed as a cost-effective, DIY home-safety mechanism suitable for Indian households.

Problem Context: 
Indian homes rely heavily on LPG cylinders, and accidental gas leaks or smoke exposure can lead to severe injuries, fires, or fatalities. Many households lack commercial smoke detectors due to cost and awareness barriers.
This project provides an accessible, low-cost safety solution that can act as a complementary early-warning system.

System Features:
1. MQ-6 Gas Detection: Triggers when LPG levels exceed threshold
2. MQ-135 Smoke & VOC Detection: Analog sensing of smoke, benzene vapors, and air quality
3. Real-Time Alerts: LED or buzzer-based alarms (customizable)
4. Threshold Calibration: Digital + analog sensor thresholding
5. Continuous Monitoring: Live reading loop for instantaneous hazard detection
6. Expandable Design: Supports optional LCD/OLED display output

Hardware Components:
1. Raspberry Pi Pico
2. MQ-6 Gas Sensor (digital output)
3. MQ-135 Air Quality Sensor (analog output)
4. Breadboard, jumpers, power supply
5. LCD/OLED display, buzzer, LED

System Architecture: 
1. The Raspberry Pi Pico acts as the controller:
2. Reads MQ-6 digital output for LPG detection
3. Reads MQ-135 analog output via ADC for smoke/VOC detection
4. Compares readings to preset thresholds
5. Activates alarms if unsafe levels are detected

Algorithm (Simplified):
1. Initialize GPIO + ADC pins
2. Continuously read MQ-6 digital output
3. Continuously sample MQ-135 analog voltage
4. Convert analog reading via ADC
5. Compare both sensor readings against thresholds
6. Trigger alarm if either exceeds limits
7. Repeat indefinitely

Results:
1. System successfully detects both LPG leaks and smoke
2. Threshold logic works reliably during testing
3. Alarm mechanism activates instantly when hazrds detected
4. System is suitable as an additional household safety tool

Future Enhancements:
More accurate calibration
Data logging and trend visualization
Battery-backup system
Integration with smart home devices
