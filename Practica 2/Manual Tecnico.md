UNIVERSIDAD DE SAN CARLOS DE GUATEMALA

FACULTAD DE INGENIERIA

REDES DE COMPUTADORAS

CATEDRÁTICO: ING. ESPINO

============================================================================================

  
  <div style="text-align: center;">
    <h1 style="color: White; text-decoration: underline; text-decoration-color: black;" >MANUAL TÉCNICO Red de Hospitales Metropolitanoy</h1>
  </div>

============================================================================================

<p align="right">
OTTONIEL FABRICIO VÁSQUEZ PINEDA
<br>
CARNÉ: 202307820
<br>
SECCIÓN A
</p>

<P align="center">GUATEMALA 10 DE MARZO DEL 2026</P>


## Tabla de subnetting organizada por área.

| Area | VLAN | Máximo de Hots | Red | Máscara(Decimal) | CIDR | Gateway |
| -----|-------|---------------|-----|-------------------|----|----------|
| Quirófanos | 10 | 63 (H1) | 192.168.20.0 | 255.255.255.128 | /25 | 192.168.20.1 |
| Admin. | 30 | 32 (H3) | 192.168.20.128 | 255.255.255.192 | /26 | 192.168.20.129 |
| UCI |  20 | 26 (H5) |  192.168.20.192 | 255.255.255.224 | /27 | 192.168.20.193 |
| Emergencias | 40 | 25 (H2) | 192.168.20.224 | 255.255.255.224 | /27 | 192.168.20.225 |
| Consultas | 50 | 15 (H4) | 192.168.21.0 | 255.255.255.255.240 | /28 | 192.168.21.1 |