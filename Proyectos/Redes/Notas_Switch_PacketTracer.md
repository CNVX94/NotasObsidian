#Redes 

[[Router_PacketTracer]]

1. Por alguna razón, cuando hay varias VLAN el puerto del que viene el fastEthernet del Router al Switch debe estar truncado...
2. Recordar la configuración para dar red a sub red:

	```bash
R-IZQ(config)# interface FastEthernet0/0.10
R-IZQ(config-subif)# encapsulation dot1Q 10
R-IZQ(config-subif)# ip address 192.168.100.1 255.255.255.0
	```

	Por alguna razón olvido el _encapsulation_ _dot1q_ _10_
