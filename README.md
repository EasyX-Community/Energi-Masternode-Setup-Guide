# Energi GEN3 Masternode Setup Guide<br />


#### This is a simple guide to show you step by step how to setup your GEN3 Energi / NRG Masternode.

### WARNINGS (please read!):
- NEVER let anyone install your Masternode for you! This guide will help you :)<br />
- NEVER download files except from the [Energi Wiki](https://docs.energi.software/) `https://docs.energi.software/` unless at your own risk!<br />
- NEVER let anyone access your Masternode with ANY remote access tools (ssh, ftp, TeamViewer, etc.)<br /><br />
- I will NEVER direct message you unless you message me first. You can find `MooCat ( pool.easyx.cc ) #4182 UID: 409032031713099788` on this Discord server: [https://discord.gg/pUUJKYB](https://discord.gg/pUUJKYB) <br /><br />
- Only send your assets to the [Energi Nexus](https://nexus.energi.network/). Make sure the URL is correct `https://nexus.energi.network/` and the SSL certificate is valid. If you are using this guide, you are responsible for your assets and where you send them. As a courtousey we will remind you of this again.<br /><br />

__Throughout this guide__ you will find referral links, all that I ask is that you use them to support my work. Should you modify these instructions that you keep the referral links there - unless your new instructions use another service not already referred. I also ask that you leave these warnings and notices here. You can press and hold CTRL while clicking these links to open them in a new tab.

__Anyone who forks this repository without leaving these notices here is trying to scam you!__

#### ~ LeshaCat

---
### Table of Contents:
- [Referral Links](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#an-overview-of-referral-links) - An overview of referral links<br />
[Step 1](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-1-deploy-a-vps-instance) - Deploy a VPS instance<br />
[Step 2](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-2-connect-to-your-vps-and-complete-basic-setup) - Connect to your VPS and complete basic setup<br />
[Step 3](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-3-install-and-run-energi-masternode-install-script) - Install and run Energi Masternode Install script<br />
[Step 4](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-4-obtain--deposit-your-collateral-for-the-masternode) - Obtain & Deposit your collateral for the Masternode<br />
- [Optional](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#optional-steps-to-complete) - Optional steps to complete<br />
- [Troubleshooting](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#troubleshooting-any-issues) - Troubleshooting any issues<br />
- [Conclusion](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#conclusion) - Concluson and contact information<br />

---
### An overview of referral links
##### Used within this tutorial:
- Vultr - Get $100 USD free for the first month! [https://www.vultr.com/?ref=8543730-6G](https://www.vultr.com/?ref=8543730-6G)
- Kucoin - A great exchange to buy Energi / NRG [https://www.kucoin.com/ucenter/signup?rcode=24g7KdH](https://www.kucoin.com/ucenter/signup?rcode=24g7KdH)

##### NOT used within this tutorial (pls support!):
- Lbry - Get paid crypto to post videos. [https://lbry.tv/$/invite/@leshacat:7](https://lbry.tv/$/invite/@leshacat:7)
- Brave Browser - Surf the internet, block ads, earn crypto, and keep your privacy. [https://brave.com/les666](https://brave.com/les666)
- CoinSwitch - Swap between cryptos with multiple exchanges. [https://coinswitch.co/?ref=6P01FNXZR1](https://coinswitch.co/?ref=6P01FNXZR1)

---
### Step 1: Deploy a VPS instance
- visit [https://www.vultr.com/?ref=8543730-6G](https://www.vultr.com/?ref=8543730-6G) and sign up. Your account will be auto credited for $100 which expires at the end of the month (basically 1 month free) - Ensure it has the following requirements:
``` 
Operating System	Ubuntu 18.04 x64	Ubuntu 18.04 x64

Hardware	  Minimum	  Recommended
CPU (Core)	  1 x 1 GHz	  2 x 2 GHz
RAM (Memory)	  2 GB	          4 GB
Storage	          30 GB	          30 GB
SWAP	          2 GB	          0 GB
```

---
### Step 2: Connect to your VPS and complete basic setup
-  run `ssh root@192.168.1.15` (replace root username and IP) to ssh to your system
-  run `sudo passwd ;` to change your root password
-  run `sudo apt update ; sudo apt upgrade -y ; sudo apt dist-upgrade -y ;` to update your system
-  run `sudo apt install -y htop git logrotate net-tools psmisc;` to install requirements
-  [set up 2fa](https://www.vultr.com/docs/using-two-factor-authentication-to-login-to-vultr-control-panel) on your Vultr account
-  [set up swap space](https://www.vultr.com/docs/setup-swap-file-on-linux) on your Vultr node

---
### Step 3: Install and run Energi Masternode Install script

- run `bash -ic "$(wget -4qO- -o- raw.githubusercontent.com/energicryptocurrency/energi3-provisioning/master/scripts/linux/energi3-linux-installer.sh)" ; source ~/.bashrc` to download and run the installer script
- enter root password if asked
- press enter on main screen
- copy down the username + password for user `nrgstaker`
- press `y` and press enter to confirm you've copied the information
- press `a` and press enter to select `new install`
- enter `y` or `n` to enable 2fa
  - download [Google Authenticator](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_us) app
  - scan the QR code shown on screen
  - write down the backup codes
  - enter `y` to accept current 2fa codes
- energi core node will now download and install
- enter `y` to download your keystore file to the VPS
  - upload your keystore file from your wallet to [Firefox Send](https://send.firefox.com/)
  - copy the URL to your keystore file, paste it into the console window and press enter
- your node is now set up and will be ready after downloading the blockchain

---
### Step 4: Obtain & Deposit your collateral for the Masternode
- download and install Energi wallet on another computer (not on the VPS) from [https://docs.energi.software/en/downloads/myenergiwallet](https://docs.energi.software/en/downloads/myenergiwallet)
  - install and open the wallet
  - click on `Create New Wallet` and then click `generate wallet`
  - follow instructions and copy your backup codes and save them in safe place
  - copy your Energi wallet receiving address
- visit [https://www.kucoin.com/ucenter/signup?rcode=24g7KdH](https://www.kucoin.com/ucenter/signup?rcode=24g7KdH) and sign up
  - log in to your Kucoin account
  - hover on your account name in the top right
  - click on `deposit`
  - click the dropdown and select your currency to deposit
  - copy the address, send the deposit to the address
  - wait for confirmations
  - trade the asset for BTC or ETH if it is not already
  - click `markets` in the top left
  - enter your trading password
  - type in `NRG` and select either `BTC-NRG` or `ETH-NRG` pair
  - click on the link `transfer` in the buy order form to transfer your BTC/ETH to your trading account
  - either place a limit order or select `market` and place an order
  - you need to buy 1000 NRG increments to run a masternode
  - click on the link `transfer` on the sell order form to transfer your NRG to your main account
  - hover over your name in the top right
  - click on withdraw
  - copy your Energi wallet receiving address from above
  - enter the amount, press send, and enter your trading password
- once received it will take about 1 hour for the funds to be added to your `staking balance`
- now you are ready to deposit your Masternode collateral
  - visit the [Energi Nexus](https://nexus.energi.network/). Make sure the URL is correct `https://nexus.energi.network/` and the SSL certificate is valid. If you are using this guide, you are responsible for your assets and where you send them
  - click on `Masternodes`
  - you can enter your Energi wallet receiving address to check the status of your node
  - click on `Collateral` on the left side menu
  - enter your Energi wallet receiving address and click on `Deposit Collateral` - if it is greyed out you do not have enough NRG (need 1000)
  - login using your keystore file
  - fill out the pre-filled form to send your collateral and click send
  - wait for the transaction to confirm
  - once you've received your MNRG Masternode collateral you can now announce your node
- now you are ready to announce your Masternode
  - visit the [Energi Nexus](https://nexus.energi.network/). Make sure the URL is correct `https://nexus.energi.network/` and the SSL certificate is valid. If you are using this guide, you are responsible for your assets and where you send them
  - click on `Masternodes`
  - you can enter your Energi wallet receiving address to check the status of your node
  - click on `Operations` on the left side menu
  - click on `Announce Masternode`
  - login using your keystore file
  - fill out the pre-filled form to announce your masternode and click send
  - wait for the transaction to confirm
  - click on `Collateral` on the left side menu
  - enter your Energi wallet receiving address
  - watch your node status and balances on this page

---
### Optional steps to complete
<br />

---
### Troubleshooting any issues

##### Trouble: Signature errors during APT update/upgrade
Example:
```
[ubuntu@server ~]$ sudo apt-get update
Ign http://security.ubuntu.com trusty-security InRelease
Get:1 http://security.ubuntu.com trusty-security Release.gpg [933 B]
...
Fetched 21.9 MB in 14s (1,537 kB/s)
Reading package lists... Done
W: GPG error: http://security.ubuntu.com trusty-security Release: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 40976EAF437D05B5 NO_PUBKEY 3B4FE6ACC0B21F32
W: GPG error: http://archive.canonical.com trusty Release: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 40976EAF437D05B5 NO_PUBKEY 3B4FE6ACC0B21F32
W: GPG error: http://archive.ubuntu.com trusty Release: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 40976EAF437D05B5 NO_PUBKEY 3B4FE6ACC0B21F32
W: GPG error: http://archive.ubuntu.com trusty-updates Release: The following signatures couldn't be verified because the public key is not available: NO_PUBKEY 40976EAF437D05B5 NO_PUBKEY 3B4FE6ACC0B21F32
[ubuntu@server ~]$ 
```
__Solution:__<br />

Run the following command and replace SIGNATURE with the signature missing the PUBKEY from above:
```
[ubuntu@server ~]$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys SIGNATURE
```
Example:
```
[ubuntu@server ~]$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 3B4FE6ACC0B21F32
```
<br />

---

### Conclusion<br />

I hope you've found this setup guide useful! 

If you have any issues You can find `MooCat ( pool.easyx.cc ) #4182 UID: 409032031713099788` on this Discord server: [https://discord.gg/pUUJKYB](https://discord.gg/pUUJKYB)

Issue tickets can also be submitted for help. Do NOT send sensitive information over Discord OR support tickets!

Good Day :)
<br >
<br >

__EOF__
<br >
<br >
