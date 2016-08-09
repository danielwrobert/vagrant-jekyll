# Vagrant Jekyll

A basic Vagrant setup with RVM, Ruby, and Jekyll.
Uses the ubunty/trusty64 Vagrant box for the official Ubuntu Server 14.04 LTS (Trusty Tahr) builds.

## Getting started

To get up and running with this environment, you first need to have Virtualbox and Vagrant installed on your system.

If you don't already have those, visit the downloads pages below and follow the instructions for your operating system:

* [Virtualbox Downloads](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant Downloads](https://www.vagrantup.com/downloads.html)

Once you're set up with those, you can download the `Vagrantfile` from this repo, place it in the root directory of your project, and run `vagrant up` from your Terminal application.

After everything installs, you can run `vagrant ssh`. This will shell you in to your local Vagrant instance. Have a look around, if you'd like, but the main folder you want to be aware of is the shared directory. This directory is shared between your virtual machine and your local project directory. In this setup (and the default Vagrant setup) that is the `/vagrant` folder.

To run Jekyll, move into the shared folder, `cd /vagrant` and run your Jekyll commands from there. Note that, since localhost is the default host for Jekyll, you will need to run `jekyll serve --host 0.0.0.0 --force_polling` for the server to be available from outside of your Vagrant instance (i.e., your local web browser). You can keep this running in a separate Terminal tab (or screen, whatever your preference) and then work on your project files from your project directory on your system with your preferred editor.

That's all there is to it. Now you have Ruby, RVM, and Jekyll installed in a virtual machine and your local system environment is left untouched!
