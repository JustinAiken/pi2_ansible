# Pi2 Ansible

This is the Ansible that sets up my [Raspberry Pi 2](http://www.amazon.com/Raspberry-Pi-Model-Project-Board/dp/B00T2U7R7I?tag=cc0a0-20):
  - Does some common setup (hostname, etc..)
  - Sets up a mySQL server w/ Docker
  - Sets up openHAB w/ Docker
  - Runs a little sinatra app that updates my openHAB's garage door status (w/ Docker)

As a whole this probably isn't very useful to anyone but me, but parts of it might be...

### Prepare the Pi

- 1. Flash the SD card w/ http://blog.hypriot.com/downloads/ (I used the 2015-11-15 build).
- 2. Plug it in and find it's IP address
- 3. `ssh-copy-id pi@xxx.xxx.xxx.xxx` (Default pass is `raspberry`)
- 4. Add the IP to your ssh config and hosts file as 'pi2'
- 5. ssh to the pi:
  - `sudo rpi-update`
  - `sudo apt-get install python`

### Ansible up

- 1. Install Ansible 2.0+
- 2. `cp secrets.sample.json secrets.json` and edit to taste.
- 3. `./go_ans`
- 4. ???
- 5. Profit!
