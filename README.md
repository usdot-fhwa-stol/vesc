# Veddar VESC Interface

![ROS2 CI Workflow](https://github.com/f1tenth/vesc/workflows/ROS2%20CI%20Workflow/badge.svg)

Packages to interface with Veddar VESC motor controllers. See https://vesc-project.com/ for details

This is a ROS2 implementation of the ROS1 driver using the new serial driver located in [transport drivers](https://github.com/ros-drivers/transport_drivers).

## Changes made from upstream

* Updated `README.md` with this change notice
* Negated the `current_speed` value in `vesc_to_odom.cpp`

## How to test

1. Clone this repository and [transport drivers](https://github.com/ros-drivers/transport_drivers) into `src`.
2. `rosdep update && rosdep install --from-paths src -i -y`
3. Plug in the VESC with a USB cable.
4. Modify `vesc/vesc_driver/params/vesc_config.yaml` to reflect any changes.
5. Build the packages `colcon build`
6. `ros2 launch vesc_driver vesc_driver_node.launch.py`
7. If prompted "permission denied" on the serial port: `sudo chmod 777 /dev/ttyACM0`


# CARMAPlatform
The primary CARMAPlatform repository can be found [here](https://github.com/usdot-fhwa-stol/CARMAPlatform) and is part of the [USDOT FHWA STOL](https://github.com/usdot-fhwa-stol/)
github organization. Documentation on how the CARMAPlatform functions, how it will evolve over time, and how you can contribute can be found at the above links as well

## Contribution
Welcome to the CARMA contributing guide. Please read this guide to learn about our development process, how to propose pull requests and improvements, and how to build and test your changes to this project. [CARMA Contributing Guide](https://github.com/usdot-fhwa-stol/CARMAPlatform/blob/develop/Contributing.md) 

## Code of Conduct 
Please read our [CARMA Code of Conduct](https://github.com/usdot-fhwa-stol/CARMAPlatform/blob/develop/Code_of_Conduct.md) which outlines our expectations for participants within the CARMA community, as well as steps to reporting unacceptable behavior. We are committed to providing a welcoming and inspiring community for all and expect our code of conduct to be honored. Anyone who violates this code of conduct may be banned from the community.

## Attribution
The development team would like to acknowledge the people who have made direct contributions to the design and code in this repository. [CARMA Attribution](https://github.com/usdot-fhwa-stol/carma-platform/blob/develop/ATTRIBUTION.md) 

## License
By contributing to the Federal Highway Administration (FHWA) Connected Automated Research Mobility Applications (CARMA), you agree that your contributions will be licensed under its Apache License 2.0 license. [CARMA License](https://github.com/usdot-fhwa-stol/CARMAPlatform/blob/develop/docs/License.md) 

## Contact
Please click on the CARMA logo below to visit the Federal Highway Adminstration(FHWA) CARMA website.

[![CARMA Image](https://raw.githubusercontent.com/usdot-fhwa-stol/CARMAPlatform/develop/docs/image/CARMA_icon.png)](https://highways.dot.gov/research/research-programs/operations/CARMA)
