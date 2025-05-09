# 1dam_subnetting
## Daniel Rodríguez Pérez
Ejercicios de subnetting

### Crear 4 subredes desde la red 192.168.1.0/24
Buscar un número elevado a 2 que de 4

2^2=4 /24+2 = /26
/32 -> límite de máscara
/32-/26 = 6

2^6= 64 número mágico

- 192.168.1.0/26
- 192.168.1.64/26
- 192.168.1.128/26
- 192.168.1.192/26


---------------------------------------------

### Crear 8 subredes desde la red 192.168.1.0/24
Buscar un número elevado a 2 que de 8
2^3=8 -> /24+3 = /27


/32-/27 = 5
2^5=32

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
Red -> 10101100.00010000.00000000.00000000
Máscara-> 11111111.11111111.00000000.00000000

Red -> 172.16.0.0
Máscara-> 255.255.0.0
Buscar un número elevado a 2 mayor o igual
a 10
2^3 = 8
2^4 = 16 -> usaremos 10

/16+4 -> /20

32-20 = 12

2^12 = 4096

12>8

12-8 = 4 (al ser superior que 8, omitimos el segundo octeto, trabajaremos en el nivel superior)

2^4 = 16 -> número mágico

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

192.223.50.0 -> `255.255.255.128`

Dirección de BROADCAST -> `192.223.50.127`


