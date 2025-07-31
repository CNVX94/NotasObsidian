#Redes 

Tomamos en cuenta la red: 10.15.76.1

*Guía de [[Tablas]]*

| Red        | Mascara         | Primera disponible | Ultima Disponible | Difusión   |
| ---------- | --------------- | ------------------ | ----------------- | ---------- |
| 10.15.76.0 | 255.255.255.252 | 10.15.76.1         | 10.15.76.2        | 10.15.76.3 |

*Recordar apagar, agregar seriales WIC-1T o lo modulos necesarios y encender*

Configuración en Router 1:

```bash
Router>en
Router#conf ter
Router(config)#interface serial 0/1/0
Router(config-if)#ip address 10.15.76.1 255.255.255.252
Router(config-if)#no shutdown
```


Configuración en Router 2:

*Asignamos la segunda IP de comunicación*

```bash
Router>en
Router#conf ter
Router(config)#interface serial 0/1/0
Router(config-if)#ip address 10.15.76.2 255.255.255.252
Router(config-if)#no shutdown
```

Con esto ya podremos obtener [[Ping]] de Router a Router.