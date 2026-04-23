# klipper-toolchanger for Klicky-Changer

## This is a "very light, bare minimum" copy of Viesturz's Klipper-Toolchanger software
## This is/or will be modified to work with my version of a toolchanger, that uses Klicky-Probe as Z-Probe, named Klicky-Changer.
## Use this page only for the klipper-toolchanger plug-in installation, the hardware and configs for Klicky-Changer can be found [here](https://github.com/printicus/Klicky-Changer)


# Installation

To install this plugin, run the installation script using the following command over SSH. This script will download this GitHub repository to your RaspberryPi home directory, and symlink the files in the Klipper extra folder.

```
wget -O - https://raw.githubusercontent.com/printicus/Klipper-Toolchanger-for-Klicky-Changer/main/install.sh | bash
```

Optional, ad this to your moonraker.conf to enable automatic updates:

```
[update_manager klipper-toolchanger]
type: git_repo
channel: dev
path: ~/klipper-toolchanger
origin: https://github.com/printicus/Klipper-Toolchanger-for-Klicky-Changer.git
managed_services: klipper
primary_branch: main
```

If an update has new klipper files, they will not be automatically installed into Klipper. You will need to run the intall script manualy to add them:

```
bash ~/klipper-toolchanger/install.sh
```
