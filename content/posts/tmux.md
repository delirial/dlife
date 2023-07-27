---
title: "Tmux"
date: 2023-07-17T23:54:37+02:00
description: 'As soon as Winston had dealt with each of the messages, he clipped his speakwritten corrections to the appropriate copy of the Times and pushed them into the pneumatic tube. '
image: images/cctv.jpeg
draft: true
---
The terminal multiplexer that allow to use multiple windows, panes and commands in terminal,providing a lightweigth enviroment to develop, read or modify code and configuration files.

The tool rewrite your way of thinking on terminal, so we need to embrace that to aprecciate the simplicity offer by **tmux**.

## [TPM](https://github.com/tmux-plugins/tpm)

Only tmux is, surely, not enough for your day to day work. But some devs come to the rescue with **tpm** package. This piece of software work with the concept of *package manager* in **tmux** itself!. This is great for devs that based work on the multiplexer because allow to customise aspect, functionality and behavior of **tmux**. 
## [Tmuxinator](https://github.com/tmuxinator/tmuxinator)

Tmux allow us to manage some workspaces with shell scripts. But manage two or three scripts is not kind, but is manageable; manage more is not. The solution provide by **tmuxinator** is define workspace on *yaml* format. Like a system master, you can create and reuse workspace with a declarative way of thinking. You can use some tricks to elaborate it, but simply enough and a lot of scales better than manage shell scripts. 

For example, to write this blog, normally i use little screens. This force me to use a screen split in two windows, the editor and the visualizer, tmux and firefox. My terminal is based on **alacritty**, **nvim** and **tmux** manage by **tmuxinator**. I can resume this with the follow configuration:
```yaml
root: ~/code/blog
window:
  editor: 
    layout: 
    - nvim content/posts
    - hugo serve -D
```
