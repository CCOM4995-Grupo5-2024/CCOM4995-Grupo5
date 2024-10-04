Carlos Aparicio Mestra  
Ian M. Pérez López  
Ramón E. Miranda Calderón  
CCOM 4995: Desarrollo de Vídeo Juegos
Grupo 5

# Challenge 4: Bullet Time
  En este challenge implementamos scripts y visual graphs en nuestro proyecto que nos permiten: 
  Mover al personaje y poder implementar el efecto de disparar. 
  Se creo un prefab que funciona como bala y el personaje fue descargado del asset store.

# Player Shooting script

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





 


