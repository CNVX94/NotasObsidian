#Redes 
## Modificación para [[VLAN]]

### Para una sola [[VLAN]]:

*Recordar usar 0/0.X para el valor de la VLAN utilizada*

```bash
R-IZQ(config)# interface FastEthernet0/0
R-IZQ(config-if)# no shutdown

R-IZQ(config)# interface FastEthernet0/0.10
R-IZQ(config-subif)# encapsulation dot1Q 10
R-IZQ(config-subif)# ip address 192.168.100.1 255.255.255.0
```

### Para más de una [[VLAN]]:

```bash

R-IZQ(config)# interface FastEthernet0/0
R-IZQ(config-if)# no shutdown

R-IZQ(config)# interface FastEthernet0/0.10
R-IZQ(config-subif)# encapsulation dot1Q 10
R-IZQ(config-subif)# ip address 192.168.100.1 255.255.255.0

R-IZQ(config)# interface FastEthernet0/0.20
R-IZQ(config-subif)# encapsulation dot1Q 20
R-IZQ(config-subif)# ip address 192.168.200.1 255.255.255.0

```

### Habilitar enrutamiento con otro Router

*Ejemplo con IP de práctica*

```bash
R-IZQ(config)# ip route 0.0.0.0 0.0.0.0 10.15.76.2
```




## Notas

*Es mejor tener configuradas las VLAN desde el principio: configuración desde [[Switch_PacketTracer]]*
