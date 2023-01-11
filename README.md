# Apple-Silicon Pre-requisites

Follow this guide if using an Apple Silicon ARM chip (M1, M2, etc.)

## Homebrew

`Homebrew` is a free and open-source package manager for macOS. We will need it to install the virtualization software for this course.

Open the `Terminal` application, copy-paste the following, and hit `return`:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Read the information the script presents you, and then accept it to continue. 

Once `Homebrew` is installed, type `brew -v` in `Terminal`, hit `return`, and ensure you don't get any errors.

## Tart

`Tart` is a free and open-source virtualization toolset, which we will be using in this course for Apple silicon Macs. 

Installation is simple, just run the following in `Terminal` like we previously did to install `Homebrew`:

`brew install cirruslabs/cli/tart`

# VM Setup

## Ubuntu Server

Now we are ready to set up our Linux Virtual Machine! The Linux distribution of choice for this course is `Ubuntu`.

Since Apple silicon is ARM, we will be using the ARM version of `Ubuntu`. You can [download it here](https://ubuntu.com/download/server/arm). 
Make sure to download the **LTS** version!

Next up, we need to use `Tart` in order to set up the image we just downloaded. 

First, we need to navigate in the `Terminal` to the folder where this image just downloaded. In most cases this is your `Downloads` folder. Run the following command:

`cd Downloads` (you can replace `Downloads` with the name of another folder if necessary, e.g. `cd /Users/john/Documents/custom-folder`)

Next, we can create our Virtual Machine:

`tart create --linux ubuntu`
`tart run --disk ubuntu-22.04.1-live-server-arm64.iso ubuntu`

Our Virtual Machine is now running, with the Ubuntu installation disk inserted! Continue to the next guide to find out how to install it.

From here on out, you can start the Virtual Machine by simply running `tart run ubuntu` in `Terminal`.
