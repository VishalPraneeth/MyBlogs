# Understanding Linux Kernel concepts for DevOps.

### Introduction

![Image](https://pbs.twimg.com/media/FpTQNU7agAAHFXh?format=jpg&name=small align="left")

To begin with, it's important to understand that the Linux kernel is not a complete operating system on its own. Rather, it is a component of an operating system known as GNU/Linux Which is the combination of the GNU project's userland tools and the Linux kernel.

### General Layout

![Image](https://pbs.twimg.com/media/FpTQU9qakAAIo-C?format=jpg&name=900x900 align="left")

Kernel Space is responsible for accessing and sharing the hardware. It runs important system functions with higher privileges user applications run with lower privileges in a separate space. This distinction is important for maintaining security.

### Monolithic Kernel

![Image](https://pbs.twimg.com/media/FpTQbk9aIAAJ8VV?format=jpg&name=900x900 align="left")

Linux primarily uses a monolithic kernel design. This design lacks access protection between subsystems and allows direct calling of public functions. The monolithic design can offer fast performance, but it may be more vulnerable to errors and crashes.

### Microkernel

![Image](https://pbs.twimg.com/media/FpTQmIAaQAA0CB4?format=jpg&name=900x900 align="left")

It provides access protection between its subsystems and uses message passing for inter-process communication This design will offer better security and stability but may be slower due to the need for message passing.

### Virtual address space

![Image](https://pbs.twimg.com/media/FpTQ6w6aIAA1BO5?format=jpg&name=900x900 align="left")

It is simply a range of virtual memory addresses that a process can access, here user and kernel spaces share VAS with kernel space at the top and user space at the bottom. The kernel creates mappings to prevent user processes from accessing kernel space.

### Asymmetric Multi-Processing

![Image](https://pbs.twimg.com/media/FpTRC8caYAAgLDF?format=jpg&name=900x900 align="left")

In this type of architecture where the processors in a system are not equal in terms of their processing power or capabilities. The idea behind ASMP is to provide a way to optimize the performance of different parts of a system by assigning tasks to the appropriate core.

### Symmetric Multi-Processing

![Image](https://pbs.twimg.com/media/FpTRHnkaAAAXMn0?format=jpg&name=900x900 align="left")

Linux has been designed to support SMP from the beginning, Where multiple processors are connected to a single shared memory. This allows the processors to work together on a given task, making the system more efficient.

### Source code Layout

![Image](https://pbs.twimg.com/media/FpTRQYyaUAEAlkE?format=jpg&name=900x900 align="left")

It has a bunch of top-level folders where each folder has its own set of code some of which like The arch contains arch code specific to (distro) Block has code that deals with block devices and creates block I/O requests.

### Architecture

![Image](https://pbs.twimg.com/media/FpTRfcNaIAEYPZZ?format=jpg&name=900x900 align="left")

It consists of different layers of code, each responsible for a specific task such as memory management, process management, and device drivers. The code is written in the C programming language, and developers can build on top of it.

### Network stack

![Image](https://pbs.twimg.com/media/FpTS28VaAAIlBA0?format=jpg&name=900x900 align="left")

It's an interface for applications to interact with the network. It provides a powerful and flexible framework for managing network communications in the GNU/Linux operating system.

### Virtual file system

![Image](https://pbs.twimg.com/media/FpTR0h5aMAIkH5_?format=jpg&name=900x900 align="left")

It sits on the top of the block I/O layer and provides a layer of abstraction between the filesystems and the applications that use them. It enables applications to interact with the filesystems in a consistent way, regardless of the underlying filesystem type.

### Block I/O

![Image](https://pbs.twimg.com/media/FpTS_D0aEAEj4VF?format=jpg&name=900x900 align="left")

It's the layer that sits between the storage devices and the higher-level file systems, handling requests for read and write operations. It uses a queue-based algorithm to manage the I/O requests so that the requests are processed in the most efficient way.

---

*I'll be covering the other Linux topics in my upcoming blogs. Please stay tuned, and share your feedback.*

### **Guys, you can connect with me on LinkedIn and GitHub.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1676386979809/f85946a9-b3ab-4d46-a39b-49cb17feeca2.gif?auto=format,compress&gif-q=60&format=webm align="left")

If you run an organization and want me to write content for you, please do connect with me 🤝.