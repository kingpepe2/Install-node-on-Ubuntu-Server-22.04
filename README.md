Tutorial - Install node on Ubuntu Server 22.04
Install a node for your coin on Ubuntu Server 22.04 with the following tutorial.

Update your Ubuntu server with the following command:

sudo apt-get update && sudo apt-get upgrade -y

Download the Linux daemon for your wallet with the following command:

wget "https://dl.walletbuilders.com/download?customer=7fd7ad0365703844c530ed1b76f8838f9e81a832a1178f1a56&filename=kingpepe-daemon-linux.tar.gz" -O kingpepe-daemon-linux.tar.gz

Extract the tar file with the following command:

tar -xzvf kingpepe-daemon-linux.tar.gz

Download the Linux tools for your wallet with the following command:

wget "https://dl.walletbuilders.com/download?customer=7fd7ad0365703844c530ed1b76f8838f9e81a832a1178f1a56&filename=kingpepe-qt-linux.tar.gz" -O kingpepe-qt-linux.tar.gz

Extract the tar file with the following command:

tar -xzvf kingpepe-qt-linux.tar.gz

Type the following command to install the daemon and tools for your wallet:

sudo mv kingpeped kingpepe-cli kingpepe-tx /usr/bin/

Create the data directory for your coin with the following command:

mkdir $HOME/.kingpepe

Open nano.

nano $HOME/.kingpepe/kingpepe.conf -t

Paste the following into nano.

rpcuser=rpc_kingpepe

rpcpassword=dR2oBQ3K1zYMZQtJFZeAerhWxaJ5Lqeq9J2

rpcbind=127.0.0.1

rpcallowip=127.0.0.1

p2pport=24028

rpcport=24027

listen=1

server=1

txindex=1

daemon=1

addnode=node3.walletbuilders.com

Save the file with the keyboard shortcut ctrl + x.

Type the following command to start your node:

kingpeped




# Tutorial - Install KingPepe Node on Ubuntu Server 22.04

Install a node for your **KingPepe** coin on Ubuntu Server 22.04 by following these steps:

```bash
# Step 1: Update Your Server
sudo apt-get update && sudo apt-get upgrade -y

# Step 2: Download the Linux Daemon
wget "https://dl.walletbuilders.com/download?customer=7fd7ad0365703844c530ed1b76f8838f9e81a832a1178f1a56&filename=kingpepe-daemon-linux.tar.gz" -O kingpepe-daemon-linux.tar.gz

# Step 3: Extract the Daemon
tar -xzvf kingpepe-daemon-linux.tar.gz

# Step 4: Download the Linux Tools (QT, CLI, TX)
wget "https://dl.walletbuilders.com/download?customer=7fd7ad0365703844c530ed1b76f8838f9e81a832a1178f1a56&filename=kingpepe-qt-linux.tar.gz" -O kingpepe-qt-linux.tar.gz

# Step 5: Extract the Tools
tar -xzvf kingpepe-qt-linux.tar.gz

# Step 6: Move Daemon and Tools to /usr/bin
sudo mv kingpeped kingpepe-cli kingpepe-tx /usr/bin/

# Step 7: Create the Configuration Directory
mkdir $HOME/.kingpepe

# Step 8: Create and Edit Configuration File
nano $HOME/.kingpepe/kingpepe.conf -t

