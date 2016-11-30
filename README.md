# Vagrant configurations

These are useful for learning Linux and for learning system administration.  It
uses [Vagrant][vagrant] and [VirtualBox][vbox] to provision virtual machines
which are useful for learning.

Recommended system requirements for GUI VMs:

* 16GB RAM
* 512MB Video RAM
* 5GB disk free

For learning about Linux, it sometimes helps to provision Linux with a GUI to
get around.  However, professionally Linux is typically configured without a
GUI.  An OS with no GUI is called "headless".

# Provision Ubuntu with GUI

If you want to start with smaller requirements, then you'll need to edit the
memory in the `Vagrantfile`.

    cd ubuntu16.04-gui
    vagrant up

Ubuntu should bootstrap and eventually reboot with a GUI.  User name and
password is `ubuntu`.

# Provision headless machines

> Note: Only provision one of the following four Linux distros.  If you want to
> configure them all then there needs to be a separate folder (working
> directory) for each OS.  By running `vagrant init`, Vagrant will create a file
> named `Vagrantfile` in the current directory.  You can learn more about
> Vagrant by reading it.

Ubuntu 14.04

    vagrant init ubuntu/precise64
    vagrant up

Ubuntu 16.04

    vagrant init ubuntu/xenial64
    vagrant up

RedHat Enterprise Linux 6 (CentOS 6)

    vagrant init centos/6
    vagrant up

RedHat Enterprise Linux 7 (CentOS 7)

    vagrant init centos/7
    vagrant up

# Log into headless machines

    vagrant ssh

Now you're logged into the headless machine.

> Note: `vagrant` commands _must_ be run from the same directory in which you
> ran `vagrant up`.

# Delete virtual machines

    vagrant destroy

Learn more about Vagrant by reading documentation on the [Vagrant
website][vagrant].

[vagrant]: https://www.vagrantup.com/
[vbox]: https://www.virtualbox.org/
