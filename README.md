# practica-1
En esta práctica observaremos el manejo de discos con comandos dentro de la terminal de Linux.

## 1. Identificar y describir las diferencias entre hda, sda y vda, además explicar que significa la letra y el numero al final de los identificadores.

La diferencia entre hda, sda y vda es que sda se le asigna a un disco SCSI, que es una interface de pequeños sistemas informáticos que puede ser una USB, mientras que al vda que significa agente de entrega virtual, se le asigna a un controlador permita una conexión una máquina y un dispositivo personal y hda se le asigna a un disco maestro en el controlador IDE que permite la conexión a diferentes dispositivos internos.
Todas estas denominaciones aparecen como entradas en el directorio /dev.
El sda es el nombre que se le da al primer disco que la maquina detecta y la última letra se ira cambiado por orden alfabetico cada vez que se detecte un disco, por lo que, el primer disco que detecte le pondrá de nombre sda, el segundo disco que detecte lo llamara sdb y asi sucesivamente y se le asignara un numero al final que indica el número de partición del disco por ejemplo sda1, sda2, sda3, etc.
El vda puede acceder a aplicaciones virtuales de Linux en cualquier momento y en cualquier dispositivo con la ayuda de la aplicación Citrix Workspace.
En el caso de hda, Linux reconoce un disco duro como completo y cada partición se le asignara un numero que va al final por ejemplo hda1, hd2, hd3, etc.
Las siglas vda significa virtual Delivery Agent en ingles, las siglas sda significa disco SCSI que significa Interface de Sistemas Pequeños de Información, mientras que hda es el controlador IDE que significa Integrated Drive Electronics.


## 2. Para poder montar y desmontar un disco externo en linix.
Primero tenemos que observar si el disco está montado con el comando de **"lsblk"** si esta mondado lo podremos desmontar con el comando de **"umount seguido de la dirección en donde se encuentra el disco"** como se muestra en la imagen siguiente.

![1](https://user-images.githubusercontent.com/88467362/155009044-10d79196-d6a6-4fcd-93ab-6bd65fb87344.JPG)

   para poder verificar si se desmonto correctamente utilizaremos el comando de **"lsblk"** 
      
![1 2](https://user-images.githubusercontent.com/88467362/155009343-f925f4c9-97e0-4831-a1c1-83143643ba3b.JPG)

   Para poder montar el disco usaremos el comando de **mount** después deberemos especificar el tipo de archivo que es (vfat) para     ello usaremos el parámetro **-t** seguiremos con la partición que queremos montar y en que carpeta se encuentra. verificamos que si se montó correctamente.
      
![1 3 con permisos](https://user-images.githubusercontent.com/88467362/155010123-7a8ffb9b-e8e1-484a-9269-dd46be71d27c.JPG)

## 3. Para poder enlistar los dispositivos de bloque que se encuentran conectados. 
Lo podremos mostrar en terminal con el comando de **”lsblk”**.
 
![3](https://user-images.githubusercontent.com/88467362/155010937-371a0ee7-0e80-4fd8-a988-378cef3e5d59.JPG)

## 4. Si desea observar la tabla de particiones del disco en el que contiene el sistema operativo.
En terminal se pondrá el comando de **”blkid”**.

![4](https://user-images.githubusercontent.com/88467362/155012102-4e1e34f0-e064-4837-b738-825c523413bf.JPG)

## 5. Para observar la tabla de particiones de la “usb”. 
En terminal se pondrá en comando de **” sudo”** este comando nos permite tener permisos para obtener esta información seguido de los comandos **”fdisk -l con la dirección del archivo que se desea”**.

![5](https://user-images.githubusercontent.com/88467362/155012266-a54fed7d-061e-4341-9a30-0eb93bf7baa4.JPG)

## 6. Boorar todas las particiones de una usb en terminal.
Comenzamos a trabajar usando **fdisk** con **sudo** para que nos permita hacer estos cambios y la ruta al dispositivo, luego escriba la letra “d” para poder borrar las particiones, para comprobar que se borraron exitosamente usaremos el comando**” sudo fdisk -l ruta al dispositivo”**  
![6](https://user-images.githubusercontent.com/88467362/155014425-f7554fdd-e47d-4b72-8d39-ce43d057c2e1.JPG)
![6 1](https://user-images.githubusercontent.com/88467362/155014445-341ff9cd-6f71-48d5-a5e7-981819c0ca9f.JPG)

## 7. Crear en el “usb” tres particiones físicas y una extendida en terminal.


## 11. Referencias.

C.4. Nombres de dispositivos en Linux. (s. f.). Debian. Recuperado 20 de febrero de 2022, de https://www.debian.org/releases/stable/armel/apcs04.es.html
A. (2021, 24 septiembre). Preguntaste: ¿Qué es Linux VDA? CompuHoy.com. Recuperado 20 de septiembre de 2022, de https://www.compuhoy.com/preguntaste-que-es-linux-vda/
Suárez, R. (2021). FUSE: todo es un fichero. Dialnet. Recuperado 20 de febrero de 2022, de https://dialnet.unirioja.es/servlet/articulo?codigo=3208255




