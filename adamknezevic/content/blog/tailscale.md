---
title: "Tailscale"
date: 2023-02-09T21:56:00+11:00
draft: true
---

## Exposing ports suck, even in the home lab

Opening ports on your firewall sucks big time. Even if all your opening is a port for your VPN, your *still* opening up a potential attack vector for a would be hacker scrolling through Shodan to find an open hole in your security to poke and prod at until they get in. Not ideal.

**BUTTTTT**, you still need services behind your firewall open to the internet for you to access. Be it your file server, your Jellyfin running on your home lab or your big fancy pants core application for your buisness. So... what do you do? You try an alternative type of VPN instead. Something that dosnt need an open port to the world, but instead, something that can pin hole through the gate way to a broker of sorts, and routes your traffic between your devices instead via this broker.

There are a few ways of going about this, but the best I have found for myself would be Tailscale. What I love the most about Tailscale was how.... easy it was. Account sign up was an OAuth connection with someone else, so I dont need to add another username/password combo into the password manager, registering endpoints is a painless experience and even just exploring the additional features of their DNS features and file sending was painless and very straight forward. Its now allowing me to no longer keep things like SSH open for a VPS I need access to, or worry about how I am supposed to access a Raspberry Pi I keep offsite somewhere since as long as the thing has internet access, I have access to the device via my TailNet(TailNet being the fancy name they give for your virtual network in Tailscale).