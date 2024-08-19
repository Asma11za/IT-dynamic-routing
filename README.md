<h1> Design and configure dynamic routing (RIP and OSPF) for non-profit educational organization </h1>

<h2> Network Topology: </h2>
<img src="https://github.com/user-attachments/assets/1476609d-374c-4ac2-95f2-353f89956865" alt="IMG_6095" width="600">

<h2> Methadology: </h2>

- Designing and configuring two network models that have several non-profit educational that provide many interactive rooms for creative learning. (The organization has branches located in different areas).
- Simulating network models to observe how the performance varies from the OSPF network to the RIP network.
- Calculate the packets lost in each protocol.
<br>
Calculation of packet loss = (Packet data send - Packet data revived / Packet data send)* 100

<h2> Software Tools Used: </h2>

- Cisco Packet Tracer.

<h2> Addressing Table: </h2>

| **Device**       | **Interface**    | **IP address**    | **Subnet Mask**   | **Default Gateway** |
| ---------------- | ---------------- | ----------------- | ----------------- | ------------------- |
| **R1**           | **S0/1/1 (DCE)** | **14.0.0.1**      | **255.0.0.0**     | **N/A**             |
| **S0/0/1**       | **10.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **S0/1/0**       | **11.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **R2**           | **G0/0**         | **192.168.1.1**   | **255.255.255.0** | **N/A**             |
| **S0/0/0 (DCE)** | **13.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **S0/0/1 (DCE)** | **10.0.02**      | **255.0.0.0**     | **N/A**           |
| **R3**           | **S0/0/0**       | **13.0.0.1**      | **255.0.0.0**     | **N/A**             |
| **G0/0**         | **192.168.2.1**  | **255.255.255.0** | **N/A**           |
| **S0/0/1**       | **12.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **R4**           | **S0/1/0 (DCE)** | **11.0.0.2**      | **255.0.0.0**     | **N/A**             |
| **S0/0/0 (DCE)** | **12.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **192.168.3.1**  | **255.255.255.0** | **N/A**           |
| **R5**           | **S0/0/0**       | **14.0.0.2**      | **255.0.0.0**     | **N/A**             |
| **S0/0/1**       | **15.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **S0/1/0**       | **17.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **S0/1/1 (DCE)** | **19.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **R6**           | **S0/0/0 (DCE)** | **16.0.0.1**      | **255.0.0.0**     | **N/A**             |
| **S0/0/1 (DCE)** | **15.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **194.168.1.1**  | **255.255.255.0** | **N/A**           |
| **R7**           | **S0/0/0**       | **16.0.0.2**      | **255.0.0.0**     | **N/A**             |
| **S0/0/1**       | **18.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **194.168.2.1**  | **255.255.255.0** | **N/A**           |
| **R8**           | **S0/0/0 (DCE)** | **18.0.0.2**      | **255.0.0.0**     | **N/A**             |
| **S0/1/0 (DCE)** | **17.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **194.168.3.1**  | **255.255.255.0** | **N/A**           |
| **G0/1**         | **194.168.4.1**  | **255.255.255.0** | **N/A**           |
| **R9**           | **S0/0/1**       | **20.0.0.1**      | **255.0.0.0**     | **N/A**             |
| **S0/1/1**       | **21.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **S0/1/0**       | **19.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **R10**          | **S0/0/0 (DCE)** | **20.0.0.2**      | **255.0.0.0**     | **N/A**             |
| **S0/0/1**       | **23.0.0.1**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **195.168.1.1**  | **255.255.255.0** | **N/A**           |
| **R11**          | **S0/0/0 (DCE)** | **23.0.0.2**      | **255.0.0.0**     | **N/A**             |
| **S0/0/1**       | **22.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **195.168.2.1**  | **255.255.255.0** | **N/A**           |
| **G0/1**         | **195.168.3.1**  | **255.255.255.0** | **N/A**           |
| **R12**          | **S0/0/0 (DCE)** | **22.0.0.1**      | **255.0.0.0**     | **N/A**             |
| **S0/1/0 (DCE)** | **21.0.0.2**     | **255.0.0.0**     | **N/A**           |
| **G0/0**         | **195.168.4.1**  | **255.255.255.0** | **N/A**           |
| **S1**           | **N/A**          | **VLAN**          | **N/A**           | **N/A**             |
| **S2**           | **N/A**          | **VLAN**          | **N/A**           | **N/A**             |
| **S3**           | **N/A**          | **VLAN**          | **N/A**           | **N/A**             |
| **S4**           | **N/A**          | **VLAN**          | **N/A**           | **N/A**             |
| **S5**           | **N/A**          | **VLAN**          | **N/A**           | **N/A**             |
| **PC - A**       | **Fa/0**         | **192.168.1.2**   | **255.255.255.0** | **192.168.1.1**     |
| **Laptop - A**   | **Fa/0**         | **192.168.1.3**   | **255.255.255.0** | **192.168.1.1**     |
| **PC - B**       | **Fa/0**         | **192.168.2.2**   | **255.255.255.0** | **192.168.2.1**     |
| **Printer - A**  | **Fa/0**         | **194.168.2.3**   | **255.255.255.0** | **192.168.2.1**     |
| **Laptop - B**   | **Fa/0**         | **192.168.3.2**   | **255.255.255.0** | **192.168.3.1**     |
| **Printer - B**  | **Fa/0**         | **194.168.3.3**   | **255.255.255.0** | **192.168.3.1**     |
| **PC - C**       | **Fa/0**         | **192.168.3.4**   | **255.255.255.0** | **192.168.3.1**     |
| **PC - D**       | **Fa/0**         | **192.168.1.2**   | **255.255.255.0** | **192.168.1.1**     |
| **Printer - C**  | **Fa/0**         | **194.168.1.3**   | **255.255.255.0** | **192.168.1.1**     |
| **PC – E**       | **Fa/0**         | **194.168.2.2**   | **255.255.255.0** | **194.168.2.1**     |
| **Laptop – C**   | **Fa/0**         | **194.168.2.3**   | **255.255.255.0** | **194.168.2.1**     |
| **PC – F**       | **Fa/0**         | **194.168.3.3**   | **255.255.255.0** | **194.168.3.1**     |
| **PC – G**       | **Fa/0**         | **194.168.4.4**   | **255.255.255.0** | **194.168.4.1**     |
| **PC - H**       | **Fa/0**         | **194.168.1.2**   | **255.255.255.0** | **194.168.1.1**     |
| **PC – K**       | **Fa/0**         | **194.168.1.3**   | **255.255.255.0** | **194.168.1.1**     |
| **Laptop – D**   | **Fa/0**         | **195.168.2.2**   | **255.255.255.0** | **195.168.2.1**     |
| **PC – L**       | **Fa/0**         | **195.168.3.3**   | **255.255.255.0** | **195.168.3.1**     |
| **Laptop – E**   | **Fa/0**         | **195.168.4.2**   | **255.255.255.0** | **195.168.4.1**     |
| **Printer - D**  | **Fa/0**         | **194.168.4.4**   | **255.255.255.0** | **194.168.4.1**     |


