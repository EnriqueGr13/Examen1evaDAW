
# **Ejercicio 1**
Test
# **Ejercicio 2 examen**

## Paso 1: Acceder a la máquina remota mediante SSH
``` bash
ssh usuario@192.168.0.148 
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio2/cap1.png "Captura1")
## Paso 2: Ir al escritorio
``` bash
cd Escritorio
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio2/cap2.png "Captura2")
## Paso 3: Crear un archivo de texto con tu nombre y apellidos como nombre de archivo
``` bash
touch enriquegallenroda.txt
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio2/cap3.png "Captura3")
## Paso 4: Escribir en el archivo el resultado de whoami
``` bash
whoami > enriquegallenroda.txt
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio2/cap4.png "Captura4")
## Paso 5: Concatenar al final del archivo el resultado del comando para saber quién está conectado por SSH
``` bash
echo "Usuarios conectados por SSH: $(who)" >> enriquegallenroda.txt
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio2/cap5.png "Captura5")
## Resumen de los comandos utilizados:
``` bash
ssh usuario@192.168.0.148
cd Escritorio
touch enriquegallenroda.txt
whoami > enriquegallenroda.txt
echo "Usuarios conectados por SSH: $(who)" >> enriquegallenroda.txt
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio2/resultadoFinal.png "Captura resultado final")

[Enlace](https://github.com/EnriqueGr13/Examen1evaDAW/tree/main/Capturas/Capturas%20Ejercicio2) a la carpeta del repositorio de GitHub donde se encuentran todas las capturas.

# **Ejercicio 3 examen**

## Paso 1: Abrir el archivo de configuración de Apache
``` bash
sudo nano /etc/apache2/sites-available/daw_ejercicio3.conf
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt1.png "Captura1")
## Paso 2: Agregar la configuración del virtualhost
``` bash
<VirtualHost *:80>
    ServerAdmin webmaster@localhost
    ServerName daw.ejercicio3.com
    ServerAlias www.daw.ejercicio3.com
    DocumentRoot /var/www/www.ejericico3.daw

    <Directory /var/www/www.ejericico3.daw>
        Options Indexes FollowSymLinks
        AllowOverride All
        Require all granted
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log
    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt2.png "Captura2")
## Paso 3: Guardar y cerrar el archivo
Guardar y cerrar el archivo

## Paso 4: Habilitar el nuevo virtualhost
``` bash
sudo a2ensite daw_ejercicio3.conf
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt4.png "Captura4")
## Paso 5: Reiniciar Apache para aplicar los cambios
``` bash
sudo service apache2 restart
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt3.png "Captura5")

## Paso 6: Configuración del archivo hosts
Abre el archivo hosts para asignar la dirección IP local al dominio.
``` bash
sudo nano /etc/hosts
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt5.png "Captura6.1")
Agrega la siguiente línea al final del archivo.
``` bash
127.0.0.1   daw.ejercicio3.com
```
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt6.png "Captura6.2")
##Paso 7: Añadimos el index.html
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/capt7.png "Captura7")
## Resultado en la web
![Captura](https://github.com/EnriqueGr13/Examen1evaDAW/blob/main/Capturas/Capturas%20Ejercicio3/web.png "Captura resultado final")

[Enlace](https://github.com/EnriqueGr13/Examen1evaDAW/tree/main/Capturas/Capturas%20Ejercicio3) a la carpeta del repositorio de GitHub donde se encuentran todas las capturas.

[Repositorio GitHub](https://github.com/EnriqueGr13/Examen1evaDAW)
