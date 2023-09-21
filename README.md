# Klipper Config

My configs for klipper firmware.

## Printer List

 - Creality CR-10s
 - Creality Ender 3

## Setup
1. Install [KIAUH](https://github.com/dw-0/kiauh).
```sh
sudo apt install git
cd ~ && git clone https://github.com/dw-0/kiauh.git
~/kiauh/kiauh.sh
```
2. Using KIAUH install Klipper, Moonraker, Mainsail, and Crowsnest.
3. Using KIAUH build and flash the Klipper firmware on the mainboard.
4. Setup the config.
```sh
cd ~/printer_data/
rm -rd config
git clone git@github.com:AquaMorph/klipper-config.git config
ln -s ~/Klipper-Adaptive-Meshing-Purging/Configuration ~/printer_data/config/KAMP
```
5. Create printer.cfg file and link to desired printer config.
```sh
emacs printer.cfg
```
```
[include printer/cr10s.cfg]
```
