# vagrant-jos

_Vagrantfile_ for running _JOS_ and its dependencies in a [_Vagrant_](https://www.vagrantup.com/downloads.html) virtual machine.

### Setup

Just copy your _jos_ folder into this repository and then run:

```bash
$ vagrant up
```

It will take some minutes while it downloads the _ubuntu_ image and then install all the dependencies.

### Running

First you need to connect to the virtual _Vagrant_ machine doing:

```bash
$ vagrant ssh
```

As explained in the script `cp-jos` in this project, _JOS_ file system (_LAB5_) use `mmap(2)` syscall with `MAP_SHARED` flag on. _Vagrant_ virtual machines implement shared files between the working directory where the _Vagrantfile_ is located and the `/vagrant` directory. If you run `make` in that _JOS_ directory it will fail the `mmap(2)` syscall.

For that reason, when you login, there will be a _JOS_ folder in your `HOME` directory ready for testing. You `cd` into it and you are ready for running `make` and all the other targets in the _JOS Makefile_. If you want to use _GDB_ you will need to open another terminal and login into the _Vagrant_ machine as you did before. Thats all!

- Changes

When you make some changes in your local _JOS_ project, you will then need to update the local copy of it in the `HOME/jos` directory. Just run the command:

```bash
$ cp-jos
```

and you are done!

