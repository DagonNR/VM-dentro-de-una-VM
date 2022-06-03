# Creación de Virtual Machine dentro de una Virtual Machine en Azure

Esto es un recopilatorio sobre como crear una Virtual Machine en Azure, y además el como crear otra Virtual Machine y ejecutarla desde la primera Virtual Machine.

![Microsoft Azure Virtual Machine Logo](imagenes\Azure-VM-Logo.png)

---

## Requisitos
- Cuenta en [Microsoft Azure](portal.azure.com)
- Un dispositivo, por ejemplo una computadora
- Acceso a internet

---

## Pasos a seguir

- Primero entramos en [Microsoft Azure](portal.azure.com), y nos vamos al apartado de Virtual Machines.
![P1](imagenes\P1.png)

- Luego creamos lo que sería la primera Virtual Machine, en el apartado de "Crear".
![P2](imagenes\P2.png)

- Clicamos en "Máquina Virtual de Azure".
![P3](imagenes\P3.png)

- Nos saldran varias opciones, en este caso se creo con el sistema operativo de Windows 10.
![P4](imagenes\P4.png)

- Después nos vamos al apartado de "Revisar y crear" y si todo esta bien, le damos clic en "Crear"
![P5](imagenes\P5.png)

- Después nos redireccionará a algo parecido a la siguiente imagen, nos tocará esperar unos pocos minutos (dependiendo de tu conexión a internet).
![P6](imagenes\P6.png)

- Una vez finalizado, si todo sale bien, aparecerá lo siguiente.
![P7](imagenes\P7.png)

- Hasta aquí tendríamos creada la primera Virtual Machine, entonces solo queda crear la segunda, vamos a repetir los anteriores pasos nuevamente para crearla.
![P8](imagenes\P8.png)

- Luego de tener creada la segunda Virtual Machine, lo que sigue es conectarnos con la primera Virtual Machine. Entonces vamos al "Grupo de recursos" donde se encuentra la primera Virtual Machine y nos vamos al apartado de "Conectar", en este caso lo haremos por "RDP".
![P9](imagenes\P9.png)

- Para conectarnos por "RDP", le damos clic en "Descargar archivo RCP" y lo ejecutamos, despues nos pedira la cuenta y contraseña que pusimos al crear la Virtual Machine, y entraríamos en ella.
![P10](imagenes\P10.png)

- Ahora para poder abrir la Virtual Machine, dentro de la Virtual Machine, debemos abrir "Windows PowerShell", importante ejecutar como Administrador, y aparecera lo siguiente.
![P11](imagenes\P11.png)

- Entonces escribimos lo siguiente tal cual: New-NetFirewallRule –DisplayName “Allow ICMPv4-In” -Protocol ICMPv4 después nos aparecerá el siguiente mensaje.
![P12](imagenes\P12.png)

- Ahora lo que sigue es buscar la "Dirección IP Privada" de la segunda Virtual Machine. Después de encontrarlo dentro del "Windows PowerShell" pondremos: mstsc /v:AQUI PONEMOS LA IP PRIVADA y si sale bien nos pedirá la cuenta y contraseña de la segunda Virtual Machine.
![P13](imagenes\P13.png)

- Con esto ya tendríamos ejecutada la Virtual Machine dentro de otra Virtual Machine.
![P14](imagenes\P14.png)