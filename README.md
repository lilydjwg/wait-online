Wait until we're connected to the Internet.

The Internet may be behind a captive portal, so let's wait for that.

`check-online` will check if we are connected to the Internet.

`wait-online` will wait until we are connected to the Internet.

systemd services are installed so it's managed automatically.

Run `sudo systemctl enable --now wait-online` after installation to activate.
