# AOBL - arch-opt-bin-lib

Some useful bash scripts that are being installed to `/opt/bin` in your arch distro.

## Included scripts

### User scripts

- [.bashrc](./src/.bashrc): Useful shell extensions and requirements for OBL
- [aobl](./src/aobl): Manager for this bash scrips
- [pkg](./src/pkg): Simplified pacman/yay wrapper

### Root scripts

Root scripts require to be logged in via `su` and won't be available, globally, so you need to run `cd /opt/bin` beforehand.

- [su-hostname-setup](./src/su-hostname-setup): Quick way to change the hostname.

## Develop

### Add new script

- `./new scriptname`

### Deploy

- `./deploy YOUR_SCP_TARGET_HOST`

## Install

In Arch Linux, download and install the scripts and modify your `.bashrc` and `.bash_profile`, if you haven't done it, already:

- `curl -s https://arch.martin-braun.net/download/obl.tar.gz | sudo tar xvz -C /opt && sudo chmod -R +x /opt/bin` (Use your own download link, if you modified and deployed yourself.)
- `echo source /home/username/.bashrc > /home/username/.bash_profile`, if not done, already
- `echo source /opt/bin/.bashrc > /home/username/.bashrc`, if not done, already
- `exit` to restart shell

## Update

In Arch Linux you can use the built-in updater.

- `aobl upd YOUR_DOWNLOAD_LINK && exit` or just `aobl upd && exit` for the official download
