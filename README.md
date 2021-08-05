# 802.11-Network-Implementation


1.) REQUIREMENTS -
Software installation - NS3.26
Programming Language - C++ 

2.) Simulation
- Aim - Point to point transmission
- Model used - Random grid location model, mobility_Rx function. We set the receiver randomly around the transmitter in a circle and set the distance of the receiver to (500,500).
- Simulation parameters - n = number of nodes, d = distance between nodes
- Simulation time - 20 seconds
- Result - 1.) The total number of packets received by the receiver as a text output on the terminal. 2.) Two .pcap files that capture all the packets that travel through each of the nodes in the network. These files can be analyzed using wireshark.
- Part 1 - Simulate using original n and d, e.g. n=5, d=100.
- Part 2 - increase the number of nodes (increasing n improves throughput and also increases the number of packets received). We keep on increasing the number of users to 10,20 and 30. As we increase the number of users, the number of packets received and the throughput decreases.
- Part 3 - increase the distance between the nodes (increasing d increases the transmission time between the transmitter and the receiver in additon to hidden node problem that leads to decrease in n). We increase the d from 100 to 300.
- Part 4 - enable RTS/CTS (transmitter/receiver) handshake in the code by setting the threshold value for the packet size above which an RTS/CTS handshake would be performed. RTS/CTS handshake improves the number of packets received due to reduced number of collisions.
