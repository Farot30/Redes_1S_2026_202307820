UNIVERSIDAD DE SAN CARLOS DE GUATEMALA

FACULTAD DE INGENIERIA

REDES DE COMPUTADORAS

CATEDRÁTICO: ING. ESPINO

============================================================================================

  
  <div style="text-align: center;">
    <h1 style="color: White; text-decoration: underline; text-decoration-color: black;" >MANUAL TÉCNICO NetCore Academy</h1>
  </div>

============================================================================================

<p align="right">
OTTONIEL FABRICIO VÁSQUEZ PINEDA
<br>
CARNÉ: 202307820
<br>
SECCIÓN A
</p>

<P align="center">GUATEMALA 19 DE MARZO DEL 2026</P>

## Topologías Completas

1. Topología Completa

<p align="center">
 <img src="Imagenes/Topología_Completa.PNG" widt>
</p>

  1.2. Topología por Áreas

* Edificio A:

<p align="center">
 <img src="Imagenes/Topología_A.PNG" widt>
</p>

* Edificio B:

<p align="center">
 <img src="Imagenes/Topología_B.PNG" widt>
</p>

* Edificio C:

<p align="center">
 <img src="Imagenes/Topología_C.PNG" widt>
</p>

* Eidifcio D:

<p align="center">
 <img src="Imagenes/Topología_D.PNG" widt>
</p>


## Segmentos: Interfaces y Medios de Transmisión

| Segmento (Conexión) | Tipo de Interfaz | Medio de Transmisión |
|---------------------|------------------|----------------------|
| Switches Inter-Edificios | GigabitEthernet / FastEthernet | Fibra Óptica |
| Switches Intra-Edificio | GigabitEthernet / FastEthernet | Cable de Cobre (UTP Cat 6) |
| Switch a PCs / Laptops | FastEthernet | Cable de Cobre (UTP Cat 5e/6) |
| Switch a Servidor Web | FastEthernet | Cable de Cobre (UTP Cat 6) |
| Switch a Access Points (APs) | FastEthernet/Port | Cable de Cobre (UTP Cat 6) |
| Switch a Repetidor | FastEthernet/Ethernet | Cable de Cobre (UTP Cat 6) |
| Switch a Hub-PT | GigabitEthernet | Cable de Cobre (UTP Cat 6) |
| Access Point a Laptops/Smartphones | IEEE 802.11 (WLAN) | Ondas de Radio (Inalámbrico) |


<p align="center">
 <img src="Imagenes/Medio_transmision.PNG" widt>
</p>

## Tabla de Dominios de Colisión

| Área / Edificio | Cantidad de Dominios | Descripción | 
|-----------------|----------------------|------------- |
| Edificio A | 10 | Puertos de acceso a PCs y troncales a otros switches. |
| Edificio B | 10 | Puertos de acceso a PCs y troncales. |
| Edificio C | 10 | Puertos de acceso y puntos de acceso inalámbricos. |
| Edificio D | 12 | Puertos de Laboratorio, Access Point de Visitantes y troncales. |

## Tabla de Dominios de Broadcast

| Vlan ID | Nombre | Dispositivos Incluidos |
|---------|--------|----------------------- |
| 10 | Estudiantes | Lógica de la VLAN 10 en toda la red |
| 20 | Catedráticos | Lógica de la VLAN 20 en toda la red |
| 30 | Administración | Lógica de la VLAN 30 en toda la red |
| 40 | WiFi_Invitados | Lógica de la VLAN 40 en Edificio D |
| 99 | Nativa/Gestión | Tráfico de control y gestión |

## Tabla de IPS asignadas

| Edificio | Nombre Area | Tipo de dispositivos | ips|
|----------|-------------|----------------------|----|
| A | Admin2 | Computadora | 192.168.10.2 |
| A | Docencia1 | Smartphone | 192.168.20.1 |
| A | Docencia2 | Laptop | 192.168.20.2 |
| A | Docencia3 | Laptop | 192.168.20.3 |
| A | Laboratorio2 | Computadora | 192.168.40.2 |
| A | Laboratorio4 | Computadora | 192.168.40.4 |
| B | Admin1 | Laptop | 192.168.10.1 |
| B | Docencia6 | Laptop | 192.168.20.6 |
| B | Biblioteca1 | Computadora | 192.168.30.1 | 
| B | Biblioteca2 | Laptop | 192.168.30.2 |
| B | Biblioteca3 | Computadora | 192.168.30.3 |
| B | Biblioteca4 | Computadora | 192.168.30.4 |
| B | Biblioteca5 | Computadora | 192.168.30.5 |
| C | Admin3 | Computadora | 192.168.10.3 |
| C | Docencia7 | Laptop | 192.168.20.7 |
| C | Docencia8 | Computadora | 192.168.20.8 |
| C | Docencia9 | Computadora | 192.168.20.9 |
| C | Biblioteca6 | Computadora | 192.168.30.6 |
| D | Admin4 | Computadora | 192.168.10.4 |
| D | Admin5 | Computadora | 192.168.10.5 |
| D | Docencia10 | Servidor | 192.168.20.10 |
| D | Biblioteca7 | Computadora | 192.168.30.7 |
| D | Laboratorio3 | Computadora | 192.168.40.3 |
| D | Visitantes1 | Computadora | 192.168.50.1 |
| D | Visitantes2 | Computadora | 192.168.50.2 |
| D | Visitantes3 | Copmutadora | 192.168.50.3 |


## Tabla de direccionamiento de VLANS

| ID VLAN | Nombre | Uso / Área |
|---------|--------|----------------------- |
| 10 | ADMIN | Administración |
| 20 | DOCENTES | Docencia |
| 30 | BIBLIOTECA | Biblioteca |
| 40 | LABORATORIO | Laboratorio |
| 50 | VISITANTE | Visitante |


## Presupuesto

### Equipo de Networking (Switches y Acceso)

| Cantidad | Descripción | Precio Unitario | Total |
|----------|-------------|-----------------|-------|
| 9 | Switch Cisco Catalyst 2960-24TT | Q 1,239 | Q 11,151 |
| 8 | Switch-PT | Q 115 | Q 920 |
| 2 | Hub-PT | Q 450 | Q 900 |
| 1 | Repeater-PT | Q 350 | Q 350 |
| 2 | Access Point | Q 1,200 | Q 2,400 |

### Dispositivos Finales

| Cantidad | Descripción | Precio Unitario | Total |
|----------|-------------|-----------------|-------|
| 18 | Computadoras de Escritorio (i5/8GB/SSD) | Q 4,800 | Q 86,400 |
| 6 | Laptops (i5/16GB/SSD) | Q 4,500 | Q 27,000 |
| 1 | Servidor (Xeon/32GB/2TB) | Q 18,500 | 18,500 |
| 1 | Smartphone (Gama Media para pruebas) | 1,800 | 1,800 |

### Cableado y Medios de Transmisión

| Cantidad | Descripción | Precio Unitario | Total |
|----------|-------------|-----------------|-------|
| 4 | Bobinas de Cable UTP Cat6 | Q 1,100 | Q 4,400 |
| 5 | Jumpers de Fibra Óptica | Q 250 | Q 1,250 |
| 1 | Lote de Conectores RJ45 y SFP | Q 1,500 | Q 1,500 |
