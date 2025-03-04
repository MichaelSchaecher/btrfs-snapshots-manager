<div align=center>
  <h1>BTRFS Snapshots Manager</h1>
    <p>Simple BTRFS snapshots manager made for Ubuntu, but works on any Linux distribution.</p>
</div>

## Introduction

**BTRFS Snapshots Manager** is simple way to manage BTRFS snapshots on systems that use BTRFS as root filesystem and none [Ubuntu](https://ubuntu.com) subvolume layout.

## Features

- Create snapshots on a daily basis using Systemd timers.
- Delete old snapshots to keep the disk usage under control.
- Easy to install and configure.

## Installation

### Using DPKG/APT

You can install the project using the following command:

```bash
wget -c https://github.com/MichaelSchaecher/btrfs-snapshots-manager/releases/download/1.24.07-81/btrfs-snapshots-manager_1.24.07-81_all.deb

sudo dpkg -i btrfs-snapshots-manager_1.24.07-81_all.deb
```

### From Source

Building and installing the project is straightforward. Follow these steps:

1. Clone the repository:

```bash
git clone https://github.com/MichaelMure/btrfs-snapshots-manager.git
```

2. Build the project:

```bash
cd btrfs-snapshots-manager
make build
```

3. Install the project:

```bash
sudo make install
```

## Usage

**BTRFS Snapshots Manager** is setup as a Systemd service and apt hook to create snapshots and delete old snapshots. The service is enabled by default and will create snapshots on a daily basis. You can also manually create snapshots by running the following command:

```bash
sudo btrfs-snapshots-manager
```

Once everything is set up and running you can rest assured that your well be able to restore your system to a previous state in case of a failure.

## Configuration

The configuration file is located at `/etc/btrfs-snapshots-manager.conf`. You can change the default values to fit your needs before installing the project.
