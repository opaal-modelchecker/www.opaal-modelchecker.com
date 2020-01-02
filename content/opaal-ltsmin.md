
---
title: "opaal + LTSmin"
date: 2020-01-02T11:23:51+01:00
draft: false
menu: "main"
weight: 5
---


# Setup Instructions

</div>

This guide is for installing opaal+LTSmin and have been tested on Ubuntu 12.04 and Ubuntu 14.04 but have also been confirmed to work on Arch Linux and Mac OS X - however you will have to identify the needed software packages yourself on those platforms. The installation of opaal+LTSmin is automated so users simply need to download and run a bash script. Besides installation on a PC, this method also support installing of opaal+LTSmin on multiuser system which, e.g., are typical used for application servers and compute clusters.

## Requirements:

Before installing please make sure that the nessecary software packages are already installed. We currently only support 64 bit versions of Ubuntu 12.04 and Ubuntu 14.04\.

### Ubuntu 12.04

For Ubuntu 12.04 the required software packages can be installed by:

<div class="indent">

> sudo apt-get install bzr build-essential libtool automake libc6-dev-i386 libboost-all-dev swig python2.7-ply ant flex libpopt-dev libtbb-dev python2.7-numpy

</div>

### Ubuntu 14.04

For Ubuntu 14.04 the required software packages can be installed by:

<div class="indent">

> sudo apt-get install bzr build-essential libtool automake libboost-all-dev swig python-ply ant flex libpopt-dev libtbb-dev python-numpy

</div>

### Installing opaal+LTSmin on an application server or cluster:

In order to install opaal+LTSmin on an application server or compute cluster the required software must be installed by the system administrator, so please consult your local system administrator to get those or similar packages installed before you run the script.  
For a cluster installation we recommend using the Enthought Python Distribution which also includes python2.7-numpy and python2.7-ply. Please see their installation instructions.

## Installation:

The following commands will install opaal+LTSmin in the subdirectory opaal-ltsmin in the users home-directory:  

        cd && mkdir opaal-ltsmin && cd opaal-ltsmin  

        wget [mcc.uppaal.org/opaal/install_opaal_ltsmin-1.0.15](http://mcc.uppaal.org/opaal/install_opaal_ltsmin-1.0.15)  

        bash install_opaal_ltsmin-1.0.15  

After the script is done it will print out information on how to run opaal+LTSmin.  

If you want to use a different version of one of the software components please feel free to modify the installation script as you see fit.  

## Problem installing:

If you get an error similar to this:

checking for gcc... gcc  
checking for C compiler default output file name...   
configure: error: in `/home/fmg/laarman/opaal-ltsmin/UPPAAL-dbm-2.0.8-opaal3/modules':  
configure: error: C compiler cannot create executables  
See `config.log' for more details.

please see: [stackoverflow.com/questions/6329887/compiling-problems-cannot-find-crt1-o](http://stackoverflow.com/questions/6329887/compiling-problems-cannot-find-crt1-o)

