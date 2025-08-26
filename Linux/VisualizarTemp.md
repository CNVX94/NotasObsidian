#Facilidades #Linux

Aquí tenemos el código para simplificar la llamada al monitor de temperaturas:

```bash
alias temp='watch -n 2 sensors'
```

De manera que ahora solo lo llamamos en terminal:

```bash
temp
```

Esto es posible gracias a que la Think-Pad tiene una propiedad orientada al control y registro de la batería.

