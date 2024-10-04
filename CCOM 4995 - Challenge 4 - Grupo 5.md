Carlos Aparicio Mestra  
Ian M. Pérez López  
Ramón E. Miranda Calderón  
CCOM 4995: Desarrollo de Vídeo Juegos
Grupo 5

# Challenge 4: Bullet Time
  En este challenge implementamos scripts y visual graphs en nuestro proyecto que nos permiten: 
  Mover al personaje y poder implementar el efecto de disparar. 
  Se creo un prefab que funciona como bala y el personaje fue descargado del asset store.

# Character Rotation

## Código
En la implementación en C#, definimos una variable pública de tipo float llamada **speedRotation** que determina qué tan rápido     girará el personaje. Después de manejar la lógica de movimiento, capturamos el movimiento en el eje X desde la entrada del ratón y   lo aplicamos a la rotación en el eje Y del personaje. Esto permite que el personaje gire en respuesta al movimiento del ratón,     mejorando nuestro control sobre la orientación del personaje en el mundo del juego.

![image](https://github.com/user-attachments/assets/ade2ba08-d8e4-4b94-86a9-5b976a0b7b03)

## Gráfica
En la implementación en la gráfica, creamos una variable de tipo float llamada **speedRotation** y le asignamos un valor. Luego, traducimos las instrucciones de C# en nodos gráficos, lo que implica usar nodos para manipular la rotación del personaje basándonos en la entrada del ratón. Esta configuración permite una representación visual de la lógica, donde los nodos gráficos manejan la rotación de manera similar al código en C#, asegurando que el personaje responda a nuestra entrada.

![image](https://github.com/user-attachments/assets/d95a8894-1a16-436a-a84a-2362874dfda2)

## Bullet Prefab

Para configurar el prefab de la bala:

1. Hacemos clic en el prefab de la bala y añadimos un script llamado `forwardMovement`.
2. En el script `forwardMovement`, creamos una variable pública de tipo float llamada `speed` e implementamos la lógica de movimiento para que la bala avance hacia adelante a lo largo del eje Z.
3. En Unity, configuramos la velocidad de la bala en 20 y nos aseguramos de que el script esté habilitado.
4. Creamos un GameObject vacío llamado `shootPoint` y lo posicionamos donde queremos que la bala sea disparada.

![image](https://github.com/user-attachments/assets/661e05eb-0079-4cb8-aaf8-a5b46ae8cb96)


# Player Shooting

  Se creó un objeto vacío llamado 'shootPoint' que funciona para poder darle una posicion inicial a la bala.
  En este caso lo colocamos dentro de la jerarquía del personaje ya que es él el que dispara la bala.
  Luego posicionamos el objeto vacío en el torso del personaje para simular como si él estuviera disparando.
  
<img width="179" alt="Screenshot 2024-10-04 at 11 38 58 AM" src="https://github.com/user-attachments/assets/b42a737e-bb92-452e-99b0-b73d4cdb5866"><img width="367" alt="Screenshot 2024-10-04 at 11 43 28 AM" src="https://github.com/user-attachments/assets/0c1f9101-1e2f-4d33-a88e-cbd36dd39346"><img width="450" alt="Screenshot 2024-10-04 at 11 44 12 AM" src="https://github.com/user-attachments/assets/dff46b70-cb6e-4761-93eb-7c8702fb6379">

 Luego, en el script the Player Movement se incorporaron dos variables de tipo GameObject para
 referenciar a los objetos previamente creados, estas variables fueron nombradas: prefab y shootPoint
<img width="503" alt="Screenshot 2024-10-04 at 12 07 00 PM" src="https://github.com/user-attachments/assets/47cb54f7-0b92-4a40-9f24-fdb4671774bd">

 Para poder hacer que el personaje 'dispare', es decir, que produzca una bala; añadimos este if en el Update()
 del codigo: 
<img width="896" alt="Screenshot 2024-10-04 at 12 13 35 PM" src="https://github.com/user-attachments/assets/1666ecd1-3f90-4705-9b02-e49f4de2e7d4">

 Ahora, finalmente el personaje produce una bala en cualquier posición que esté, simulando como si él la estuviera disparando.

 

 <img width="362" alt="Screenshot 2024-10-04 at 12 33 24 PM" src="https://github.com/user-attachments/assets/02470f80-b976-45c5-9a9d-87b5b1f409a2"><img width="831" alt="Screenshot 2024-10-04 at 12 33 46 PM" src="https://github.com/user-attachments/assets/77aa3aaa-2163-4c40-b275-59c05882f371">
<img width="567" alt="Screenshot 2024-10-04 at 12 34 10 PM" src="https://github.com/user-attachments/assets/c5200997-6f3f-4a4e-b184-6871172f7f8d">

# creción del script grafico del Robot


## script  grafico completo
<img width="1084" alt="Screenshot 2024-10-04 at 5 58 10 PM" src="https://github.com/user-attachments/assets/ee1f83ad-41c5-4561-ba21-10e58e4d9718">

Se puede visualizar el script gráfico completo, al cual le añadimos una nueva animación para mejorar la fluidez del movimiento del personaje. Específicamente, hemos incorporado animaciones para correr, moverse lentamente hacia adelante, atrás, a la derecha y a la izquierda. Además, hemos ocultado el cursor en el modo de juego.

## creación del script grafico 

<img width="1062" alt="Screenshot 2024-10-03 at 6 40 45 PM" src="https://github.com/user-attachments/assets/fbc38c92-3e1a-40cd-8f97-4c6ae9322cd3">

<img width="1051" alt="Screenshot 2024-10-03 at 6 41 01 PM" src="https://github.com/user-attachments/assets/84f8a9f4-d289-48a9-9dec-a368900629ee">

<img width="746" alt="Screenshot 2024-10-03 at 6 41 09 PM" src="https://github.com/user-attachments/assets/0ef29eb2-1473-48df-9f9c-980c1246214c">

<img width="879" alt="Screenshot 2024-10-03 at 6 41 17 PM" src="https://github.com/user-attachments/assets/f7d6d9da-dcc9-4120-a807-77afaa62d808">

<img width="861" alt="Screenshot 2024-10-03 at 6 41 22 PM" src="https://github.com/user-attachments/assets/2aaca980-d847-4168-a911-d4e2169c6837">

<img width="980" alt="Screenshot 2024-10-03 at 6 41 40 PM" src="https://github.com/user-attachments/assets/510819b7-6808-4405-9ae2-f30b12f0785c">

<img width="923" alt="Screenshot 2024-10-03 at 6 41 51 PM" src="https://github.com/user-attachments/assets/fd8b67f7-ad11-42bf-a8ed-fdc24f88d8da">

# jugador con el script grafico asignado

https://github.com/user-attachments/assets/b0550fb8-205f-4be2-adc4-4dd1f1ab4e09






