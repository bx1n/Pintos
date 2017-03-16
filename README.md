# Introduction

[Pintos](https://web.stanford.edu/class/cs140/projects/pintos/pintos.html#SEC_Top) is a simple operating system framework for the 80x86 architecture. It supports kernel threads, loading and running user programs, and a file system, but it implements all of these in a very simple way. This assignment was used in MIT as a part of OS course.

Doing this as an assigments would give you a clear idea on the various topics in OS. This guide will take you through how to install Pintos in your native Ubuntu machine. Pintos is a very small operating system and can run it on a virtual machine. The tutorial will be using [Qemu](http://www.qemu-project.org/) to run Pintos.

Once you are finished setting up the Pintos you can start working on your assignments.

# Setting up

**Step 1: Install Qemu**

If you are using Ubuntu: ```sudo apt-get install qemu```

**Step 2: Download Pintos**

Download Pintos from [here](http://www.stanford.edu/class/cs140/projects/pintos/pintos.tar.gz). Extract it in your home folder. Eg: /home/abhi/os. 'abhi' is your $HOME folder

**Step 3: Set GDBMACROS**

Now open the script ‘pintos-gdb’ (in $HOME/os/pintos/src/utils) in any text editor. Find the variable GDBMACROS and set it to point to ‘$HOME/os/pintos/src/misc/gdb-macros’.

Your 'gdb-macros' file will contain ```GDBMACROS=/home/abhi/os/pintos/src/misc/gdb-macros```

**Step 4: Compiling utilities**

Go to /home/pintos/os/src/utils ```cd /home/abhi/os/pintos/src/utils```

And compile utilities folder ```make```

If this preoduces an error: “Undefined reference to ‘floor'” then edit “Makefile” in the current directory and replace “LDFLAGS = -lm” by “LDLIBS = -lm” and compile again.









 
