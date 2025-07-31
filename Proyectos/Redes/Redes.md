#Redes

## IP

*Material de [[Tablas]]*

Numero de registro único en una red.

Una IP se compone de 4 partes y cada una es un conjunto de 4 bytes. de manera que tenemos disponibles 32 Byte.

Cada byte encendido representa una cantidad, y por lo tanto, una traducción en decimal para su aplicación: (Representación de un octeto)

*Recordemos que se realiza la suma de los valores activos siguiendo la regla de la cantidad que queremos conseguir*

| Numero | 128 | 64  | 32  | 16  | 8   | 4   | 2   | 1   |
| ------ | --- | --- | --- | --- | --- | --- | --- | --- |
| 255    | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |
*Entendiendo resto, recordemos que en redes tenemos 256 porque la red 0 también cuenta pero por la forma en que se distribuyen la IP a continuación disponible sera usable*

Por lo tanto, una red puede verse así:

0000 0000 . 0000 0000 . 0000 0000 . 0000 0000  = 0
1111 1111 . 1111 1111 . 1111 1111 . 1111 1111  = 255

----

### Clases de Redes:

![[Pasted image 20250521003033.png]]

A, B y C son nuestras principales redes a recordar, esto nos ayuda generalmente a reconocer la mascara de red.

____

Podemos entender rápidamente las redes IP como una traducción de números en binario a decimal, los cuales se interpretan como bits encendidos:

| IP            | Mascara       |
| ------------- | ------------- |
| 192.168.100.1 | 255.255.255.0 |
| 10.15.0.1     | 255.255.255.0 |

### ¿Por qué son iguales?

Únicamente disponemos de el ultimo octeto de red para poder compartir redes según los bits asignados.

## Mascara de Red

Retomando el apunte, según el valor inicial de nuestra red o las redes que tengamos realmente la capacidad de asigna, tomando algunos principios de [[Subnneting]], tendremos por defecto lo siguiente:

| Clase | Valor   | Mascara       | Byte |
| ----- | ------- | ------------- | ---- |
| A     | 1-127   | 255.0.0.0     | /8   |
| B     | 128-191 | 255.255.0.0   | /16  |
| C     | 192-223 | 255.255.255.0 | /24  |

Estas mascaras se aplican por defecto ya que interpretamos que *255* nos indica prácticamente que no podemos usarlos, esto es debido a que esos octetos son fijos tomando en cueta que son el valor de la red base.

________