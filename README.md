# VM_Network
Hyper-V

VMs are isolated, even when they are running on the same (VM) host, and are communicate with others and each other only over the network.

            ------------------------------- Host ------------------
            |                                                     |
            |   ----------------------                            |
            |   |                    |                            |
            |   |    VM1 kernel      |                            |
            |   |      |             | ....  VMn                  |
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
                | physical SW | -------- (another IP addr) ----- Pro ENV
                |_____________|
                    |          \
                    |           \
                (Single IP adde) \
               Internet      shared storage
                    |
                Test ENV

VMware or Hyper-V includes vSW playing a role as NIC (網路卡網孔), which enable basic network Packet-Forward and Support for Network Virtualization.

Administrator can connect a vSW to different network, and based on this connection, a private/internal/external vSW can be created.


![vsw](https://www.nakivo.com/blog/wp-content/uploads/2018/07/Virtual-switches-of-an-ESXi-host-1024x901.png)


If the features also includes Virtual Hardware (vHard-Disk) supported by Hardware, then it also can have Single Root I/O & Dynamic VM Queue, which enable higher network throuput & lower CPU utilization and consumption.


# Virtual SW


* Netwok Features:


* Config


* Test

# Apply Scenario

Administrator may be asked to demo how to do a Network Virtualization, which aims at to seperate TEST & Preproduction ENVs that are using the same network infra.

IT operator will ensure that the servers in both ENVs can use the "Same IP addr", and can communicate with other servers that are in the same ENV.

* Demo Steps:

1. ping IP addresses to different ENV to diff ports of NIC.

2. cfrm the  port has connectivity with other 3 VMs.

3. 

4.

5.

6.

7.

8.

9.

10.

11.
