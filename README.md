# Vagrant LegoUSBTower

This configures a headless Ubuntu virtual machine to communicate with Lego Mindstorms control bricks. A vm is kind of overkill, but it serves as a container for the LegoUSBTower drivers and the NQC compiler.

First, you need Virtualbox and Vagrant.

Once you have those installed, clone this project and run `vagrant up`. That'll take some time. When it's done, your vm should be ready to go.

Try `./send example.nqc` with the LegoUSBTower plugged in and pointed at your powered-on control brick. The `send` script is an example of sending commands to the vm via `vagrant ssh`.
