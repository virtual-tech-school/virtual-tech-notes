# Context

Linux is the most widely used Operating System by software engineers. Most of us still prefer Windows for our day to day tasks, and dual booting can be tricky. There are a few ways in which you can still use Linux without letting go of Windows or go through the hassle of dual booting.

## WSL (Windows Subsystem Linux)

It can be that your system is not powerful enough to run a virtual machine, but you still want to get started with Linux.

WSL is a lightweight Linux subsystem that can help you in that scenario.

WSL command is available by default. You can simply run the following command in your command prompt (CMD) to check the distributions available to install -

`wsl --list --online`

This displays 2 columns -

1. The name of the distribution.
2. Friendly name for it.

You can then simply run -

`wsl --install -d <distro>`
