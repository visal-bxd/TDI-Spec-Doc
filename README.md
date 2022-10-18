# Introduction
Intel® P4 Studio Software Development Environment (SDE) is a set of packages for programming Intel’s line of programmable Ethernet Switches. The package also contains scripts for building and installing SDE. The fully automated script (install.sh) introduced in this release works in conjunction with the existing command line interface tool (p4studio) to ease the build and installation process. The following sections describe how to build and install the Intel P4 Studio SDE.

**Note**: SDE Release 9.5.0 and earlier uses p4studio_build.py CLI tool to build and install the SDE.
# Prerequisites
Supported OS: Refer to release-specific Release Notes for the list of supported OS.
Free Space: More than or equal to 20 GB
# Installation
**Note 1**: The installation method explained below is applicable for SDE Release 9.11.0 and later. 
**Note 2**: Refer to appropriate release-specific Installation guide for SDE Release 9.5.0 and earlier.
**Note 3**: Refer to Intel® P4 Studio Software Development Environment (SDE) Installation Guide for SDE Release 9.6.0 to 9.10.0.

1. Run the install.sh script at the top level of the SDE package (that is, at bf-sde-9.x.x level).
**Note**: The install.sh script initially evaluates system capabilities such as free space and OS support to build and install SDE.
2. Install default settings or user-defined settings based on your need.
## Install default setting:
**Note**: Default settings allow you to run P4-16 examples for all Tofino chip types on the ASIC model. This is more appropriate for a beginner as the entire build and installation will be taken care of by the script.

a)	Select Yes to start with default setting installation.
b)	Script validates   the following source packages:
* bridge
* libcli
* thrift
* grpc
c)	Script validates the following configuration options:
* tofino
* tofino2
* tofino2m
* tofino3
d)	Script validates the p4-16-programs.
e)	Script installs all the dependencies one after the other.

## Install user-defined setting:

**Note 1**: It is recommended to install user-defined settings by an experienced SDE user.

a)	Select No to start with user-defined setting installation.
b)	Select Yes to install missing third-party dependencies.
c)	Select an appropriate deployment target.
**Note**: The available targets are Hardware and ASIC Model. The following interactive questions varies based on the target selection. Here, we use ASIC Model to explain the concept. 
d)	Select the Tofino chip type.
**Note**: The available p4 architectures are tofino, tofino2, tofino2m, and tofino3.
e)	Select Yes to build kernel modules (bf_kdrv, bf_kpkt, bf_knet).
f)	Enter path to kernel headers directory or leave blank to autodetect.
g)	Select p4 programs and corresponding control plane cod  e.
**Note**: The supported options are P4 examples: P4-16, P4 examples: P4-14, switch-p4-16: x1_tofino, switch-p4-16: x2_tofino, switch-p4-16: x6_tofino, and bf-diags.
h)	Select Yes to configure advanced options. Advanced options include p4rt, TDI, and SAI configurations.
i)	The created profile details are displayed at this stage. Save the profile details in a YAML file for future use.  
3.	Script finally lets you log in to p4studio.  

