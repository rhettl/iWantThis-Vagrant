# iWantThis Vagrant Runner

This will run a VirtualBox/Vagrant machine, use git to download php code for iWantThis Project, and install dependancies via bower and any other required tools.

## Dependancies

- VirtualBox (4.2 or 4.3)
- Vagrant (Current Stable)

##Directions

After VBox and Vagrant are installed, run 

`$ git clone git@github.com:ishowcaseiWantThis-vagrant iWantThis && cd iWantThis/`

Then, once in the downloaded directory with the `VagrantFile`, run 

`$ vagrant up`

To stop run gently

`$ vagrant halt`

To SSH in

`$ vagrant ssh`

To view from web direct browser to http://192.168.33.10/

