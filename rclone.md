# Working with Rclone and OSN
[Rclone](https://rclone.org/) is a CLI program to manage files on cloud storage. 
It's similar to rsync but provides many additional features including support for over 
(40 cloud storage products)[https://rclone.org/#providers].

## Install Rclone
### macOS installation
#### Install Rclone via Homebrew

[Homebrew](https://brew.sh/) is a 3rd party package manager for macOS that can be used 
to easily install many FOSS packages. To install Homebrew, please see the documentation
on their [website](https://brew.sh) or simply run the following command:

```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Homebrew is installed, install rclone by running the following command:
```
$ brew install rclone
```

#### Install Rclone without Homebrew
Alterantively, you can install rclone for macOS by running the rclone-provided install.sh 
script which will download the relevant precompiled binary.

```
$ sudo -v ; curl https://rclone.org/install.sh | sudo bash
```

### Linux installation

 