<h2> Routers configuration: </h2>

<h3> R1 </h3>
R1# configure terminal

Enter configuration commands, one per line. End with CNTL/Z.

R1(config)# interface Serial0/0/1

R1(config-if)# ip address 10.0.0.1 255.0.0.0

R1(config-if)# no shutdown

R1(config-if)# exit

R1(config)# interface Serial0/1/0

R1(config-if)# ip address 11.0.0.1 255.0.0.0

R1(config-if)# no shutdown

R1(config-if)# exit

<h3> R2 </h3>
R2# configure terminal

Enter configuration commands, one per line. End with CNTL/Z.

R2(config)# interface Serial0/0/1

R2(config-if)# ip address 10.0.0.2 255.0.0.0

R2(config-if)# no shutdown

R2(config-if)# exit

R2(config)# interface Serial0/0/0

R2(config-if)# ip address 13.0.0.2 255.0.0.0

R2(config-if)# no shutdown

R2(config-if)# exit

<h3> R3 </h3>
R3# configure terminal

Enter configuration commands, one per line. End with CNTL/Z.

R3(config)# interface Serial0/0/1

R3(config-if)# ip address 12.0.0.2 255.0.0.0

R3(config-if)# no shutdown

R3(config-if)# exit

R3(config)# interface Serial0/0/0

