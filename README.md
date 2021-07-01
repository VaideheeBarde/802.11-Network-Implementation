# 802.11-Network-Implementation

Initially, we installed ns-3 on our Linux system in our laptop. We make a copy of the template code and put it in ns3.26 installation.
The first simulation is the one for point to point transmission. We run the simulation for 20 seconds.
As a result of this simulation, we get two pieces of information.
- The total number of packets received by the receiver as a text output on the terminal.
- Two .pcap files that capture all the packets that travel through each of the nodes in the network. These files can be analyzed using wireshark.
We change the simulation parameter n ie the number of nodes and add one more node into the network. When we add more nodes into the network, the throughput of the network increases.  Also, the number of packets received also increases.
The third part of the project was to increase the distance. We increased the distance between all the 3 nodes from 100 to 350. After increasing the distance, the number of packets received are reduced due to increase in the transmission time between the transmitter and the receiver. Also there exists hidden node problem which leads to the decrease in the number of packets.
Now, we enable the RTS and CTS by uncommenting the lines of code.
We run the simulation with 3 nodes and a distance of 350 between each nodes.
RTS CTS handshake is obtained by changing the threshold value from 2200 to 0. This threshold sets the value for packet size. Any packet above this threshold value will have to do a RTS CTS handshake.
After enabling RTS CTS, there has been a dramatic increase in the number of packets received due to reduced number of collisions.
Transmitter send an RTS and waits for the receiver to reply back with a CTS.
Throughput for a different number of users:
Firstly, we start using the random grid location model and use the mobility_Rx function. We set the receiver randomly around the transmitter in a circle and set the distance of the receiver to (500,500).
Thus, we keep on increasing the number of users to 10,20 and 30. As we increase the number of users, the number of packets received and the throughput decreases.
