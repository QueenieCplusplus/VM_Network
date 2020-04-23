# VM_Network
Hyper-V

            ------------------------------- Host ------------------
            |                                                     |
            |   ----------------------                            |
            |   |                    |                            |
            |   |    VM kernel       |                            |
            |   |      |             |                            |
            |   |   vNIC (2-4 ports) |                            |
            |   ---------------------                             |
            |       |     |                                       |
            |       |     |                                       |
            |       |     |                                       |
            |      --------------------    --------------------   |
            |      |  vSW             |    |  vSW             |   |
            |      --------------------    --------------------   |
            |        |  |                     |  |                |
            |     NIC of Host             NIC of Host             |
            |------- |  | ------------------- |  |----------------|
                 _____________
                |             | 
                | physical SW |
                |_____________|
                    |          \
                    |           \
               Internet         shared storage


VMs are isolated, even when they are running on the same (VM) host, and are communicate with others and each other only over the network.


![vsw](https://www.nakivo.com/blog/wp-content/uploads/2018/07/Virtual-switches-of-an-ESXi-host-1024x901.png)

VMware or Hyper-V includes vSW playing a role as NIC (網路卡網孔), which enable basic network Packet-Forward and Support for Network Virtualization.

Administrator can connect a vSW to different network, and based on this connection, a private/internal/external vSW can be created.

If the features also includes Virtual Hardware (vHard-Disk) supported by Hardware, then it also can have Single Root I/O & Dynamic VM Queue, which enable higher network throuput & lower CPU utilization and consumption.


# Virtual SW


* Netwok Features:


* Config


* Test
