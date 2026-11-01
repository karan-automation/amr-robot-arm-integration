# Architecture

## High-level flow

1. Sensors provide LiDAR, IMU, and depth information to the robot stack.
2. ROS / ROS 2 handles localisation, mapping, transforms, and navigation.
3. Nav2 executes mobile navigation toward task locations.
4. A task coordination layer determines when the manipulation stage should begin.
5. MQTT is used to exchange commands/status with the robotic arm.
6. RViz/RViz2 and simulation tools are used for visualisation and debugging.

## Main interfaces

| Interface | Purpose |
| --- | --- |
| LiDAR -> ROS | Mapping and obstacle information |
| IMU -> ROS | Motion/orientation sensing |
| RealSense -> ROS | Depth perception |
| TF | Coordinate-frame relationships |
| Nav2 | Navigation and goal execution |
| MQTT | AMR-to-arm communication |
| Jetson | Edge compute platform |

More detailed diagrams and launch/configuration references will be added as the original workspace is organised.
