If you have a container that requires Layer 2 connectivity e.g. for IP multicast in/out. Then macvlan is one way to achieve this.

## Pros
- The container sits on the network of your ethernet interface

## Cons
- The downside is that your container will be sitting on the Layer 2 domain and requires you to have some firewalling in place on the container, rather than depending on the host
- You cannot communicate between your container and the host machine due to the security restrictions in the Linux kernel. So pinging is not possible. You therefore need a separate interface to achieve communication
- Promiscuous mode requirement may be undesirable




