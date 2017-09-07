Wait until we're connected to the Internet.

The Internet may be behind a captive portal, so let's wait for that.

## Installation

If you are using Arch Linux, just `makepkg` and use pacman to install.

If not, you're on your own (patches welcome).

## Service usage

Run `sudo systemctl enable --now wait-online` after installation to activate.

This service will be ordered before `network-online.target`, so your services needing Internet access will be started at the correct time.

## Command line usage

`check-online` will check if we are connected to the Internet and notify `wait-online`. This is the service script.

`wait-online` will wait until we are connected to the Internet (need `check-online` running).

