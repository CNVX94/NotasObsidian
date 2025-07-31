#Redes 

## Asignar [[IP]] a una interfaz fastEthernet

*Guía de [[Tablas]]*

| Red           | Mascara       | Primera disponible | Ultima Disponible | Difusión        |
| ------------- | ------------- | ------------------ | ----------------- | --------------- |
| 192.168.100.0 | 255.255.255.0 | 192.168.100.1      | 192.168.100.254   | 192.168.100.255 |

Configuración en Router fastEthernet 0/0:

```bash
Router>en
Router#conf t
Router(config)#interface fastEthernet 0/0
Router(config-if)#ip address 192.168.100.1 255.255.255.0
Router(config-if)#no shutdown
```

Para más de una VLAN: [[Router_Switch_Vlan]]