Grupo de Seguridad para un Servidor Web

```
Inbound Rules:
- HTTP (TCP, 80) from 0.0.0.0/0
- HTTPS (TCP, 443) from 0.0.0.0/0
- SSH (TCP, 22) from 203.0.113.0/32

Outbound Rules:
- All traffic (ALL, ALL) to 0.0.0.0/0
```

Grupo de Seguridad para una Base de Datos MySQL

```
Inbound Rules:
- MySQL/Aurora (TCP, 3306) from 10.0.0.0/16 (supongamos que la base de datos solo debe ser accesible desde una subred específica)

Outbound Rules:
- All traffic (ALL, ALL) to 0.0.0.0/0
```

#### Grupo de Seguridad para una Aplicación Multi-Tier

- **Web Tier**: Servidor web accesible públicamente

```
Inbound Rules:
- HTTP (TCP, 80) from 0.0.0.0/0
- HTTPS (TCP, 443) from 0.0.0.0/0
- SSH (TCP, 22) from 203.0.113.0/32

Outbound Rules:
- All traffic (ALL, ALL) to 0.0.0.0/0
```

- **App Tier**: Servidor de aplicaciones solo accesible desde el Web Tier

```
Inbound Rules:
- Custom TCP (TCP, 8080) from sg-xxxxxxxx (ID del grupo de seguridad del Web Tier)

Outbound Rules:
- All traffic (ALL, ALL) to 0.0.0.0/0
```

- **Database Tier**: Base de datos solo accesible desde el App Tier

```
Inbound Rules:
- MySQL/Aurora (TCP, 3306) from sg-yyyyyyyy (ID del grupo de seguridad del App Tier)

Outbound Rules:
- All traffic (ALL, ALL) to 0.0.0.0/0
```

