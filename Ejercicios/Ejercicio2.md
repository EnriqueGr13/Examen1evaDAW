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
