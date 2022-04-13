IP routing

1. I have Buikd this scheme of the network, where VM1 works like ganeway for VM2. Also I set NAT forwarding on the VM1 NAT adapnet for connection to VM1 and VM2

![image](https://user-images.githubusercontent.com/97533533/163141578-8184c1d9-0987-4f27-aa0c-d3c80c8a5dde.png)

![image](https://user-images.githubusercontent.com/97533533/163141748-47e5e968-5ffc-4f1b-b176-076784834a44.png)

![image](https://user-images.githubusercontent.com/97533533/163141848-d9d885e1-4aa0-4192-a57a-33f69ee26998.png)

2. For this exercise we must:

Configure interface eth0 on VM1:

sudo ip addr add 192.168.1.1/255.255.255.0 broadcast 192.168.1.255 dev eth0 

sudo ip link set eth0 up

Configure interface enp0s3 on VM2

sudo ip addr add 192.168.1.10/255.255.255.0 broadcast 192.168.1.255 dev enp0s3 

sudo ip link set enp0s3 up 

sudo ip route add default 192.168.1.1 via enpes3 

sudo echo nameserver 8.8.8.8 >> /etc/resolv.conf 

sudo echo nameserver 4.4.4.4 >> /etc/resolv.conf

Enable Forwarding on VM1

sudo echo 1> /proc/sys/net/ipv4/ip_forward

3. Add IPTABLES rules for forward SSH traffic to hosy VM2 and Masquerade traffic from VM2: image

![image](https://user-images.githubusercontent.com/97533533/163142290-8c757d31-9c79-42c4-a11d-43f34ae459ec.png)

4. Checking route from VM2 to host traceroute 4.4.4.6

![image](https://user-images.githubusercontent.com/97533533/163142606-61743ffa-0df2-480b-add3-77dccd431d11.png)

5. Checking internet connection ping 8.8.8.8

![image](https://user-images.githubusercontent.com/97533533/163142792-3f92b431-052e-42fa-ae51-062ed22b9a88.png)

6. For find who owner of the rosource I use "whois", this address (8.8.8.8) velongs to the Google DNS. whois 8.8.8.8

![image](https://user-images.githubusercontent.com/97533533/163143326-9f827a7f-d499-4624-8096-ad1d67d3f152.png)

or nslookup 8.8.8.8

![image](https://user-images.githubusercontent.com/97533533/163143429-42372e65-03eb-4466-b86e-5feca9df83f2.png)

7. For determine routes of my host based on Windows I use following command: route print.

8. My traceroute google.com

![image](https://user-images.githubusercontent.com/97533533/163143693-71453977-e70d-4e6f-9fb3-7f4d636fd147.png)








