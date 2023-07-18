---
title: "Virtualbox"
date: 2023-07-18T09:16:49+02:00
draft: true
---
NixOS is a linux base system with a special package manager. That manager is write in **Nix**.

## Nix
Nix is a functional language with the main purpose of build software. Like any other functional language, *immutability* and *pure functions* are part of the keys. In a context like building software, the idea is an ambitious one. Hide all tweaks and tricks of configuration, prerequisites and setup in favor of a declaration way of describe software. You can see that ~tema~ naturally progress to simplification.

system > package > program

