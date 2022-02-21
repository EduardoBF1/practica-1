# practica-1
En esta práctica observaremos el manejo de discos con comandos dentro de la terminal de Linux.

2. Para poder montar y desmontar un disco externo en linix primero tenemos que observar si el disco está montado con el comando de **"lsblk"** si esta mondado lo podremos desmontar con el comando de **"umount seguido de la dirección en donde se encuentra el disco"** como se muestra en la imagen siguiente.
![1](https://user-images.githubusercontent.com/88467362/155009044-10d79196-d6a6-4fcd-93ab-6bd65fb87344.JPG)

      para poder verificar si se desmonto correctamente utilizaremos el comando de **"lsblk"** 
![1 2](https://user-images.githubusercontent.com/88467362/155009343-f925f4c9-97e0-4831-a1c1-83143643ba3b.JPG)

      Para poder montar el disco usaremos el comando de **mount** después deberemos especificar el tipo de archivo que es (vfat) para     ello usaremos el parámetro **-t** seguiremos con la partición que queremos montar y en que carpeta se encuentra. verificamos que si se montó correctamente.
![1 3 con permisos](https://user-images.githubusercontent.com/88467362/155010123-7a8ffb9b-e8e1-484a-9269-dd46be71d27c.JPG)

3. Para poder enlistar los dispositivos de bloque que se encuentran conectados lo podremos mostrar en terminal con el comando de **”lsblk”**.
 
![3](https://user-images.githubusercontent.com/88467362/155010937-371a0ee7-0e80-4fd8-a988-378cef3e5d59.JPG)

4. Si desea observar la tabla de particiones del disco en el que contiene el sistema operativo, en terminal se pondrá el comando de **”blkid”**.

![4](https://user-images.githubusercontent.com/88467362/155012102-4e1e34f0-e064-4837-b738-825c523413bf.JPG)

5. Para observar la tabla de particiones de la “usb” , en terminal se pondrá en comando de **” sudo”** este comando nos permite tener permisos para obtener esta información seguido de los comandos **”fdisk -l con la dirección del archivo que se desea”**.

![5](https://user-images.githubusercontent.com/88467362/155012266-a54fed7d-061e-4341-9a30-0eb93bf7baa4.JPG)



