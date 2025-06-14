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

# Step 9: Start the Node
kingpeped

# Optional: Verify Block Count and Status
kingpepe-cli getblockcount
kingpepe-cli getblockchaininfo

