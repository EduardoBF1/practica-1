# practica-1
En esta práctica observaremos el manejo de discos con comandos dentro de la terminal de Linux.

## 1. Identificar y describir las diferencias entre hda, sda y vda, además explicar que significa la letra y el numero al final de los identificadores.

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
Comenzamos a trabajar usando **fdisk** y la ruta al dispositivo, luego escriba la letra “n” para poder acceder a el apartado de añadir particiones luego escogeremos la letra “ p “ para hacer las particiones primarias, para comprobar que se agregaron exitosamente usaremos el comando**” sudo fdisk -l ruta al dispositivo”**  

![7](https://user-images.githubusercontent.com/88467362/155017866-5890e1c3-869a-4fd2-ab81-1a70f2c38c87.JPG)
![7 1](https://user-images.githubusercontent.com/88467362/155017888-5d0af8ff-0efe-4cea-b1a0-ba8a86a944c8.JPG)

## 8. Crear una partición dentro de la partición extendida del “usb” en terminal.
Comenzamos a trabajar usando **fdisk** y la ruta al dispositivo, al ya no haber espacio para otras particiones primarias y/o extendidas el sistema crea una partición lógica y estas son almacenadas en la partición extendida.

![8](https://user-images.githubusercontent.com/88467362/155017999-2696447a-0fea-4d31-a2de-4f012675e69f.JPG)
## 9. En la interfaz gráfica de la aplicación disks, borrar las particiones para que sólo exista una partición que abarque toda la “usb”.
Tenemos que seleccionar las particiones y borrarlas con el icono de “- “que esta debajo de donde se muestran las particiones justo al lado de los engranes de configuración.

![9](https://user-images.githubusercontent.com/88467362/155018551-bc326aec-3310-4595-9799-d322f3a24005.JPG)

Así tenemos que ir borrando una por una hasta solo dejar una. Ya que tenemos una sola partición tenemos que seleccionarla y apretar el botón de los engranes, una vez adentro tenemos que seleccionar la opción de redimensionar e indicar que esa partición utilice todo el espacio de la USB

![9 2](https://user-images.githubusercontent.com/88467362/155018584-7a21b793-a511-4fef-96c5-17c8aa511b06.JPG)

¡Y listo! Así tendrás una partición que ocupe toda la memoria USB.

![9 3](https://user-images.githubusercontent.com/88467362/155018606-c979be26-adc4-448e-8457-1aea670f5cbd.JPG)

## 10. Copiar un archivo .iso de distribución live de linux a la usb por medio del comando "dd".



