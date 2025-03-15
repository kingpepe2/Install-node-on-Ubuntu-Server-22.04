Install a node for your coin on Ubuntu Server 22.04 with the following tutorial.

Update your Ubuntu server with the following command:

sudo apt-get update && sudo apt-get upgrade -y

Download the Linux daemon for your wallet with the following command:

wget "https://dl.walletbuilders.com/download?customer=b99a53a3f81f1bbb2049773ab7e188c73b503cc19256b64eb5&filename=kingpepe-daemon-linux.tar.gz" -O kingpepe-daemon-linux.tar.gz

Extract the tar file with the following command:

tar -xzvf kingpepe-daemon-linux.tar.gz

Download the Linux tools for your wallet with the following command:

wget "https://dl.walletbuilders.com/download?customer=b99a53a3f81f1bbb2049773ab7e188c73b503cc19256b64eb5&filename=kingpepe-qt-linux.tar.gz" -O kingpepe-qt-linux.tar.gz

Extract the tar file with the following command:

tar -xzvf kingpepe-qt-linux.tar.gz

Type the following command to install the daemon and tools for your wallet:

sudo mv kingpeped kingpepe-cli kingpepe-tx /usr/bin/

Create the data directory for your coin with the following command:

mkdir $HOME/.kingpepe

Open nano.

nano $HOME/.kingpepe/kingpepe.conf -t

Paste the following into nano.

addnode=kpepesolo.pool.sexy:21053

addnode=kpepe.pool.sexy:11053


Save the file with the keyboard shortcut ctrl + x.

Type the following command to start your node:

kingpeped
