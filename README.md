# openvpn_bash_wrapper
A simple wrapper script for openvpn.

##What do I need to make this script work?

1. Openvpn installed
2. .ovpn files for whichever vpn you use


##How to install manually

###1. Download this repository
###2. Unzip the archive
###3. Create a new folder to your home 

	```
	mkdir ~/bin
	```
###4. Mv the vpn script to newly created bin
###5. Add your bin folder to path by editing .bashrc and adding the following line

	```
	PATH=~/bin:$PATH
	```

###6. Log out and back in for the changes to take effect or if you feel adventurous:

	Run the same line in terminal so you don't have to log out and back in for the changes to take effect
	```
	export PATH=~/bin:$PATH
	```
###7. Create configuration folder

	```
	mkdir ~/.config/openvpn
	```

###8. Move or copy all the .ovpn files to created config folder

Note that the script goes through the openvpn config folder and lists all the files and their full file names as potential vpn connections. As such possible connection listing could be:

	1) Quit
	2) a.ovpn
	3) b.ovpn
	4) something.ovpn

This can get cumbersome so I personally rename all the config files omitting .ovpn extension.  Linux doesn't case about file extensions anyways.

###9. Open the script in text editor: 

	replace the `USERNAME` variable with your own username
	
	OR

	Replace 'CONFIGROOT` with path to whichever folder you stashed your .ovpn files 


## How to use

The script can be used in two ways:

###1. Run the script
	sudo vpn

And choose where to connnect

###2. Run the script with path to .ovpn

	sudo vpn /etc/openvpn/blah.ovpn