R3(config-if)# ip address 13.0.0.1 255.0.0.0

R3(config-if)# no shutdown

R3(config-if)# exit

<h3> R4 </h3>
R4# configure terminal

Enter configuration commands, one per line. End with CNTL/Z.

R4(config)# interface Serial0/0/0

R4(config-if)# ip address 12.0.0.1 255.0.0.0

R4(config-if)# no shutdown

R4(config-if)# exit

R4(config)# interface Serial0/1/0

R4(config-if)# ip address 11.0.0.2 255.0.0.0

R4(config-if)# no shutdown

R4(config-if)# exit

<h2> Configuration Routing RIP </h2>
(*Note): This configuration has been done inside all 12 routers to enable the RIP protocol

Router(config)# router rip

Router(config-router)# network 10.0.0.0

Router(config-router)# network 11.0.0.0

Router(config-router)# network 12.0.0.0

Router(config-router)# network 13.0.0.0

Router(config-router)# network 192.168.1.0

Router(config-router)# network 192.168.2.0

Router(config-router)# network 192.168.3.0

Router(config-router)# network 14.0.0.0

Router(config-router)# network 15.0.0.0

Router(config-router)# network 16.0.0.0

Router(config-router)# network 17.0.0.0

Router(config-router)# network 18.0.0.0

Router(config-router)# network 19.0.0.0

Router(config-router)# network 20.0.0.0

Router(config-router)# network 21.0.0.0

Router(config-router)# network 22.0.0.0

Router(config-router)# network 23.0.0.0

Router(config-router)# network 194.168.1.0

Router(config-router)# network 194.168.2.0

Router(config-router)# network 194.168.3.0

Router(config-router)# network 194.168.4.0

Router(config-router)# network 19.0.0.0

Router(config-router)# network 20.0.0.0

Router(config-router)# network 21.0.0.0

Router(config-router)# network 22.0.0.0

Router(config-router)# network 23.0.0.0

Router(config-router)# network 195.168.1.0

Router(config-router)# network 195.168.2.0

Router(config-router)# network 195.168.3.0

Router(config-router)# network 195.168.4.0

Router(config-router)# exit

<h2> Configuration Routing OSPF</h2>

Router(config)# router ospf 1

Router(config-router)# network 192.168.1.1 0.0.0.255 area 0

Router(config-router)# network 13.0.0.0 0.255.255.255 area 0

Router(config-router)# network 10.0.0.0 0.255.255.255 area 0

Router(config-router)# network 11.0.0.0 0.255.255.255 area 0

Router(config-router)# network 14.0.0.0 0.255.255.255 area 0

Router(config-router)# network 13.0.0.0 0.255.255.255 area 0

Router(config-router)# network 12.0.0.0 0.255.255.255 area 0

Router(config-router)# network 192.168.2.1 0.0.0.255 area 0

Router(config-router)# network 192.168.3.1 0.0.0.255 area 0

Router(config-router)# network 15.0.0.0 0.255.255.255 area 0

Router(config-router)# network 17.0.0.0 0.255.255.255 area 0

Router(config-router)# network 19.0.0.0 0.255.255.255 area 0

Router(config-router)# network 16.0.0.0 0.255.255.255 area 0

Router(config-router)# network 194.168.1.1 0.0.0.255 area 0

Router(config-router)# network 18.0.0.0 0.255.255.255 area 0

Router(config-router)# network 17.0.0.0 0.255.255.255 area 0

Router(config-router)# network 19.0.0.0 0.255.255.255 area 0

Router(config-router)# network 20.0.0.0 0.255.255.255 area 0

Router(config-router)# network 21.0.0.0 0.255.255.255 area 0

Router(config-router)# network 23.0.0.0 0.255.255.255 area 0

Router(config-router)# network 195.168.1.1 0.0.0.255 area 0

Router(config-router)# network 22.0.0.0 0.255.255.255 area 0

Router(config-router)# network 195.168.4.1 0.0.0.255 area 0


