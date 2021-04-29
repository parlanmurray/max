#!/bin/bash

# requires sshpass
# apt-get install sshpass

# requires setting up ssh key authentication with the pi

# assign variables
declare -A pi_list

# pi names can be according to location
pi_list['<device_name>']='<device_ip>'

while getopts h flag
do
	case "${flag}" in
		h)
			echo "./pi_ssh.sh <device_name>"
			exit 1
			;;
	esac
done

if [[ $!pi_list[$1] ]]; then
	ssh "pi@${pi_list[$1]}"
fi
