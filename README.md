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

Mostrar los **cambios de configuración** hasta el momento

```Java
sh run
```

Para **copiar** lo que hemos estado haciendo

```Java
copy run start
```

# Boletín 1 Protocolo DHCP (Dynamic Host Configuration Protocol)

```Java
Ejercicio 1. ¿Para qué sirve DHCP?

Imagina que en tu aula hay 25 ordenadores y todos necesitan conectarse a Internet. El profesor te plantea dos escenarios:
    • Escenario A: configuras manualmente la IP, la máscara, la puerta de enlace y el DNS en cada uno de los 25 equipos.
    • Escenario B: instalas un servidor DHCP en la red para que los equipos se configuren automáticamente.
Responde:
    1. ¿Cuál de los dos escenarios crees que es más rápido? ¿Por qué?
    2. Indica dos problemas que pueden aparecer en el Escenario A si dos alumnos eligen la misma IP.
    3. ¿En qué tipo de redes crees que sigue siendo razonable configurar IP manualmente?
```

1) El escenario más rápido es el **B** sin duda alguna, son muchos equipos para hacerlo manual, DHCP asigna los parámetros de red automáticamente.
   
2) Los dos ordenadores pueden perder la conexión, o funcionar de forma inestable, prácticamente nulo. Con recursos externos como internet habrá problemas por que si usan la misma IP no sabe a quien mandar los datos.

3) En redes que haya pocos equipos como en una red doméstica. O algunas que necesitan usar siempre la misma IP como cámaras de seguridad por ejemplo.

```Java
Ejercicio 2. Asocial

Concepto	Definición
1. Servidor DHCP	A. Tiempo durante el que un equipo puede usar la IP que se le ha entregado.
2. Cliente DHCP	B. Rango de direcciones IP que el servidor puede repartir.
3. Concesión (lease)	C. Equipo que solicita configuración de red automática.
4. Ámbito (scope)	D. Equipo que entrega configuración IP a otros equipos.
5. Reserva	E. Asociación fija entre una MAC y una IP concreta dentro del ámbito.

```

1.- **Servidor DHCP** --> D. Equipo que entrega configuración IP a otros equipos.

2.- **Cliente DHCP** --> C. Equipo que solicita configuración de red automática.

3.- **Concesión** (lease) --> A. Tiempo durante el que un equipo puede usar la IP que se le ha entregado.

4.- **Ámbito** (scope) --> B. Rango de direcciones IP que el servidor puede repartir.

5.- **Reserva** --> E. Asociación fija entre una MAC y una IP concreta dentro de el ámbito.

