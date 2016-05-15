# Raspberry-Pi-Internet-Radio
Boot standard Raspbian image
expand filesystem
sudo reboot
sudo nano /etc/wpa-supplicant/wpa-supplicant.conf
 - add network info
	network={
		ssid="media43foder27donor"
		psk ="secret_key"
	}
sudo reboot
sudo apt-get update
sudo apt-get upgrade
sudo reboot
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
--------------------------
 - TO DO
--------------------------

sudo nano /etc/rc.local
	- add this lione just before the last line "exit 0"
	su -c "python /home/pi/radio.py &"
