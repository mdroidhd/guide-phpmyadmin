
# Pasos

## Paso 1 
Actualizamos las librerias.
```
sudo apt update
```
## Paso 2
Instalamos mysql.
```
sudo apt install mysql-server
```
Iniciamos el servicio.
```
sudo service mysql start
```
Comprobamos que se haya iniciado.
```
sudo service mysql status
```
``PD``: Debe aparecer en verde todo.
## Paso 3
Instalacion de phpmyadmin
```
sudo apt install phpmyadmin
```
![paso de mysql](https://github.com/mdroidhd/guide-phpmyadmin/blob/main/img/mysql-step-1.png)

En las pantallas que salgan, deberemos marcar la casilla apache (el la tecla ```ESPACIO```) luego presionamos ```ENTER```.
El resto de pasos les pedira una contraseña para el mysql y el resto sera darle ```OK``` a todo.
``PD``: Nos movemos en la interfaz con las flechas (```← →↑↓```)

## Paso 4
Ahora vamos cambiar la contraseña del root en el phpmyadmin, para ello entramos a la linea de comando de ```MYSQL```.
```
sudo mysql 
```
Una vez dentro ponemos los siguiente comandos:
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'tu_contraseña';
```

``PD``: donde dice ```tu_contraseña``` poner la que vosostros querais.
Luego aplicamos los cambios
```
FLUSH PRIVILEGES;
```
Salimos del la terminal de ``MYSQL``
```
EXIT;
```
### Verficación
#### Comprobamos que la contraseña se haya cambiado
Escribimos la contrañea que creamos en el [Paso 4](https://github.com/mdroidhd/guide-phpmyadmin/blob/main/README.md#Paso-4) y nos deberia de dejar entrar.

``PD``: La contraseña no se ve cuando se escribe.
```
mysql -u root -p
```
## Paso 5 FINAL

Ahora vamos a nuestro navegador y escribimos
```
http://[IP_PUBLICA o NOMBRE_DOMINIO]/phpmyadmin
```
### Ejemplo:
```
https://dam09jesuitas2024.mhdflix.com/phpmyadmin/
```

Para acceder ponemos:

``Usuario``: root

``Contraseña``: [Paso 4](https://github.com/mdroidhd/guide-phpmyadmin/blob/main/README.md#Paso-4)


## Autores

- [@Mibrahim0001](https://github.com/Mibrahim0001)
### Conejillos de indias
- [@ElViero7](https://github.com/ElViero7/) (Javier)
- [@Imarcosr01](https://github.com/Imarcosr01/) (Isaac)
