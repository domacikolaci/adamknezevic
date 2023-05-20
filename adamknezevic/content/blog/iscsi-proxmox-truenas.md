---
title: "Iscsi Proxmox Truenas"
date: 2023-05-18T23:49:24+10:00
draft: true
---
## Intro

Just finished setting this up myself and struggled to find any decent, up to date instructions on setting up a Proxmox server connecting to a TrueNAS Scale server using iSCSI, so, I decided to make my own damn guide!

I am using TrueNAS Scale for this guide but this should be technically no different for Core. Also, the steps for the Proxmox side would technically apply to other iSCSI targets (Synology, QNAP, etc) althoguh I havnt tested it, so by all means go for it and see what happens :)

## TrueNAS

First, lets start on the TrueNAS side.