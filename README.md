# Packer templates for Vagrant boxes

**Contents** [Overview] | [Getting started] | [Usage] | [Next steps] | [Contributing] | [Resources]  

## Overview

[Overview]: #overview

[Packer]: https://www.packer.io/
[Vagrant]: https://www.vagrantup.com/
[VirtualBox]: https://www.virtualbox.org/
[Hyper-V]: https://docs.microsoft.com/en-us/virtualization/
[Nested virtualization]: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/user-guide/nested-virtualization/
[Chef]: https://chef.io/chef/

### Operating systems

The following Vagrant boxes can be used for generic expirments on the respective platforms.

They contain the core operating system with the minimum configuration required to make Vagrant work, and some of the commonly used tools installed and options configured for easier provisioning. All the other Vagrant boxes below are based on these configurations as well.

- **Windows 10**
  - **[Enterpise][w10e]**
  - **[Enterpise with Docker for Windows Community Edition][w10e-docker-ce]**
- **Windows Server 2016**
  - **[Standard][w16s]**
  - **[Standard with Docker for Windows Community Edition][w16s-docker-ce]**
- **Linux**
  - **[Ubuntu 1604][u1604]**
  - **[CentOS 7.4][c7]**

In the box:

- **Windows 10 Enterprise** 1709 (15063.674) and **Windows Server** 1709 (14393.1770)
  - Operating system
    - Administrator user with user name `vagrant` and password `vagrant` set to never expire
    - WinRM service enabled
    - UAC disabled
    - Windows Updates installed and service disabled
    - Windows Defender service disabled
    - Remote Desktop enabled
    - Generalized with Sysprep
  - Tools
    - [Chocolatey](https://chocolatey.org/packages/chocolatey/) 0.10.8
    - [7-Zip](https://chocolatey.org/packages/7zip/) 16.4.0
    - [Chef Client](https://chocolatey.org/packages/chef-client/) 12.14.77
    - **VirtualBox** [VirtualBox Guest Additions](https://www.virtualbox.org/manual/ch04.html) 5.1.22
      - Recommended to have VirtualBox version 5.1.22 or later on the host
    - **Hyper-V** Generation 1, Configuration Version 8.0
      - Requires Windows 10 or Windows Server 2016 version 1607 or later on the host
  - Vagrant box
    - WinRM communicator
    - 1 CPU
    - 1 GB RAM
    - **VirtualBox** Port forwarding for RDP from 3389 to 33389 with auto correction
    - **Hyper-V** IP address reporting timeout of 5 minutes

- **Docker for Windows Community** 17.09 Edge
  - **VirtualBox** Windows containers on Windows Server 2016
  - **Hyper-V** Linux and Windows containers on Windows 10 and Windows Server 2016

[Operating systems]: #operating-systems

[w10e]: https://app.vagrantup.com/stephanebouchard/boxes/w10e
[w10e-docker-ce]: https://app.vagrantup.com/stephanebouchard/boxes/w10e-docker-ce
[w16s]: https://app.vagrantup.com/stephanebouchard/boxes/w16s
[w16s-docker-ce]: https://app.vagrantup.com/stephanebouchard/boxes/w16s-docker-ce
[u1604]: https://app.vagrantup.com/stephanebouchard/boxes/u1604
[c7]: https://app.vagrantup.com/stephanebouchard/boxes/c7

## Getting started

[Getting started]: #getting-started

## Usage

[Usage]: #usage

## Next steps

[Next steps]: #next-steps

## Contributing

Any feedback, [issues] or [pull requests] are welcome and greatly appreciated.

[Contributing]: #contributing

[Issues]: https://github.com/stephanebouchard/packer-templates/issues/
[Pull requests]: https://github.com/stephanebouchard/packer-templates/pulls/

## Resources

This repository could not exist without the following great tools:

* [Packer]
* [Vagrant]
* [VirtualBox]
* [Hyper-V]

This repository borrows awesome ideas and solutions from the following sources:

* [Alex Smagin]
* [Gusztav Vargadr]
* [Matt Wrock]
* [Jacqueline]
* [Joe Fitzgerald]
* [Boxcutter]

[Resources]: #resources

[Alex Smagin]: https://github.com/asmagin/sitecore-packer/
[Gusztav Vargadr]: https://github.com/gusztavvargadr/packer/
[Matt Wrock]: https://github.com/mwrock/packer-templates/
[Jacqueline]: https://github.com/jacqinthebox/packer-templates/
[Joe Fitzgerald]: https://github.com/joefitzgerald/packer-windows/
[Boxcutter]: https://github.com/boxcutter/windows/
