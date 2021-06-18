# setup
Tools for setting up remote jupyter servers in AWS ubuntu instances

Overly simplified version of [fastsetup](paste link here)

## Steps
0. `ssh -L localhost:8888:localhost:8888 ubuntu@<ip_adress>` --> to be able to connect to jupter server from browser

1. Installing mamba and other basic stuff: 
  - `wget https://raw.githubusercontent.com/Space-Intelligence/setup/main/setup.sh`
  - `. ./setup.sh`

2. Reboot and install nvidia drivers (if using GPU instance)
  - `ubuntu-drivers devices` --> select appropriate driver from the list for next step:
  - `sudo apt install -y nvidia-driver-460-server`
  - `sudo modprobe nvidia`
  - `nvidia-smi`
