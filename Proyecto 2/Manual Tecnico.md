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




## Tabla de subnetting organizada por Sedes.

### 1. Sede Occidente (Agencia Regional Comercial)
| VLAN | Área Funcional | Hosts | ID de Red | Máscara (CIDR) | Rango IPs Útiles | Broadcast | Gateway |
|----------|------------|-------|-----------|----------------|------------------|---------| --------|
| 10 | Cajas | 45 | 192.168.20.0 | /26 (255.255.255.192) | .1 - .62 | .63 | .1 |
| 20 | Asesores | 30 | 192.168.20.64 | /27 (255.255.255.224) | .65 - .94 | .95 | .65 |
| 30 | Gerencia | 10 | 192.168.20.96 | /28 (255.255.255.240) | .97 - .110 | .111 | .97 |
| 40 | Seguridad | 12 | 192.168.20.112 | /28 (255.255.255.240) | .113 - .126 | .127 | .113 |

### 2. Sede Norte (Centro de Autorización de Créditos)
| VLAN | Área Funcional | Hosts | ID de Red | Máscara (CIDR) | Rango IPs Útiles | Broadcast | Gateway |
|----------|------------|-------|-----------|----------------|------------------|---------| --------|
| 50 | Análisis | 50 | 192.168.20.128 | /26 (255.255.255.192) | .129 - .190 | .63 | .1 |
| 60 | Auditoria | 25 | 192.168.20.192 | /27 (255.255.255.224) | .193 - .222 | .95 | .65 |
| 70 | Legal | 14 | 192.168.20.224 | /27 (255.255.255.224) | .225 - .238 | .225 | .239 |

### 3. Sede Oriente (Centro Financiero Legado)
| VLAN | Área Funcional | Hosts | ID de Red | Máscara (CIDR) | IP MS1 (Real) | IP MS2 (Real) |Rango IPs Útiles | Broadcast | Gateway |
|----------|------------|-------|-----------|----------------|---------------|---------------| -----------|---------| --------|
| 80 | Bóveda | 40 | 192.168.21.0 | /26 (255.255.255.192) | .2 | .3 | .4 - .62 | .63 | .1 |
| 90 | Plataforma | 60 | 192.168.21.64 | /26 (255.255.255.192) | .66 | .67 | .68 - .126 | .127 | .65 |

### 4. Data Center y Sede Central (Alta Seguridad)
| VLAN | Área Funcional | Hosts | ID de Red | Máscara (CIDR) | Rango IPs Útiles | Broadcast | Gateway |
|----------|------------|-------|-----------|----------------|------------------|---------| --------|
| 10 | Core_BD | 14 | 192.168.21.128 | /28 (255.255.255.192) | .129 - .142 | .143 | .129 |
| 20 | Web_Apps | 28 | 192.168.21.144 | /27 (255.255.255.224) | .145 - .174 | .175 | .145 |
| 30 | NOC | 10 | 192.168.21.176 | /28 (255.255.255.240) | .177 - .190 | .191 | .177 |

## Tabla de direccionamiento de VLANS

| ID VLAN | Nombre | Sede |
|---------|--------|----------------------- |
| 10 | Ventas_Cajas | Occidente |
| 20 | Asesores | Occidente |
| 30 | Gerencia_Local | Occidente |
| 40 | Seguridad_Occ | Occidente |
| 50 | Analistas_Cred | Norte |
| 60 | Auditoria_Norte | Norte |
| 70 | Legal_Norte | Norte |
| 80 | Boveda_Oriente | Oriente |
| 90 | Plataforma_VIP | Oriente |
| 10 | Core_BD | Central/DC |
| 20 | Web_Apps | Central/DC |
| 30 | NOC_Monitoreo | Central/DC |