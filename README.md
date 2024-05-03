Custom setup of sonar configurations within Project DAVE

Based on:
- [https://field-robotics-lab.github.io/dave.doc/contents/dave_sensors/Multibeam-Forward-Looking-Sonar/](project DAVE Multibeam FLS)
- [https://www.blueprintsubsea.com/oculus/oculus-m-series](Oculus sensor)
- [https://github.com/Field-Robotics-Lab/nps_uw_multibeam_sonar/tree/main](DAVE github for dual sonar)



TODO:
- [x] Finish Oculus settings
- [x] Make visible FOV for oculus (like it is for blueview).
- [ ] Make controllable (not fixed position) - e.g. on cmd_vel.
- [ ] Set up the different configurations.



# How to run DFLS environment container:

1. (docker compose up dev)
1. Open VSCode
1. Click the connection and choose Reopen in container (opens as dev container)
1. Install/clone/activate git submodules which entails the custom / configurable ros packages (e.g. this package)
1. Open a bash terminal
1. Use catkin build
    ```bash
    catkin build
    ```
1. source
    ```bash
    source devel/setup.bash
    ```
1. Run the launch file
    ```bash
    roslaunch dave_simulations dual_sonar_config.launch world_number:=1
    ```

dev container source is mounted at ```~/packages```