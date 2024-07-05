# Iagon Compute CLI

Iagon Compute Node CLI is a CLI application which allows users to share their computational power on the Iagon network to earn rewards.

## Introduction

This document provides step-by-step instructions to help you install and set up Iagon Compute Node CLI on your system. Currently only Linux based OS (Ubuntu 22.04) is supported.

## Installation

You can install the Official Compute Node CLI binary by using our install.sh script, which you can get from [Iagon's Github Release page](https://github.com/Iagonorg/Mainnet-Compute-Node/releases).

```bash
wget -qO- https://github.com/Iagonorg/Mainnet-Compute-Node/releases/download/v0.2.0-beta/install.sh | sudo bash
```

The script installs and configures necessary 3rd party trusted packages as dependencies, which includes:

- fio, sysbench (for benchmarking)
- nginx (for reverse proxy)
- kvm and libvirt (for resource isolation through virtual machine)

## Update from previous versions

You can update your compute node binary to latest version by using our update.sh script, which you can get from [Iagon's Github Release page](https://github.com/Iagonorg/Mainnet-Compute-Node/releases).

```bash
wget -qO- https://github.com/Iagonorg/Mainnet-Compute-Node/releases/download/v0.2.0-beta/update.sh | sudo bash
```

### Prerequisites

Before installing the Compute Node CLI, ensure the following prerequisites are met:

#### virtualization support

Enable kvm virtualization support on your bios. Consult your device manufacturer documentation.

#### port forwarding

Enable port forwarding for the compute node binary on a static ip. The port 443 should be accessible from the internet.

## Usage

Once the binary and the necessary dependencies are installed, you can use the Compute Node CLI. There are various commands available in the CLI to make the on-boarding/registration process easier. The user can start the node and execute various test commands to check the hardware status of the node.

### Commands

Execute the following commands, as: `iag-compute-cli some-command`

1. **start**

   Evaluate/Register the host machine as compute node or start compute node if already evaluated.

2. **stop**

   Stop compute node (if already running)

3. **status**

   Check running status of compute node

4. **check**

   Check if the system adhere to prerequisite criteria

5. **info**

   Extract basic information about the system

6. **test-node**

   Test if the node is accessible from the internet

7. **clear-config**

   Clear the configurations

8. **tasks**

   Show the compute tasks running on the node.

9. **benchmark-memory**

   Run memory tests and benchmark for the host machine

10. **benchmark-cpu**

    Run cpu tests and benchmark for the host machine

11. **benchmark-storage**

    Run storage i/o tests and benchmark for the host machine

12. **benchmark-network**

    Run network tests and benchmark for the host machine

13. **help**

    Display help for command
