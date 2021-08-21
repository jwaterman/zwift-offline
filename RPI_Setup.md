# RPI Setup

I used the rpi-lite image.

## Set timezone

```bash
sudo raspi-config
```
It's under "localization options"

## Enable ssh 

```bash
sudo systemctl enable ssh
sudo systemctl start ssh
```

## Install ssh key on rpi

From the host that wants to ssh into rpi: 

```bash
ssh-copy-id -i ~/.ssh/mykey user@host
```

## Setup python
```bash
sudo apt install python3-pip
pip3 install flask flask_sqlalchemy flask-login pyjwt gevent protobuf protobuf3_to_dict stravalib
```

## Fetch repo

* Install `id_rsa` in `.ssh` to allow access to the git repo. 

## Running

```bash
sudo python3 ./standalone.py
```


