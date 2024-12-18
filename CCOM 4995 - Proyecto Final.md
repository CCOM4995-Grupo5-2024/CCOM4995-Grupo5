Carlos Aparicio Mestra  
Ramon E. Miranda Calderon  
Ian M. Perez Lopez  
Grupo 5  
CCOM 4995: Desarrollo de video juegos

# Proyecto Final: Arcade Zombie Shooter
## Introduccion

## input system
<img width="559" alt="Screenshot 2024-12-17 at 4 47 22 PM" src="https://github.com/user-attachments/assets/d6ce149f-cd15-4f21-8cb2-9f10a8a6e7d0" />

## Assets Importados
### AllSky
![Screenshot 2024-12-17 171008](https://github.com/user-attachments/assets/e4d66e93-9f8d-4540-b4c4-30f92241fe80)  
Se importo el asset para crear un ambiente que sea de noche.
### M1A1 Machine Gun
![Screenshot 2024-12-17 171144](https://github.com/user-attachments/assets/51ed7bec-e661-4417-8e4a-211a5dec65c1)  
Rifle del jugador
### Free PBR barrel
![Screenshot 2024-12-17 171402](https://github.com/user-attachments/assets/8dfe4003-e9cc-4b3d-bb53-ff6457361461)  
Para crear ambiente  
### Horror Elements
![Screenshot 2024-12-17 171424](https://github.com/user-attachments/assets/d6436faf-c689-49ee-951f-4421b0ac1f46)  
Sonidos de horror  
### Procedural terrain painter
![image](https://github.com/user-attachments/assets/d27e83ff-d83d-40ed-9ada-6faa72d02a2a)  
Fue de utilidad a la hora de crear y modificar el terreno  
### Three Signs
![Screenshot 2024-12-17 171512](https://github.com/user-attachments/assets/709f9e1d-1c47-4483-8146-67869f70b8a5)  
Para crear ambiente  
### Towers PBR pack
![Screenshot 2024-12-17 171533](https://github.com/user-attachments/assets/adf39a7d-a383-4be6-a916-b4adb9fcdb23)   
Agregar watchtower en el mapa  
### Unity Terrain - URP Demo scene
![Screenshot 2024-12-17 171604](https://github.com/user-attachments/assets/d6cdb3bd-b4d0-479f-ac01-9fa65f08cb10)   
Funciono como base para crear mapa; se utilizo las texturas para la grama y rocas y arboles para la escena   
### Wateland Cabin
![Screenshot 2024-12-17 171620](https://github.com/user-attachments/assets/21daf914-70aa-4322-907b-ab40a7565000)  
La cabina en la escena

## Mapa/Escena
### Fotos
![Screenshot 2024-12-17 173402](https://github.com/user-attachments/assets/a3a42e2a-9d21-4f7b-b791-f3633a9f8b1a)
![Screenshot 2024-12-17 174905](https://github.com/user-attachments/assets/bd722d82-0e67-4e9d-b612-27f673985e17)
![Screenshot 2024-12-17 175030](https://github.com/user-attachments/assets/f934f3fb-4186-40cd-9758-c6c824445b63)
![Screenshot 2024-12-17 175202](https://github.com/user-attachments/assets/76167ff3-156a-478d-949e-32cfe080ddf1)
![Screenshot 2024-12-17 175231](https://github.com/user-attachments/assets/d08b68c1-b2cb-4de2-a944-f28de18fccf4)
![Screenshot 2024-12-17 175657](https://github.com/user-attachments/assets/97b8c3fb-c1a2-40ce-9f77-c582fa491106)
![Screenshot 2024-12-17 175829](https://github.com/user-attachments/assets/5343debd-f790-4008-b471-7137db871b58)
![Screenshot 2024-12-17 180619](https://github.com/user-attachments/assets/64ab80de-24a4-446c-a0fe-6873691548f5)

### Terrain Inspector
![Screenshot 2024-12-17 174758](https://github.com/user-attachments/assets/bf381532-035a-49cb-90f6-6fcf90a337b9)   
Se utilizo terrain painter (elemento que viene del procedural terrain painter) para agregarle capas de texturas al terreno. Las texturas apareceran en el mapa segun la elevacion detectada en el mapa.
Por ejemplo, en lugares montanosos donde hay una pendiente estrecha aparecera la textura rocosa, pero en lugares planos aparecera la textura de la grama.
### Terrain Settings
![Screenshot 2024-12-17 175329](https://github.com/user-attachments/assets/d2260fe1-fe31-4344-bf8a-82a14343c962)
### Jerarquia del terreno
![Screenshot 2024-12-17 173446](https://github.com/user-attachments/assets/bac80b58-3703-460e-a303-c5eba3ccb9af)   
El componente 'rock' esta compuesto por muchas rocas agrandadas y alineadas para crear la base del mapa.


## Prefabs
## Animaciones

## Animaciones del jugador

la animacion del jugador se hizo mediante la manipulacion de layers el cual el layer por defecto que esta activo es la animacion sin armas. me diante script se activan y desactivan los layers dependiendo del estado del jugador, es decir que si el jugador tiene un tipo de armas pistol el layer llamado pistol se activa. hizos un layers de armas cuarpo a cuerpo pero decidimos no implementarlo. 
### layer de jugador sin armas
<img width="1438" alt="Screenshot 2024-12-17 at 4 51 47 PM" src="https://github.com/user-attachments/assets/c59a990f-8f0e-4c5e-a4a9-b4ad7d211ae2" />
este layer es el layer por defecto el cual lo utilizamos para las animaciones del movimineto del personaje, incluyendo los saltos.

### contenido del blend tree llamado locomotion
<img width="1330" alt="Screenshot 2024-12-17 at 5 01 52 PM" src="https://github.com/user-attachments/assets/0b8932da-fe2e-4c71-b79f-ecaf50e78f82" />

el layer sin armas funciona praticamente con un blend tree el cual lo que hace es conectar las animaciones dependiendo del valor de 2 variables que en nuestro caso es movimineto horizontal y movimiento vertical el cual se lee del script playerController.

### Avatar de los layers secundarios

<img width="1332" alt="Screenshot 2024-12-17 at 5 10 16 PM" src="https://github.com/user-attachments/assets/b71b9357-5344-49e9-aa5d-8206ef5a5fe8" />

este avatar se les puso a todos los layers secundarios  para que se puedan mezclar las animaciones con el layer principal el cual es el layer que jestiona el movimiento. funciona para que solamente se ejecuten las animaciones en las partes seleccionadas. 

### layer de jugador con pistola
<img width="1434" alt="Screenshot 2024-12-17 at 4 52 39 PM" src="https://github.com/user-attachments/assets/84c132df-19f4-44d5-a47b-7006a181e5fe" />


### layer de jugador con rifle
<img width="1440" alt="Screenshot 2024-12-17 at 4 54 27 PM" src="https://github.com/user-attachments/assets/5f80b8ef-cc3b-4d3e-9821-b43c86c86f7e" />

### variables del animator

<img width="785" alt="Screenshot 2024-12-17 at 4 56 27 PM" src="https://github.com/user-attachments/assets/88347071-4869-47d0-88fc-d4f41b1a7979" />

## Efectos de particulas
## Sonido
## Scripts

### script PlayerController

<img width="1000" alt="Screenshot 2024-12-17 at 5 23 31 PM" src="https://github.com/user-attachments/assets/ef424fb7-8567-4f78-babb-c229d3f050ec" />
<img width="1000" alt="Screenshot 2024-12-17 at 5 25 49 PM" src="https://github.com/user-attachments/assets/597407eb-0766-4818-bcf7-677f2c580ac2" />
<img width="1000" alt="Screenshot 2024-12-17 at 5 27 01 PM" src="https://github.com/user-attachments/assets/f9ac05d2-4352-4d48-8baf-9749a6285754" />
<img width="1094" alt="Screenshot 2024-12-17 at 5 28 41 PM" src="https://github.com/user-attachments/assets/8160d714-7c67-4a71-9c43-a77ff078a294" />
<img width="1000" alt="Screenshot 2024-12-17 at 5 29 27 PM" src="https://github.com/user-attachments/assets/dcccf2b7-05c6-400a-a61e-587fe66380f6" />
<img width="1000" alt="Screenshot 2024-12-17 at 5 30 04 PM" src="https://github.com/user-attachments/assets/a6ab8e73-9685-4eff-977b-210493ceb0e7" />

este script lo que hace es controlar las animaciones del layer principal y tambien hacer el movimiento hacia la direccion que se indica, tambien controla la animacion del salto y tambien hace el moviminto de salto, esa son las cosas principales que hace el script.

### script de shooting

<img width="1000" alt="Screenshot 2024-12-17 at 5 38 41 PM" src="https://github.com/user-attachments/assets/c64955a9-6fa1-409d-ab54-c697b05f3d97" />
<img width="1000" alt="Screenshot 2024-12-17 at 5 44 11 PM" src="https://github.com/user-attachments/assets/e862223d-9c66-4216-a58a-0fc50c5317c0" />
<img width="1000" alt="Screenshot 2024-12-17 at 5 45 15 PM" src="https://github.com/user-attachments/assets/311a8511-26cf-464a-a146-8437d4314412" />
<img width="1001" alt="Screenshot 2024-12-17 at 5 46 19 PM" src="https://github.com/user-attachments/assets/f6cf4179-fb02-4599-87ba-3fbdc5058819" />
<img width="999" alt="Screenshot 2024-12-17 at 5 47 03 PM" src="https://github.com/user-attachments/assets/48c5df93-36f3-4265-b655-1c7b11476c57" />

El script shooting controla el comportamiento de disparo, tambien que la trayectoria del disparo sea la misma que la trayectoria que va desde el centro de la camara hacia adelante

### script activar arma

<img width="991" alt="Screenshot 2024-12-17 at 5 49 50 PM" src="https://github.com/user-attachments/assets/4629909c-31a6-4cc2-8d4b-75c8c7c273a9" />

El script ActivarArmas permite activar y recoger un arma cuando el jugador entra en su rango y presiona la tecla E. Al inicio, el arma está desactivada. Cuando el jugador entra en el collider del objeto (usando la etiqueta "Player"), el script detecta que está en rango. Al presionar E, el arma se activa, se agrega al inventario del jugador y el objeto que contiene el script se destruye(el objeto que contiene el script es el arma en el suelo).

![ScreenRecording2024-12-17at6 45 21PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/39e5c6ad-e346-4704-a136-3ffbbd11b603)
### script inventario
<img width="1080" alt="Screenshot 2024-12-17 at 5 57 37 PM" src="https://github.com/user-attachments/assets/a6fe7d02-187e-4eec-aafb-d3cd4b97f329" />
<img width="1118" alt="Screenshot 2024-12-17 at 5 57 59 PM" src="https://github.com/user-attachments/assets/96530e7c-4ec5-42ff-9a21-98f0840cff00" />
El script Inventario gestiona el inventario de armas de un jugador. Permite agregar armas al inventario, cambiar entre ellas y activar su correspondiente animación usando capas del Animator. Cada vez que el jugador cambia de arma (mediante una entrada del sistema Input), el script desactiva todas las armas y capas de animación excepto la del arma seleccionada, activándola para que se muestre correctamente.

![ScreenRecording2024-12-17at6 31 26PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/e4be9765-2b84-4487-831f-9a73abf37470)

### script WeaponAimRotation

<img width="1000" alt="Screenshot 2024-12-17 at 6 05 28 PM" src="https://github.com/user-attachments/assets/92f04a49-ae2b-4ca7-925c-7bb2ff775752" />
<img width="1238" alt="Screenshot 2024-12-17 at 6 06 05 PM" src="https://github.com/user-attachments/assets/39427d74-9399-4329-b1cc-37c8a3518f02" />
<img width="948" alt="Screenshot 2024-12-17 at 6 06 52 PM" src="https://github.com/user-attachments/assets/eb91fbd2-d3fc-4895-8ab3-032178261bc9" />


este script lo que hace es que rota el tozo del personaje verticalmente si esta en un layer secundario del animtor(esto quiere decir si tiene un arma). tambien jestiona la accion mira hace que la camara haga zoom cuando el personaje invoke a la accion y la imagen la cual es la mira se redusca cuando se apunte.

![ScreenRecording2024-12-17at6 12 54PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/47c5742a-7bd7-4a61-918e-34666304b524)
## UI
## Gameplay


