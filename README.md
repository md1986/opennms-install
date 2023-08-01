# OpenNMS Install

This script is a convenient bootstrap script to install OpenNMS on Debian or CentOS systems.
The script executes the steps documented in [Installation and Configuration guide](https://docs.opennms.com/horizon/latest/deployment/core/getting-started.html).

The script is tested with:

* Ubuntu 22.04.2 (Jammy) AMD64
* Debian 12 (Bookworm) AMD64
* Rocky Linux 9 AMD64
* AlmaLinux 8/9 AMD64

[![asciicast](https://asciinema.org/a/dCzY67dR6Ph07X2XLEdoGe9FC.svg)](https://asciinema.org/a/dCzY67dR6Ph07X2XLEdoGe9FC)

## Usage

Download the script to your system.

Execute on a CentOS based system
```bash
sudo bash bootstrap-yum.sh
```

Execute on Debian-based system
```bash
sudo bash bootstrap-debian.sh
```

## Installing other releases

It is possible to install different releases of OpenNMS.
The script can set a parameter `-r` which overwrites the default release name `stable`.

Example installing snapshot on Ubuntu
```bash
sudo bash bootstrap-debian.sh -r snapshot
```

## Install from different package mirror

If you want to install from a different package mirror, you can overwrite the default `{yum,debian}.mirrors.opennms.org` with your own server.

Example installing from OpenNMS server from your own server
```bash
sudo bash bootstrap-debian.sh -m your-server-fqdn
```