# Working with Rclone and OSN
[Rclone](https://rclone.org/) is a CLI program to manage files on cloud storage. 
It's similar to rsync but provides many additional features including support for over 
[40 cloud storage products](https://rclone.org/#providers).

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
Alternatively, you can install rclone for macOS by running the rclone-provided install.sh 
script which will download the relevant precompiled binary.

```
$ sudo -v ; curl https://rclone.org/install.sh | sudo bash
```

### Linux installation

Installation of rclone for Linux can be done using your Linux distribution specific
package manager, or by using the rclone-provided binary installer.

Note, if you are on a system where you do not have administrative privledges, see the
last section of the Linux installation documentation on non-privledged installation.

#### Install Rclone using Linux package managers (requires root access)
For RedHat or RedHat clone distros:

```
$ sudo dnf install rclone
```

For Debian-based distros including Ubuntu:
```
$ sudo apt install rclone
```
 
For Arch-based distros:
```
$ sudo pacman -S rclone
```

#### Install Rclone binary directly (requires root access)
  Alternatively, you can install rclone for Linux by running the rclone-provided install.sh
  script which will download the relevant precompiled binary.
  
  ```
  $ sudo -v ; curl https://rclone.org/install.sh | sudo bash
  ```
 
#### Non-privledged installation of Rclone on Linux

If you are on an HPC system, first check to see if rclone is already installed.
For instance, if you are on a module-based system, you might search for the rclone module.
```
$ module spider rclone
```

If it is available, then you can `module load rclone` and then follow the rest of this
documentation.

If rclone is not available on your HPC system, you can install it into your $HOME
directory. First, fetch and unzip the precompiled rclone binary.

```
$ curl -O https://downloads.rclone.org/rclone-current-linux-amd64.zip
$ unzip rclone-current-linux-amd64.zip
$ cd rclone-*-linux-amd64
```
Place it in a directory that you have write access to and is in your $PATH.
If one is not available, you can create one.

```
$ mkdir $HOME/bin
$ cp rclone $HOME/bin
$ export PATH=$PATH:$HOME/bin
$ echo export PATH=\$PATH:$HOME/bin >> ~/.bashrc
```

*Note: The export and echo commands are for bash and other bourne-compatible shells.*

### Windows installation

For Windows installtion, download the correct binary for your system. 
If you are not sure, use the first download.
- [Intel/AMD - 64 Bit](https://downloads.rclone.org/rclone-current-linux-amd64.zip)
- [Intel/AMD - 32 Bit](https://downloads.rclone.org/rclone-current-linux-386.zip)
- [ARM - 64 Bit](https://downloads.rclone.org/rclone-current-linux-arm64.zip)

Once downloaded, open the file in Explorer and extract `rclone.exe`.
Rclone.exe is a portable binary and you can place it anywhere that is convenient
to call from CMD or powershell.


