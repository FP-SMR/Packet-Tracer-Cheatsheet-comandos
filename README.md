# Packet-Tracer-Cheatsheet-comandos

<img width="454" height="358" alt="image" src="https://github.com/user-attachments/assets/08d385fa-e15c-44e2-a05d-6da8ad27bba4" />

---

![Cisco](https://img.shields.io/badge/Cisco-Packet%20Tracer-1BA0D7?logo=cisco&logoColor=white)
![Routing](https://img.shields.io/badge/Routing-RIP%20v2-blue?logo=protocolsio&logoColor=white)
![Static Routes](https://img.shields.io/badge/Static%20Routing-ip%20route-green?logo=googlecloud&logoColor=white)
![CLI](https://img.shields.io/badge/CLI-IOS%20Commands-black?logo=gnubash&logoColor=white)
![Switching](https://img.shields.io/badge/Switching-VLANs-orange?logo=cisco&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-TCP%2FIP-red?logo=cloudflare&logoColor=white)
![Simulation](https://img.shields.io/badge/Simulation-Mode-purple?logo=databricks&logoColor=white)
![Router](https://img.shields.io/badge/Router-Configuration-yellow?logo=serverfault&logoColor=black)
![Switch](https://img.shields.io/badge/Switch-Configuration-success?logo=switch&logoColor=white)
![Packet Tracer](https://img.shields.io/badge/Packet%20Tracer-Network%20Labs-005073?logo=cisco&logoColor=white)



<div align="center">

### Redes Locales • Packet Tracer • FP-SMR

<sub>Hecho con ❤️ por Nicolás Fernández Núñez </sub>

</div>

---

## Comandos clave

Para entrar a **modo privilegio**

```Java
enable
```

Salir al **modo anterior**

```Java
exit
```


Volver directamente al **modo privilegiado** 

```Java
end
```

Ver **privilegios** actuales

```Java
show privilege
```

Entrar en **configuración global**

```Java
configure terminal
```

Ver todas las **acciones posibles** en el modo que estéas

```Java
?
```

**Velocidad** (Modo configuración)

```Java
Speed 100
```

El modo del **puerto** en interfaz Switch

```Java
Switch(config-if)#duplex full
Switch(config-if)#no duplex full
Switch(config-if)#duplex half
```

Para ver la tabla **MAC** de el switch

```Java
show mac-address-table
```

Para ver el estado de las **interfaces de el switch**

```Java
show ip interface brief
```

Para ver las **VLAN definidas y sus puertos**

```Java
sh vlan
```

Cambiar nombre **router / switch** (obligatorio modo configuración + privilegiado)

```Java
Router(config)#hostname R1
R1(config)#
```

Configurar **interfaz IP**

```Java
interface gigabitEthernet 0/0
ip address 192.168.1.1 255.255.255.0
```

Para **apagar interfaz**

```Java
shutdown
```

Para **encender interfaz** 

```Java
no shutdown
```

Para activar protocolo **RIP**

```Java
enable
configure terminal
router rip
version 2
network 192.168.1.0
auto-summary
```


Para entrar en una interfaz

```Java
Interface FastEthernet0/0
```


Para comprobar el **protocolo RIP**

```Java
end
[ENTER]
show ip protocols
```

Añadir nueva **entrada**

```Java
ip route 20.10.0.0 255.255.0.0 200.10.12. 2
```

Verificar la **tabla de enrutamiento**

```Java
show ip route
```

Eliminar la **entrada**

```Java
no ip route 20.10.0.0 255.255.0.0 200.10.12. 2
```

La ayuda de el comando **interface**

```Java
interface ?
```

Para asignar **IP y máscara** a la interfaz

```Java
ip address 192.168.1.1 255.255.255.0
```

Cambiar **descripción a una interfaz**

```Java
description Connected to Customer
```
