+++
weight = "1"
title = "The Vector Packet Processor (VPP)"
summary = "VPP is the core technology behind the FD.io project."

btntxt="More About Installing VPP "
####btnurl="/docs/vpp/master/gettingstarted/installing"

# The first part of these strings are displayed in the dropdown.
# The second is the url
latest = "Latest Release (2005), /docs/vpp/v2005/gettingstarted/installing"
versions = ["Master, /docs/vpp/master/gettingstarted/installing",
	 "Version 20.05, /docs/vpp/v2005/gettingstarted/installing",
	 "Version 20.01, /docs/vpp/v2001/gettingstarted/installing"]

+++

## How to Install VPP

The following describes how to install VPP on Ubuntu 18.04. For a complete
set of instructions click on the button at the bottom of the page.

### Update the OS

It is a good idea to first update and upgrade the OS before starting; run the
following command to update the OS:

``` console
$ sudo bash
# apt-get update
```

### Point to the Repository

Create a file **/etc/apt/sources.list.d/99fd.io.list** with contents that point to
the version needed. In this example we point to the latest release.

``` console
deb [trusted=yes] https://packagecloud.io/fdio/release/ubuntu bionic main
```

### Get the key:

``` console
# curl -L https://packagecloud.io/fdio/release/gpgkey | sudo apt-key add -
```

### Install the Mandatory Packages

Install the mandatory packages by running the following commands:

``` console
# sudo apt-get update
# sudo apt-get install vpp vpp-plugin-core vpp-plugin-dpdk
```
  
### Install the Optional Packages

Install the optional packages by running the following command:

``` console
# sudo apt-get install vpp-api-python python3-vpp-api vpp-dbg vpp-dev
```

### Uninstall the Packages

Uninstall the  packages by running the following command:

``` console
# sudo apt-get remove --purge vpp*
```
