UNIVERSIDAD DE SAN CARLOS DE GUATEMALA

FACULTAD DE INGENIERIA

REDES DE COMPUTADORAS

CATEDRÁTICO: ING. ESPINO

============================================================================================

  
  <div style="text-align: center;">
    <h1 style="color: White; text-decoration: underline; text-decoration-color: black;" >MANUAL TÉCNICO TAREA 3</h1>
  </div>

============================================================================================

<p align="right">
OTTONIEL FABRICIO VÁSQUEZ PINEDA
<br>
CARNÉ: 202307820
<br>
SECCIÓN A
</p>

<P align="center">GUATEMALA 28 DE Febrero DEL 2026</P>


## **Configuración de switches**

### Para Switch 0
* enable
* config t
* vtp domain Tarea3
* vtp mode server
* vtp password cisco
* vtp version 2
* vlan 10
* name ADMIN
* exit
* vlan 20
* name MERCA
* exit
* vlan 30
* name VENTAS
* exit
* interface fa0/1
* switchport mode trunk
* switchport trunk allowed vlan 10,20,30
* no shutdown
* exit
* interface fa0/2
* switchport mode trunk
* switchport trunk allowed vlan 10,20,30
* no shutdown
* exit
* interface fa0/3
* switchport mode trunk
* switchport trunk allowed vlan 10,20,30
* no shutdown
* exit
* do wr
* exit

### Para Switch 1 (ADMIN)
* enable
* config t
* vtp domain Tarea3
* vtp mode trasnparent
* vtp password cisco
* vtp version 2
* vlan 10
* name ADMIN
* exit
* interface fa0/1
* switchport mode trunk
* switchport trunk allowed vlan 10,20,30
* no shutdown
* exit
* interface fa0/2
* switchport mode access
* switchport access vlan 10
* no shutdown
* exit
* do wr

### Para Switch 2 (VENTAS)
* enable
* config t
* vtp domain Tarea3
* vtp mode client
* vtp password cisco
* vtp version 2
* interface fa0/1
* switchport mode trunk
* switchport trunk allowed vlan 10,20,30
* no shutdown
* exit
* interface fa0/2-4
* switchport mode access
* switchport access vlan 30
* exit
* do wr

### Para switch 3 (MERCA)
* enable
* config t
* vtp domain Tarea3
* vtp mode client
* vtp password cisco
* vtp version 2
* interface fa0/1
* switchport mode trunk
* switchport trunk allowed vlan 10,20,30
* no shutdown
* exit
* interface fa0/2-3
* switchport mode access
* switchport access vlan 20
* exit
* do wr

---

## **Capturas de Comandos**

### SERVER

<p align="center">
 <img src="Capturas/Server.png" widt>
</p>

### ADMIN

<p align="center">
 <img src="Capturas/Admin.png" widt>
</p>

### VENTAS

<p align="center">
 <img src="Capturas/Ventas.png" widt>
</p>

### MERCA

<p align="center">
 <img src="Capturas/Merca.png" widt>
</p>


---


## **Capturas de PINGS**

### ADMIN

<p align="center">
 <img src="Capturas/Admin1.png" widt>
</p>

### MERCA

<p align="center">
 <img src="Capturas/Merca1.png" widt>
</p>

<p align="center">
 <img src="Capturas/Merca2.png" widt>
</p>

### VENTAS

<p align="center">
 <img src="Capturas/Ventas1.png" widt>
</p>

<p align="center">
 <img src="Capturas/Ventas2.png" widt>
</p>


<p align="center">
 <img src="Capturas/Ventas3.png" widt>
</p>