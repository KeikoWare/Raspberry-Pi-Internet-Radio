# Raspberry-Pi-Internet-Radio

Boot standard Raspbian image

expand filesystem

´´´
$ sudo reboot
$ sudo nano /etc/wpa-supplicant/wpa-supplicant.conf
network={
	ssid="your-wofo-ssid"
	psk ="your-secret_key"
}
$ sudo reboot
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo reboot

sudo rpi-update
sudo reboot

sudo apt-get install -y alsa-utils mpg123 lame
sudo apt-get install -y mpd mpc
sudo nano /etc/mpd.conf
- comment out bind "localhost"

sudo reboot
 
mpc add http://live-icy.gss.dr.dk/A/A21H.mp3
mpc play
 -- radio sound emerges and fills the room with joy from "DR P7 Mix"
mpc stop

sudo apt-get install -y python-rpi.gpio

nano radio.py
    TO DO
´´´
To start playing when booting up just add this lione just before the last line "exit 0"
´´´
$ sudo nano /etc/rc.local
	su -c "python /home/pi/radio.py &"
´´´	
DONE
