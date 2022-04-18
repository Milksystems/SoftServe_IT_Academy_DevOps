Configuring DHCP, DNS servers and dynamic routing using OSPF protocol

Use already created internal-network for three VMs (VM1-VM3). VM1 has NAT and internal, VM2, VM3 – internal only interfaces.

![image](https://user-images.githubusercontent.com/97533533/163807218-948b58a6-5100-407d-9de8-65a36ba534ce.png)

![image](https://user-images.githubusercontent.com/97533533/163807273-b824c17d-32ad-4bfc-8b4c-d885100e288f.png)

![image](https://user-images.githubusercontent.com/97533533/163807351-2a668a1c-66e8-44a7-8dc8-aeeba1d03949.png)

![image](https://user-images.githubusercontent.com/97533533/163807387-622c6a0b-2f30-487a-aa2e-88015064869b.png)

Install and configure DHCP server on VM1. (3 ways: using VBoxManage, DNSMASQ and ISC-DHSPSERVER). You should use at least 2 of them.

