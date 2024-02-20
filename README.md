# U6143_ssd1306 Set-up Guide Pi Rack W/ Oled Display
This comprehensive walkthrough will guide you through the process of correctly setting up your UCTRONICS OLED Pi-rack. While not an official setup guide, it provides detailed instructions beyond what is typically available online, ensuring successful setup and operation.
If you encounter error 127 during the 'make && compile' process of your display, or face the 'externally-managed-environment' error, this guide may resolve these issues for you.
## Intro
Navigate to your home directory:
(Replace "thenameofyourpi" with your actual Pi or computer name.)
We are starting this tutorial assuming you have already installed a fresh copy
of Ubuntu or Raspi/Debian.
```bash
cd /home/thenameofyourpi/
```
Install necessary packages:

##  Install python3 
```bash
sudo apt install python3-pip
```
## Remove the externally managed library causing errors: 
```bash
sudo rm -rf /usr/lib/python3.11/EXTERNALLY-MANAGED
```
## Install the U6143_ssd1306 library from GitHub & Other Prerequisites: 
```
git clone https://github.com/UCTRONICS/U6143_ssd1306.git
```
```
sudo pip3 install adafruit-circuitpython-ssd1306
```
```
sudo apt-get install python3-pil
```
```
sudo apt-get install raspi-config
```
## Ensure that I2C is enabled in the Raspberry Pi configuration and reboot the system.
- After reboot, navigate to the directory containing the display code: 
```bash
cd /home/thenameofyourpi/U6143_ssd1306/C
```
- Clean and compile the display code:
```bash
sudo make clean && sudo make
```
- Run the display:
```bash
sudo ./display
```
- Press Ctrl + C to exit after seeing the display run and then run command below and close window:
```bash
sudo nohup ./display
```

Your display should now be working properly mess with the customization you can follow the original fork to this.

:)





