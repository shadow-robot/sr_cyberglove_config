Shadow Robot CyberGlove Configuration
=====================================

Contains the configuration for combining the Shadow Robot Hand with CyberGlove (per person and per CyberGlove)

* [Calibrations](calibrations) - Calibration files for CyberGlove to Shadow Robot hand
* [Mappings](mappings) - Files specifying the mapping of sensor readings from the CyberGlove to Shadow Robot hand joints.

## Adjusting CyberGlove calibration

Depending on the wearer of the CyberGlove, you may find that the calibration needs to be adjusted. To do this, identify the name of the joint that requires adjusting, then find a suitable range of raw readings from the CyberGlove that match your desired range of motion. This can be done by monitoring the topic for CyberGlove with the following command:
```bash
rostopic echo raw/joint_states
```
And selecting an appropriate minimum and maximum value.
The file cyberglove.cal should then be edited, inserting the new raw values taken from the joint_states topic, to coincide with the calibrated minimum and maximum values of that joint, in degrees. 
