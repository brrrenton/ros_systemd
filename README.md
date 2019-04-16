## Description

Service files and instructions for launching ROS at boot with systemd

## Installation

* Copy the service files to `~/.config/systemd/user/`
* In `roscore.service`, ensure that the paths to the system `setup.bash` and `roscore` are correct
* In `roslauch.service`, ensure that the paths to the user `setup.bash` and launch file are correct
* Enable the services with:
```
systemctl --user enable roscore.service
systemctl --user enable roslaunch.service
```
* Enable starting user services at boot with:
```
loginctl enable-linger $USER
```

