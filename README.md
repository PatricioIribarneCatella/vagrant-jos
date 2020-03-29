# vagrant-jos

_Vagrantfile_ for running _JOS_ and its dependencies in a [_Vagrant_](https://www.vagrantup.com/downloads.html) virtual machine.

### Setup

Just copy your _jos_ folder into this repository and then run:

```bash
$ vagrant up
```

It will take some minutes while it downloads the _ubuntu_ image and then install all the dependencies.

### Running

Fisrt you need to connect to the virtual _Vagrant_ machine doing:

```bash
$ vagrant ssh
```

Then you are ready for running all the targets in the _JOS Makefile_. If you want to use _GDB_ you will need to open another terminal and login into the _Vagrant_ machine as you did before. Thats all!

