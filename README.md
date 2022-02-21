# practica-1
En esta práctica observaremos el manejo de discos con comandos dentro de la terminal de Linux.

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
Comenzamos a trabajar usando **fdisk**  y la ruta al dispositivo, luego escriba la letra “d” para poder borrar las particiones, para comprobar que se borraron exitosamente usaremos el comando**” sudo fdisk -l ruta al dispositivo”**  
![6](https://user-images.githubusercontent.com/88467362/155014425-f7554fdd-e47d-4b72-8d39-ce43d057c2e1.JPG)
![6 1](https://user-images.githubusercontent.com/88467362/155014445-341ff9cd-6f71-48d5-a5e7-981819c0ca9f.JPG)

## 7. Crear en el “usb” tres particiones físicas y una extendida en terminal.
Comenzamos a trabajar usando **fdisk** y la ruta al dispositivo, luego escriba la letra “n” para poder acceder a el apartado de añadir particiones luego escogeremos la letra “ p “ para hacer las particiones primarias, para comprobar que se agregaron exitosamente usaremos el comando**” sudo fdisk -l ruta al dispositivo”**  

![7](https://user-images.githubusercontent.com/88467362/155016110-7c4e4930-ff19-4da2-bc58-0a6055ed77ff.JPG)
![7 1](https://user-images.githubusercontent.com/88467362/155016121-1dc674a6-aa49-4bcd-807c-8f3a7a879775.JPG)

## 8. Crear una partición dentro de la partición extendida del “usb” en terminal.






