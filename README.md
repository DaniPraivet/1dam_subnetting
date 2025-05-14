# 1dam_subnetting
## Daniel Rodríguez Pérez
Ejercicios de subnetting

### Crear 4 subredes desde la red 192.168.1.0/24
Buscar un número elevado a 2 que de 4

2^2=4 /24+2 = /26 <br>
/32 -> límite de máscara <br>
/32-/26 = 6 <br>

2^6= 64 número mágico

- 192.168.1.0/26
- 192.168.1.64/26
- 192.168.1.128/26
- 192.168.1.192/26


---------------------------------------------

### Crear 8 subredes desde la red 192.168.1.0/24
Buscar un número elevado a 2 que de 8 <br>
2^3=8 -> /24+3 = /27 <br>


/32-/27 = 5 <br>
2^5=32 <br>

- 192.168.1.0/27
- 192.168.1.32/27
- 192.168.1.64/27
- 192.168.1.96/27
- 192.168.1.128/27
- 192.168.1.160/27
- 192.168.1.192/27
- 192.168.1.224/27

---------------------------------------------

### Crea 10 subredes del mismo tamaño teniendo en cuenta las siguientes representaciones:
Red -> 10101100.00010000.00000000.00000000 <br>
Máscara-> 11111111.11111111.00000000.00000000

Red -> 172.16.0.0 <br>
Máscara-> 255.255.0.0 <br>
Buscar un número elevado a 2 mayor o igual <br>
a 10 <br>
2^3 = 8 <br>
2^4 = 16 -> usaremos 10 <br>

/16+4 -> /20 <br>

32-20 = 12 <br>

2^12 = 4096 <br>

12>8 <br>

12-8 = 4 (al ser superior que 8, omitimos el segundo octeto, trabajaremos en el nivel superior) <br>

2^4 = 16 -> número mágico <br>

- 172.16.0.0
- 172.16.16.0
- 172.16.32.0
- 172.16.48.0
- 172.16.64.0
- 172.16.80.0
- 172.16.96.0
- 172.16.112.0
- 172.16.128.0
- 172.16.144.0

---------------------------------------------

### ¿Podría crear 300 subredes de 2000 hosts teniendo en cuenta los siguientes datos?
Red -> 00001010.00000000.00000000.00000000
Máscara -> 11111111.00000000.00000000.00000000

32-8=24 bits de hosts disponibles

2^24=16.777.216

2000≈2048

16.777.216/2048 ≈ 8000 (8192) subredes para los 2000 hosts, por lo que sí se pueden hacer 300

---------------------------------------------

### ¿Cuántas subredes necesitaría y cuáles serían para tener en cuenta los siguientes requisitos?
IP -> 172.16.0.0/23
Máscara -> 255.255.254.0

1. 200 hosts en 1 red
2. 100 hosts en 1 red
3. 50 hosts en 1 red
4. 25 hosts en 1 red
5. 10 hosts en 1 red


- 172.16.0.0/24
- 172.16.1.0/25
- 172.16.1.128/26
- 172.16.1.192/27
- 172.16.1.224/28

---------------------------------------------

### Dada la RED: 192.10.10.0/24, se necesitan 14 subredes y 14 hosts útiles por subred. ¿Cuál es la Máscara de Subred?
IP -> 192.10.10.0
Máscara -> 255.255.255.0

2^x>=14 subredes

2^4=16 subredes

/24+4=/28

/28 => 32-28 = 4 => 2^4 = 16 hosts por subred

16 - 2 = 14 hosts útiles

La máscara de subred es `255.255.255.240`


---------------------------------------------

### Dada la RED: 165.100.0.0, se necesitan 1000 y 60 hosts útiles por subred. ¿Cuál es la Máscara de Subred?
IP -> 165.100.0.0
Máscara -> 255.255.0.0

2^x >= 1000 subredes

2^10 = 1024 subredes

/16+10 = /26

/26 => 32-26 = 6 => 2^6 = 64 hosts por subred

64 - 2 = 62 hosts útiles

La máscara de subred es `255.255.255.192`


---------------------------------------------

### Dada la RED: 195.223.50.0, se necesita 1 subred útil.

Calcula:

a) La Máscara de Subred
b) la dirección de BROADCAST para la primera subred útil.

192.223.50.0 -> `255.255.255.0`

Añadimos un bit extra para tener 2 redes, de las cuáles usaremos solo 1.

/24+1 = /25 => 255.255.255.128

- 192.223.50.0/25
- 192.223.50.128/25

a) `255.255.255.128`

b) `192.223.50.127`


---------------------------------------------

### ¿Cuál de las siguientes subredes no pertenece a la misma red si se ha utilizado la máscara de subred 255.255.224.0?

- 172.16.66.24
- 172.16.65.24
- 172.16.64.42
- 172.16.63.51

Calculamos el rango


---------------------------------------------

### Teniendo en cuenta que la dirección de red es 192.168.168.0/24
- ¿Cuántas subredes puedo tener con 3 bits? <br>
2^3(nº de bits) = 8 subredes
- ¿Cuántos equipos puede tener cada subred? <br>
2^(32-(24+3))=> 2^5 = 32 <br>
32 equipos por cada subred
- ¿Cuáles son sus direcciones de red?
  - 192.168.168.0
  - 192.168.168.32
  - 192.168.168.64
  - 192.168.168.96
  - 192.168.168.128
  - 192.168.168.160
  - 192.168.168.192
  - 192.168.168.224
- ¿Cuál es la dirección de broadcast de la subred 3?<br>
`192.168.168.95/27`
- ¿Cuál sería un ejemplo de IP que podrías asignar a un host de la subred 1?<br>
`192.168.168.1/27`


---------------------------------------------

### Su red utiliza la dirección IP 172.30.0.0/16. Inicialmente existen 25 subredes con un conjunto mínimo de 1000 hosts por subred. Se prevé un crecimiento en los próximos años de 55 subredes. ¿Qué máscara de subred se denerrá utilizar?

- 255.255.240.0
- 255.255.248.0
- 255.255.252.0
- 255.255.254.0
- 255.255.255.0

  55 futuras = 80<br>
  55 >= 2^x<br>
  2^6 >= 80<br>
  2^6 = 128<br>
  /16+6=/22<br>
  /22 => `255.255.252.0`
  

---------------------------------------------

### A partir de la dirección IP 172.18.71.2 con máscara 255.255.248.0, ¿cuál es la dirección de subred y de broadcast a la que pertenece el host?

- 172.18.64.0 broadcast 172.18.80.255
- 172.18.32.0 broadcast 172.18.71.255
- 172.18.32.0 broadcast 172.18.80.255
- 172.18.64.0 broadcast 172.18.71.255



  255.255.248.0 -> /21<br>
  32-21=11<br>
  2^11=2048/256 -> 8<br>
  2^(11-8)=2^3=8<br>
<br>
  172.18.71.2 -> 172.18.72.0-1 -> 172.18.71.255 broadcast de subred<br>
  172.18.72-8.0 -> 172.18.64.0 IP de subred<br>
<br>
  `172.18.64.0` - `172.18.71.255` <br>
  
  
  
  
