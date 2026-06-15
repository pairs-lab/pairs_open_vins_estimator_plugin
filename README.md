# pairs_open_vins_estimator_plugin

A pluginlib plugin that registers OpenVINS visual-inertial odometry as a selectable state
estimator inside the PAIRS estimation manager (`pairs_uav_managers`). Once loaded, the UAV
can switch its localization source to OpenVINS, fusing VIO position/velocity/heading
corrections into the lateral, altitude and heading estimators that feed flight control.

## Contents
- `open_vins/OpenVinsEstimatorPlugin` (`open_vins::OpenVins`) — a `pairs_uav_managers::StateEstimator`
  plugin, built as the `PairsUavStateEstimators_OpenVins` library and declared in
  `estimator_plugins.xml`.
- `custom_configs/pairs_uav_managers.yaml` — example manager configuration that wires the
  `open_vins` state estimator (lateral / altitude / heading sub-estimators, corrections,
  transform manager) into the estimation, constraint, gain and transform managers.

## Branches
- `ros1` — ROS 1 Noetic (catkin)
- `ros2` — ROS 2 Jazzy (ament_cmake)

## Install (ROS 1 Noetic)
```bash
sudo apt install ros-noetic-pairs-open-vins-estimator-plugin
```

## License
BSD 3-Clause. Derived from the CTU-MRS `pairs_open_vins_estimator_plugin` package; the original
copyright is retained in [LICENSE](LICENSE).
