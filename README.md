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
Comenzamos a trabajar usando **fdisk** con **sudo** para que nos permita hacer estos cambios y la ruta al dispositivo, luego escriba la letra “d” para poder borrar las particiones, para comprobar que se borraron exitosamente usaremos el comando**” sudo fdisk -l ruta al dispositivo”**  .

![6](https://user-images.githubusercontent.com/88467362/155014425-f7554fdd-e47d-4b72-8d39-ce43d057c2e1.JPG)
![6 1](https://user-images.githubusercontent.com/88467362/155014445-341ff9cd-6f71-48d5-a5e7-981819c0ca9f.JPG)

## 7. Crear en el “usb” tres particiones físicas y una extendida en terminal.
Comenzamos a trabajar usando **fdisk** y la ruta al dispositivo, luego escriba la letra “n” para poder acceder a el apartado de añadir particiones luego escogeremos la letra “ p “ para hacer las particiones primarias, para comprobar que se agregaron exitosamente usaremos el comando**” sudo fdisk -l ruta al dispositivo”**  .

![7](https://user-images.githubusercontent.com/88467362/155019581-12f8c19b-9406-422b-8fdd-373e0d374259.JPG)

![7 1](https://user-images.githubusercontent.com/88467362/155019596-689a6f0a-495e-43c4-b60b-f82efe3376cf.JPG)

## 8. Crear una partición dentro de la partición extendida del “usb” en terminal.
Comenzamos a trabajar usando **fdisk** y la ruta al dispositivo, al ya no haber espacio para otras particiones primarias y/o extendidas el sistema crea una partición lógica y estas son almacenadas en la partición extendida.

![8](https://user-images.githubusercontent.com/88467362/155019652-d27de383-f73e-43ec-aea3-af60e2aa83d3.JPG)

## 9.- Para borrar las particiones desde la aplicación de discos
Tenemos que seleccionar la USB, ya seleccionada la USB tenemos que seleccionar las particiones y borrarlas con el icono de “- “que esta debajo de donde se muestran las particiones justo al lado de los engranes de configuración.

![9](https://user-images.githubusercontent.com/88467362/155019769-6df3e8ec-5032-4dad-8a04-416ed5807126.JPG)


Así tenemos que ir borrando una por una hasta solo dejar una. Ya que tenemos una sola partición tenemos que seleccionarla y apretar el botón de los engranes, una vez adentro tenemos que seleccionar la opción de redimensionar e indicar que esa partición utilice todo el espacio de la USB

![9 2](https://user-images.githubusercontent.com/88467362/155019797-70ccb9d5-d70e-41bc-86e3-5ef3870fc075.JPG)


¡Y listo! Así tendrás una partición que ocupe toda la memoria USB.

![9 3](https://user-images.githubusercontent.com/88467362/155019813-7d0d545a-3b58-47ae-ac4f-b4256fc66fc0.JPG)


## 10. Copiar un archivo .iso de distribución live de linux a la usb por medio del comando "dd".

El primer paso para copiar un archivo .iso de distribución live de Linux es descargar la el .iso de la distribuidora que queramos en este caso fue Ubuntu. 
Imagen de la pagina de Ubuntu.

![image](https://user-images.githubusercontent.com/88467362/155021322-9355e449-c343-4027-bf98-6aa8d4f5483e.png)

Después le cambiamos el nombre al archivo .iso que se descarga para poderlo ubicar más fácil en este caso le pondremos Linux. 
Imagen donde están los archivos descargados.

![image](https://user-images.githubusercontent.com/88467362/155021337-77d04982-cc84-4739-bcea-dc15e555792c.png)

Y por último con el comando “dd” copiamos ese archivo0 a nuestra USB.
Foto 10

![image](https://user-images.githubusercontent.com/88467362/155021360-68b69c58-6c8e-4535-8037-6d93e77446e1.png)



