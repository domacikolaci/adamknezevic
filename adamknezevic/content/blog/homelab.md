---
title: "Homelab"
date: 2023-02-09T23:56:29+11:00
draft: true
---

## So, you want the joys of being a sysadmin at home to huh?

After finishing a day of hard work being the best sys admin you can at work, who would want nothing more then doing it all over again at home! :)

Cynicism aside, labbing at home can be very fun and rewarding, both for improving life at home with additional services in your life (be it Jellyfin to centralise all your home media, or HomeAssistant helping bridge the gaps that come with IoT devices), as well as also to learn and develop your skills as an IT professional.

Feel like stepping foot into Linux tonight? Cool! Make a new VM with Ubuntu Server and get going!

Want to try your hand at SIEM? Sweet! Spin up a Wazuh instance and lets get started pushing agents out onto all your endpoints at home!

# My homelab

Currently, my homelab is very simple. Its just a single server running TrueNAS Scale bluefin. This server is responsible for all my NAS storage as well as docker containers in my network. This also serves as my TailScale gateway into the home network for remote access via my TailNet.

The server itself is a old Cisco C220 M4. I have 3x 12TB drives in it with the ZFS equivilent of RAID5 and a 1TB SAS HPE disk for the TrueNAS OS itself. Also upgraded the server with a real mix match of RAM to bring it to a total of 32GB (have had alot of issues getting it past 32GB...)

Main docker containers I have in my network would be TailScale for remote access via my TailNet, Jellyfin for all of my media managment/access needs and code-server so I can have VSCode in a web browser for my iPad as well as so I can work on the same thing on multiple devices for any light code projects I am working on.

I have found this to work well enough for the day to day needs of myself plus the home. I have tried to use Home Assistant via Docker also but have found the limitations to tricky to work with and instead am looking to just make a dedicated VM for this sometime in the future, or buy a Raspberry Pi for this (once those things become avalible again)

Apart from the above, I do also have a old HPE and Dell server kicker around both with reasonble specs for a ESXi lab, however, these only ever get turned on for when my labbing needs require it and mainly just get scrapped for parts for the Cisco or collect dust sadly. Power bills unfortunetly stopping me from running a 24/7 mini DC in my garage + the noise dosnt help with any approval from the missess ;)

# Guides

# Tips

If you are every considering TrueNAS for your NAS needs, I strongly recommend running it in a VM. If I could go back, that server would be running in ESXi or Hyper-V or Proxmox (depending how I felt in the moment, but most likely the free version of ESXi) and been virtualised. I find that the VM capabilies of Scale to be to unreliable despite just being a pretty UI for QEMU, so any VM work I could have done on this server is now out the window. As this is the case, I am stuck with either Docker containers or instead, having to use another device for VM work such as my local PC or another one of the servers.