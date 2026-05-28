# Packet-Tracer-Cheatsheet-comandos

<img width="454" height="358" alt="image" src="https://github.com/user-attachments/assets/08d385fa-e15c-44e2-a05d-6da8ad27bba4" />





## Comandos clave

---

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

Entrar en **configuración global**

```Java
configure terminal
```

Ver todas las acciones posibles en el modo que estéas

```Java
?
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
configure terminal
router rip
version 2
network 192.168.1.0
auto-summary
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

```
no ip route 20.10.0.0 255.255.0.0 200.10.12. 2
```
