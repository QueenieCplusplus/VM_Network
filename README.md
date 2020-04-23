# VM_Network
Hyper-V

VMs are isolated, even when they are running on the same (VM) host, and are communicate with others and each other only over the network.

            ------------------------------- Host 1 ----------------
            |                                                     |
            |   ----------------------                            |
            |   |                    |                            |
            |   |    VM1 kernel      |                            |
            |   |      |             | ....  VMn                  |
            |   |   vNIC (2-4 ports) |                            |
            |   ---------------------                             |
            |       |     |                                       |
            |       |     |                                       |
            |       |     |            Groups...                  |
            |      --------------------    --------------------   |
            |      |  vSW             |    |  vSW             |   |
            |      --------------------    --------------------   |
            |        |  |                     |  |                |
            |     NIC of Host             NIC of Host             |
            |------- |  | ------------------- |  |----------------|
                     |  |                     |  |
                 PrePro Pro                 Test1 Test2 
                  
            
                 ____|__|______
                |             | 
                | physical SW | ------ Host 2 
                |             | 
                |_____________| 
                    |          \
                    |           \
                (Single IP adde) \
               Internet      shared storage
                    |
                    |
                
                Internet
               

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

1. ping IP addresses to different ports named ENV.

         PreProd$
         
               to Test1 10.0.0.16
               to Prod 10.0.0.25
               to Test2 10.0.0.26

2. cfrm the  has connectivity with other 3 VMs.

3. on Host, use below cmd to cfrm the PreProd has a VitualSubnetld property val of 0. 

         Get-VMNetworkAdapter

4. to determine the Ethernet index num for the above mentioned adapter on Host1 & Host2.

5.  

6.

7.

8.

9.

10.

11.
