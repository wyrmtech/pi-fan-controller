# Pi Fan Controller

Raspberry Pi fan controller.

## Description

This repository provides scripts that can be run on the Raspberry Pi that will
monitor the core temperature and trigger an output on GPIO 18

In my case this is then monitored via a Raspberry Pico to start the fan bank in my rack when the temperature reaches
a certain threshold.

fancontrol.py modified from the original to control the fan on pin12 (GPIO 18)

# To use this code

I would suggest that you run the following first to make sure everything is up to date:

sudo apt update

sudo apt full-upgrade

N.B, Updates were getting stuck connecting to one of the repositories, if that happens try this:

apt-get -o Acquire::ForceIPv4=true update

apt-get -o Acquire::ForceIPv4=true -y dist-upgrade

# If you don't already have git installed, you'll need to install git first using 

sudo apt-get install git

# Clone the code

git clone https://github.com/wyrmtech/pi-fan-controller.git

# Install the requirements:

# If pip is not already installed run:
sudo apt install python3-pip
or if getting stuck reading the repository
sudo apt-get -o Acquire::ForceIPv4=true install python3-pip

# Install requirements globally
sudo pip3 install -r pi-fan-controller/requirements.txt

# Run the install script:

./pi-fan-controller/script/install

You'll have to either install a fan or use a Raspberry Pico to monitor.
Details can be found at (TBC)
