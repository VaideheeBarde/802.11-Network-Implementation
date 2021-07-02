# 802.11-Network-Implementation

1.) REQUIREMENTS -
Software installation - NS3.26
Programming Language - C++ (Any programming language of choice)

2.) Simulation 1 
- Aim - Point to point transmission
- Simulation parameters - n = number of nodes, d = distance between nodes
- Simulation time - 20 seconds
- Result - 1.) The total number of packets received by the receiver as a text output on the terminal. 2.) Two .pcap files that capture all the packets that travel through each of the nodes in the network. These files can be analyzed using wireshark.
- Part 1 - Simulate using original n and d, e.g. n=5, d=100
- Part 2 - increase the number of nodes (increasing n improves throughput and also increases the number of packets received).
- Part 3 - increase the distance between the nodes (increasing d increases the transmission time between the transmitter and the receiver in additon to hidden node problem that leads to decrease in n).
- Part 4 - enable RTS/CTS handshake in the code by setting the threshold value for the packet size above which an RTS/CTS handshake would be performed.


The third part of the project was to increase the distance. We increased the distance between all the 3 nodes from 100 to 350. After increasing the distance, the number of packets received are reduced due to increase in the transmission time between the transmitter and the receiver. Also there exists hidden node problem which leads to the decrease in the number of packets.
Now, we enable the RTS and CTS by uncommenting the lines of code.
We run the simulation with 3 nodes and a distance of 350 between each nodes.
RTS CTS handshake is obtained by changing the threshold value from 2200 to 0. This threshold sets the value for packet size. Any packet above this threshold value will have to do a RTS CTS handshake.
After enabling RTS CTS, there has been a dramatic increase in the number of packets received due to reduced number of collisions.
Transmitter send an RTS and waits for the receiver to reply back with a CTS.
Throughput for a different number of users:
Firstly, we start using the random grid location model and use the mobility_Rx function. We set the receiver randomly around the transmitter in a circle and set the distance of the receiver to (500,500).
Thus, we keep on increasing the number of users to 10,20 and 30. As we increase the number of users, the number of packets received and the throughput decreases.
