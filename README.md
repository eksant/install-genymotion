# Install Genymotion

## Prerequisites
### Install Virtualbox
Download : https://www.virtualbox.org/wiki/Downloads

### Install GCC 4.9
This is not mentioned in the official documentation, but your Ubuntu server will need the basic development toolchain and gcc 4.9 installed in order to install Genymotion.
```bash
$ sudo add-apt-repository ppa:ubuntu-toolchain-r/test
$ sudo apt-get update
$ sudo apt-get install gcc-4.9 g++-4.9 -y
```
Also in order to avoid an error where ‘CXXABI_x.y.z’ is not found when running the installer, issue the following commands.
```bash
$ LD_LIBRARY_PATH=/usr/local/lib64/:$LD_LIBRARY_PATH
$ export LD_LIBRARY_PATH
```

### Install Genymotion
Although Genymotion is free for personal use, you will need to create an account in order to download the software.  Go to https://www.genymotion.com, and click on “Sign In” at the top.  This will take you to a sign in form, where you can press the “Create an account” button.
You can download the binaries.  The free “personal use only” version can be found by selecting: “Resources” > “Fun Zone” from the top menu or going directly to https://www.genymotion.com/fun-zone/ and clicking on the “Download” button.

Now we can run the installation from the download directory:
```bash
$ chmod u+x genymotion-2.10.0-linux_x64.bin
$ ./genymotion-2.10.0-linux_x64.bin
```
And the output will look something like this:
```bash
Installing for current user only. To install for all users, restart this installer as root.

Installing to folder [/home/fabian/Downloads/genymotion]. Are you sure [y/n] ?

- Trying to find VirtualBox toolset .................... OK (Valid version of VirtualBox found: 5.1.18r114002)
 - Extracting files ..................................... OK (Extract into: [/home/fabian/Downloads/genymotion])
 - Installing launcher icon ............................. OK

Installation done successfully.

You can now use these tools from [/home/fabian/Downloads/genymotion]:
 - genymotion
 - genymotion-shell
 - gmtool
```

Run Genmotion for the first time
```bash
$ cd genymotion
$ ./genymotion
```

