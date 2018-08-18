# netlink sockets (draft)

Linux中userspace和kernel space通信有以下的几种方式:

* system call
* ioctl
* /proc 文件系统
* netlink

netlink 是基于socket的进程间通信(IPC) 机制，主要用于userspace和kernel space的双向通信，与其他方式比较优点是：双工，异步，支持多播(multicast)

userspace之间的IPC可以通过Unix domain socket来实现通信, 不必用netlink。

