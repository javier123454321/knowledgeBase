# Virtualization

Computers function by transforming a physical resource into *virtual*
versions of itself in this process called Virtualization. The OS will
then expose some native functionality through system calls (APIs or
Standard Libraries). Virtualization allows for shared time (concurrency)
and Memory (resources) CPUs are sometimes considered resource managers.

A CPU, even when single threaded can simulate a concurrent computation
through virtualization. It has policies on how it does that.

You can effectively have a multi threaded programthat is printing the 
memory space of an operation (a range of bytes that it is allocating to 
its memory) and due to the fact that it is running concurrently, the 
programs will seem to be reffering to the same exact address in the hardware.

Of course that the hardware is managing these collitions, through a process
of virtualizing the memory space and allocating a virtual machine to each 
process. The process then behaves as though it has access to the entire memory
space of the machine and it effectively does have complete access to the virtual
machine. The actual physical hardware however, is compartamentalzing the avcailable
physical memory to each process.
