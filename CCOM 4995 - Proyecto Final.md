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
Se importó el asset para crear un ambiente que sea de noche.
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
Fue de útilidad a la hora de crear y módificar el terreno  
### Three Signs
![Screenshot 2024-12-17 171512](https://github.com/user-attachments/assets/709f9e1d-1c47-4483-8146-67869f70b8a5)  
Para crear ambiente  
### Towers PBR pack
![Screenshot 2024-12-17 171533](https://github.com/user-attachments/assets/adf39a7d-a383-4be6-a916-b4adb9fcdb23)   
Agregar watchtower en el mapa  
### Unity Terrain - URP Demo scene
![Screenshot 2024-12-17 171604](https://github.com/user-attachments/assets/d6cdb3bd-b4d0-479f-ac01-9fa65f08cb10)   
Funcionó como base para crear mapa; se utilizo las texturas para la grama y rocas y árboles para la escena   
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
Se utilizó terrain painter (elemento que viene del procedural terrain painter) para agregarle capas de texturas al terreno. Las texturas apareceran en el mapa segun la elevacion detectada en el mapa.
Por ejemplo, en lugares montañosos donde hay una pendiente estrecha aparecerá la textura rocosa, pero en lugares planos aparecerá la textura de la grama.
### Terrain Settings
![Screenshot 2024-12-17 175329](https://github.com/user-attachments/assets/d2260fe1-fe31-4344-bf8a-82a14343c962)
### Jerarquía del terreno
![Screenshot 2024-12-17 173446](https://github.com/user-attachments/assets/bac80b58-3703-460e-a303-c5eba3ccb9af)   
El componente 'rock' esta compuesto por muchas rocas agrandadas y alineadas para crear la base del mapa.


## Prefabs
### Zombie 
Modelo   
![Screenshot 2024-12-17 181131](https://github.com/user-attachments/assets/af6d7518-3017-46f0-8635-193cff15896b)   

Jerarquía donde incluye partícula para simular el efecto de sangre   
![Screenshot 2024-12-17 181145](https://github.com/user-attachments/assets/022c9397-94ad-4000-adb0-820060f2df0e)   

Inspector de zombie   
![Screenshot 2024-12-17 181239](https://github.com/user-attachments/assets/eb4de384-6aab-4d59-a0b5-f0d386efe828)   
![Screenshot 2024-12-17 181337](https://github.com/user-attachments/assets/1f2fe1c2-1189-4b5b-9f59-85daff02975e)   

## Animaciones
### Zombie
Las animaciones del zombie se descargaron en la aplicación mixamo

Animación de correr   
![ScreenRecording2024-12-17182358-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/22135835-d020-4032-8544-51b16571bb8e)  

Animación de atacar   
![ScreenRecording2024-12-17182442-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/eb898cc0-15fd-49d8-930b-909e9ddc753a)   

Animación de muerte   
![ScreenRecording2024-12-17182514-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/b1ee4c89-fd32-47c4-88fd-26aa11ee6a96)   
   
Controlador de animaciones   
![Screenshot 2024-12-17 182152](https://github.com/user-attachments/assets/aaa7736e-2e77-4be8-976e-7f86917fcd0a) 
  Básicamente, se agregan las animaciones importadas a la pestaña de animator y en ahí es que se establecen las transiciones de las animaciones según los parametros establecidos. En el caso del zombie, implementamos 3 animaciones: Correr, atacar y muerte. Una vez el zombie hace spawn, ya detecta al jugador y por lo tanto se activa la animacion de correr, cuando el jugador esta en rango de ataque la animación hace una transición a la de ataque. La animación del zombie puede cambiar entre esos dos estados continuamente. En el caso de muerte, las animaciones pueden hacer transiciones hacía él, pero de la animación de muerte no se puede transicionar a otra animación ya que el zombie va a estar muerto.   

  Transición de atacar a correr   
  ![ScreenRecording2024-12-17185545-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/80e74b2b-ff3b-4d01-ac5a-9d15a0fff907)   
  Transición de correr a atacar   
  ![ScreenRecording2024-12-17185520-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/4013baa4-543f-4253-b83d-f5763df3b3ba)   
  Transición de correr a muerte   
  ![ScreenRecording2024-12-17185717-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/81abd3a5-802b-41c7-9929-23fea2a627ee)   
  Transición de atacar a muerte   
  ![ScreenRecording2024-12-17185717-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/4bed94f0-0187-45e0-9ece-5dbace29fb38)

  Como se puede notar en las imagenes de arriba, las transiciones de animación ocurren cuando se activan ciertos parametros. El parametro de correr siempre es cierto, por lo tanto el zombie transiciona, de estar corriendo, a cualquiera de las otras dos animaciones. Si se activa el parametro de "Atak"(de tipo trigger) pues se transiciona a la animación de ataque. Si se activa el parametro(trigger) de 'Death' entonces se transiciona a la animación de muerte. 


## Animaciones del jugador

La animación del jugador se hizo mediante la manipulacion de layers el cual el layer por defecto que esta activo es la animacion sin armas. me diante script se activan y desactivan los layers dependiendo del estado del jugador, es decir que si el jugador tiene un tipo de armas pistol el layer llamado pistol se activa. hizos un layers de armas cuarpo a cuerpo pero decidimos no implementarlo. 
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
Todos los efectos de partículas fueron creados por nosotros utilizando el Particle System de Unity
### Sangre
![ScreenRecording2024-12-17191923-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/ed50f3d6-2de4-403d-a6a8-54569bb31a47)
### Neblina
![ScreenRecording2024-12-17192009-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/1b65386d-1edb-41db-907b-eecfa67e9bea)
### Pólvora
Por alguna razon en el gif aparece blanca pero mas adelante se vera el color real.
![ScreenRecording2024-12-17192106-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/ca6fadae-c1f4-426f-80c8-5dcd20041757)


## Sonido
### Efectos de sonido
Para para manejar los efectos de sonido en el juego se creó un objeto vacío llamado sound manager con su script respectivo. El objeto tiene 3 Audio Sources: 1 para manejar el sonido del disparo y los otros dos para manejar el sonido de los zombies.
![Screenshot 2024-12-17 193043](https://github.com/user-attachments/assets/06a161cf-cfc3-4b35-b0b8-46bddb13ace6)
### SoundTrack
Para manejar la música del juego se implementó un cubo para establecer de donde se emitirá la música, igual se le asignó 1 solo audio source para la canción
![Screenshot 2024-12-17 193657](https://github.com/user-attachments/assets/e96a3897-e8bc-4a52-841b-f1dbd5442206)

### Ejemplo 

https://github.com/user-attachments/assets/d6246740-37da-460c-b7a5-814fe348b9a4

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
### Script de SoundManager
SoundManager organiza y controla los efectos de sonido del juego de manera eficiente y accsesible   
![Screenshot 2024-12-17 202440](https://github.com/user-attachments/assets/cc82b4a3-c2a3-41ea-ab3c-d6d9e612df0e)

### Script de ZombieLife
En este script se monitorea la vida del zombie y al llegar a 0 se activa la animación de muerte, se reproduce un sonido, y se eliminan los recursos del zombie despues de la animacion.   
![Screenshot 2024-12-17 202520](https://github.com/user-attachments/assets/45f3cccc-cbd1-490a-85c4-92078167ce79)

### Script de Sight
![Screenshot 2024-12-17 202535](https://github.com/user-attachments/assets/5ea2776f-0f44-4dd7-9c88-be4f8510a1ac)   
Este script implementa la detección visual de un enemigo, simulando un campo de visión basado en una distancia y un ángulo. Es el mismo script que se implementó en clase.

### Script de Zombie
![Screenshot 2024-12-17 202646](https://github.com/user-attachments/assets/18edfd6e-2415-4ce3-8e37-ff0dc0231842)   
El Zombie script es responsable de agregar y remover un zombie al zombieManager cuando es creado o destruido.

### Script de Main Menu
![Screenshot 2024-12-17 202722](https://github.com/user-attachments/assets/db0b7f21-be19-4d4d-b6a2-732f048719c1)   
Este script se encarga en manejar el menú principal del juego, maneja la música de fondo, el inicio de una nueva partida y la salida de la aplicación.

### Script de EnemyDrop
![Screenshot 2024-12-17 202549](https://github.com/user-attachments/assets/5ab1db75-eb2d-4860-a43c-63952299bc83)   
Controla la probabilidad de que un enemigo suelte un objeto al morir. Al seleccionar un objeto aleatorio de una lista de posibles objetos, instancia el objeto en la posición actual del enemigo.

### Script de ZombieFSM
### Script de ContactDamage
### Script de ZombieManager
### Script de MedKit

## UI
### Menu
UI canvas:
![Screenshot 2024-12-17 212126](https://github.com/user-attachments/assets/ee22c535-f2ea-4a14-8fca-09a56a66d0e2)   
Jerarquía del menu:   
![Screenshot 2024-12-17 211943](https://github.com/user-attachments/assets/d0f09d04-cae9-44f5-92b5-3cfe89f45906)   
Inspector del objeto vacío MainMenu que contiene el script de MainMenu que permite gestionar la música del juego   
![Screenshot 2024-12-17 211948](https://github.com/user-attachments/assets/255f762f-8d24-4d42-8a35-8dc1adf7f1e3)   

En el inspector de ambos botones hay un componente Button(Onclick) que nos permite pasar el objeto de MainMenu como parametro y asignarle que función queremos que ejecute al precionar el botón. En este caso se utilizan las dos funciones que implementamos en el script de MainMenu.   
![Screenshot 2024-12-17 212154](https://github.com/user-attachments/assets/9fad9aab-4335-4a31-a416-869b195c4fd0)
![Screenshot 2024-12-17 212217](https://github.com/user-attachments/assets/a2c1dce8-5e32-4b5c-8e1a-f17e4b11d0bd)

## Gameplay


# ToDo ##############

### Script de ZombieFSM

![image](https://github.com/user-attachments/assets/1c9f16f1-7d0b-419e-ab2d-6581a2df4f2a)


### Script de ContactDamage

![image](https://github.com/user-attachments/assets/a14b1bd1-5622-4690-9a9c-a33d4911d32f)



### Script de Spawner

![image](https://github.com/user-attachments/assets/2d549ddf-7e2e-4c34-bad2-c0b5aa60c646)

![image](https://github.com/user-attachments/assets/29f86ad7-2c6f-41fd-bcea-df3793f78e1b)



### Script de MedKit

![image](https://github.com/user-attachments/assets/eb187726-bf70-454d-8c42-c6621618522a)


## MedKit Prefab

![image](https://github.com/user-attachments/assets/7d8e0381-87c8-4ad7-a932-178ab9893e1f)

## Medkit Asset

![image](https://github.com/user-attachments/assets/a91b4440-11b8-42d6-b0a3-959426851079)



### Gameplay

## Winning Game

## Losing Game


### Bomba

![image](https://github.com/user-attachments/assets/8a232167-34df-4b25-8ca2-3334478ff231)


## Bomb Progress Bar

![image](https://github.com/user-attachments/assets/a0f89b0e-b55f-494f-aa14-cb4486783d7a)

![image](https://github.com/user-attachments/assets/39e50a8b-2a02-44f8-97d3-ca3ab705d6ee)


## Bomb Asset

![image](https://github.com/user-attachments/assets/4e5a3980-1f5c-4288-a22c-6d1d5a238a78)


## Player Stats

![image](https://github.com/user-attachments/assets/51efc093-832b-4b31-9684-ebc7f957d0c5)

![image](https://github.com/user-attachments/assets/31bb6348-3584-4ff3-b71b-f8fe94daf33f)



## PlayerHUD

![image](https://github.com/user-attachments/assets/1de923a9-a8cf-42dc-8577-47d9de2fc88a)


### Health Bar

![image](https://github.com/user-attachments/assets/3a6437e2-8dbc-457f-b5b1-7cb85210960d)

![image](https://github.com/user-attachments/assets/7d64101b-e8e9-4f26-bdaa-4b0110b7dc8c)

![image](https://github.com/user-attachments/assets/1b96d17a-44b8-449c-9408-fc4e8381b94d)





### ZIP file del juego

