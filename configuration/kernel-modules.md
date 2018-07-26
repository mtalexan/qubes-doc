Kernel Module Overview
=======================
Source of a Kernel
--------------
Building of kernel modules is dependent on the kernel they're being built for, and is therefore very dependent on how the kernel is supplied to a VM.
Building kernel modules also requires some source code and build tools used to originally build the kernel the module will be used with.
From the [kernel overview](/doc/configuration/managing-vm-kernel.md) the following relevant points emerge:
1. kernels are either fully contained within the the VM, or they are provided by dom0
2. Fully contained kernels are either VM-distribution provided, or are custom built
3. dom0 provided kernels are packaged and provided by QubesOS, with the primary use being a secure dom0 VM

Concerns and Difficulties
------------------------


Summary
-----------------
In summary, the following information is important when building a kernel module:
1. What type of VM will the module be used in: TemplateVM, DispVM, or dom0?
2. What is the source of the kernel the module will be used against
3. What tools are necessary to create/maintain the module (e.g. kmod)?
4. What extra components are necessary to use the module (e.g. firmware)?
