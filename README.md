# Energi GEN3 Masternode Setup Guide<br />


#### This is a simple guide to show you step by step how to setup your GEN3 Energi / NRG Masternode.

### WARNINGS (please read!):
- NEVER download files except from the [Energi Wiki](https://docs.energi.software/) `https://docs.energi.software/` unless at your own risk!<br />
- NEVER let anyone install your Masternode for you! This guide will help you :)<br />
- NEVER let anyone access your Masternode with ANY remote access tools (ssh, ftp, TeamViewer, etc.)<br /><br />
- I will NEVER direct message you unless you message me first. You can find `MooCat ( pool.easyx.cc ) #4182 UID: 409032031713099788` on this Discord server: [https://discord.gg/pUUJKYB](https://discord.gg/pUUJKYB) <br /><br />
- Only send your assets to the [Energi Nexus](https://nexus.energi.network/). Make sure the URL is correct `https://nexus.energi.network/` and the SSL certificate is valid. If you are using this guide, you are responsible for your assets and where you send them. As a courtousey we will remind you of this again.<br /><br />

__Throughout this guide__ you will find referral links, all that I ask is that you use them to support my work. Should you modify these instructions that you keep the referral links there - unless your new instructions use another service not already referred. I also ask that you leave these warnings and notices here. 

__Anyone who forks this repository without leaving these notices here is trying to scam you!__

#### ~ LeshaCat

---
### Table of Contents:
- [Referral Links](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#an-overview-of-referral-links) - An overview of referral links
1. [Step 1](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-1-deploy-a-vps-instance) - Deploy a VPS instance
2. [Step 2](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-2-connect-to-your-vps-and-complete-basic-setup) - Connect to your VPS and complete basic setup
3. [Step 3](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-3-install-and-run-energi-masternode-install-script) - Install and run Energi Masternode Install script
4. [Step 4](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#step-4-obtain--deposit-your-collateral-for-the-masternode) - Obtain & Deposit your collateral for the Masternode
- [Optional](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#optional-steps-to-complete) - Optional steps to complete
- [Troubleshooting](https://github.com/EasyX-Community/Energi-Masternode-Setup-Guide/blob/master/README.md#troubleshooting-any-issues) - Troubleshooting any issues

---
### An overview of referral links
##### Used within this tutorial:
- Vultr - Get $100 USD free for the first month! [https://www.vultr.com/?ref=8543730-6G](https://www.vultr.com/?ref=8543730-6G)
- Kucoin - A great exchange to buy Energi / NRG [https://www.kucoin.com/ucenter/signup?rcode=24g7KdH](https://www.kucoin.com/ucenter/signup?rcode=24g7KdH)

##### NOT used within this tutorial (pls support!):
- Brave Browser - Surf the internet, block ads, earn crypto, and keep your privacy. [https://brave.com/les666](https://brave.com/les666)
- Lbry - Get paid crypto to post videos. [https://lbry.tv/$/invite/@leshacat:7](https://lbry.tv/$/invite/@leshacat:7)

---
### Step 1: Deploy a VPS instance
<br />

---
### Step 2: Connect to your VPS and complete basic setup
<br />

---
### Step 3: Install and run Energi Masternode Install script
<br />

---
### Step 4: Obtain & Deposit your collateral for the Masternode
<br />

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

### Conclusion <br />

I hope you've found this setup guide useful! 

If you have any issues You can find `MooCat ( pool.easyx.cc ) #4182 UID: 409032031713099788` on this Discord server: [https://discord.gg/pUUJKYB](https://discord.gg/pUUJKYB)

Issue tickets can also be submitted for help. Do NOT send sensitive information over Discord OR support tickets!

Good Day :)
<br >
<br >

__EOF__
<br >
<br >
