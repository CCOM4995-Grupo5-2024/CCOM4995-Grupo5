Carlos Aparicio Mestra  
Ian M. Pérez López  
Ramón E. Miranda Calderón  
CCOM 4995: Desarrollo de Vídeo Juegos
Grupo 5


# Challenge 6: Advanced Project (Mini Game Creation)

En este ejercicio, desarrollaremos un juego utilizando clases de mánager para rastrear y controlar varios aspectos del juego, como los estados de los objetos y el progreso del juego. Al centralizar la lógica de administración, una clase de “Game Manager” puede supervisar múltiples elementos y valores del juego, como enemigos, puntajes y estados del juego, mejorando la organización y la eficiencia. 

## Mini Game

En este mini-juego, el jugador enfrenta y le dispara a los enemigos. Si el jugador falla y les da a las paredes, los paneles del piso desaparecen según el tipo de golpe de pared: los golpes de la pared lateral eliminan un solo panel, mientras que los golpes de la pared de la esquina eliminan todos los paneles del piso. El objetivo de los jugadores es destruir tantos enemigos como sea posible antes de que se puedan caer hacia el vacío debajo del nivel.

## Stage

### Floors
![image](https://github.com/user-attachments/assets/ae9f8343-5c10-4763-8462-5881a4492395)

### Walls

#### Corners
![image](https://github.com/user-attachments/assets/6b473575-4c3e-49b3-8ee3-e288246b8f0d)

#### Side Walls
![image](https://github.com/user-attachments/assets/80f9caf0-fb82-4cda-8f9d-8e45ba811a41)


## Spawners
![image](https://github.com/user-attachments/assets/c4dfe3c7-e1a7-4bac-8b24-f4fc992acf50)

## Enemy Manager
![image](https://github.com/user-attachments/assets/6478660e-4281-422f-8411-fd3dceda5f7b)

![image](https://github.com/user-attachments/assets/891171f3-5276-4491-9a93-0d34e46bfa68)


 
## Enemies Manager Gif
![ScreenRecording2024-11-08at10 14 31PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/357127d6-b4f9-4cbc-bb98-87cf3066e67b)

## Waves Manager
Para poder tener record de cuantos spawners hay activos se creo el wave manager.
Primero se creo un objeto vacío llamado WaveManager

<img width="324" alt="Screenshot 2024-11-08 at 9 52 39 PM" src="https://github.com/user-attachments/assets/5dcf703f-ff67-434b-a5b1-a405f96ac52e">

### Script

<img width="1262" alt="Screenshot 2024-11-08 at 9 50 04 PM" src="https://github.com/user-attachments/assets/997a87b9-c5f9-4f6d-b937-14fbc5fca71f">

### Waves Manager Gif

![ScreenRecording2024-11-08at10 16 43PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/f572f2a7-b1f7-4afb-b847-42bd36e3a9f7)

## Plano de estadio
Si el jugador se cae y hace contacto con el plano, se muere
### Script

<img width="982" alt="Screenshot 2024-11-08 at 9 37 31 PM" src="https://github.com/user-attachments/assets/9efd300d-aca8-4c0f-a374-ecc373048ecf">

# script de Wall

<img width="1000" alt="Screenshot 2024-11-08 at 7 14 32 PM" src="https://github.com/user-attachments/assets/d0589bc7-7386-4df2-a31d-5f7388466218">
<img width="1000" alt="Screenshot 2024-11-08 at 7 15 13 PM" src="https://github.com/user-attachments/assets/a4e95b53-74bb-4adf-ba1e-8e0fb6b9767c">

El script Wall gestiona el comportamiento de las paredes del juego, diferenciando entre paredes laterales y de esquina. Al detectar una colisión con una bala, la pared activa un comportamiento específico dependiendo de su tipo: si es una pared lateral, elimina un piso aleatorio de la escena, mientras que si es una pared de esquina, elimina todos los pisos. Utiliza el WallManager para registrar las paredes y notificar cambios a través de un evento.

El script Wall se asignará a los prefabs de las paredes de la siguiente forma: se agregará el script a los prefabs de las paredes laterales y de esquina en la escena. Luego, se configurará el tipo de pared (lateral o esquina) utilizando el enum WallType en el inspector de Unity. Esto permitirá que cada prefab de pared tenga un comportamiento específico al detectar una colisión, eliminando un piso aleatorio en el caso de las paredes laterales o destruyendo todos los pisos en el caso de las paredes de esquina.

<img width="1440" alt="Screenshot 2024-11-08 at 7 29 03 PM" src="https://github.com/user-attachments/assets/64a53bb4-c9ec-418c-a199-ca877831e39b">
<img width="1440" alt="Screenshot 2024-11-08 at 7 29 12 PM" src="https://github.com/user-attachments/assets/bb8d49dc-e618-451c-af9b-da9962057011">



# script de WallManager

<img width="1000" alt="Screenshot 2024-11-08 at 7 24 47 PM" src="https://github.com/user-attachments/assets/490ad811-f458-4e82-bfcc-6f8d3c8bc434">

El script WallManager gestiona todas las paredes en el juego utilizando el patrón de diseño singleton. Mantiene una lista de todas las paredes registradas y proporciona métodos para añadir paredes a esta lista, como el método AddWall(), que también activa un evento (onChanged) para notificar cambios. Además, asegura que solo exista una instancia de WallManager en la escena, verificando su unicidad en el método Awake(). Este script permite centralizar el control de las paredes y reaccionar a modificaciones de la lista, facilitando la gestión de todas las paredes en el juego.

El script WallManager se asigna a un objeto vacío, donde se gestionarán y se visualizarán la cantidad de paredes laterales y de esquina.

<img width="1440" alt="Screenshot 2024-11-08 at 7 28 45 PM" src="https://github.com/user-attachments/assets/b8d69b79-97d9-40c2-9fa4-0bf1f0133ed8">

# script de FloorManager

<img width="1000" alt="Screenshot 2024-11-08 at 7 25 45 PM" src="https://github.com/user-attachments/assets/ebb26493-99fc-4a71-bd7e-4b093345b4bf">
<img width="1000" alt="Screenshot 2024-11-08 at 7 26 36 PM" src="https://github.com/user-attachments/assets/bef66bab-13e0-428f-8a1c-06cd9d01681e">

El script FloorManager gestiona todos los pisos en el juego utilizando también el patrón de diseño singleton. Mantiene una lista de todos los pisos y proporciona métodos para añadir (AddFloor()), eliminar (RemoveFloor()) y eliminar todos los pisos (RemoveAllFloors()).

El script FloorManager se asigna a un objeto vacío, donde se gestionarán y visualizarán la cantidad de pisos. Al tocar una pared lateral, se eliminará un piso aleatorio, y al disparar a una pared de esquina, se destruirán todos los pisos de la escena.

<img width="1440" alt="Screenshot 2024-11-08 at 7 28 45 PM" src="https://github.com/user-attachments/assets/b8d69b79-97d9-40c2-9fa4-0bf1f0133ed8">

## Eliminación de floor gif
Se elimina uno de los 16 pisos cuando la bala hace contacto con una pared regular. Se elimiaan todos los pisos cuando la bala choca con una esquina.

![Floors-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/9c1c61c6-305e-475f-89d2-5c8d027d5f63)


## Score Manager
Para tener un record de cuantos puntos tiene le jugador según los enemigos que mata se creó un Score Manager.

<img width="328" alt="Screenshot 2024-11-08 at 9 55 22 PM" src="https://github.com/user-attachments/assets/83a7cc5e-bf45-41b1-976c-92e3d5029fa4">

### Script Score Manager
<img width="659" alt="Screenshot 2024-11-08 at 9 58 44 PM" src="https://github.com/user-attachments/assets/d34b5ead-9604-4aa5-be03-050add821185">

### Script Score on Death
<img width="867" alt="Screenshot 2024-11-08 at 10 02 12 PM" src="https://github.com/user-attachments/assets/efe483d5-71de-4f9d-af9f-0daba0fc940a">


## Lluvia
Luego de coordinar los scripts para que se eliminara el piso cuando una bala haga contacto con la pared, incorporamos lluvia al juego para incrementar la dificultad del juego.
### Prefab
Se escogió una esfera como el objeto para representar las gotas de lluvia con un tamaño un poco mayor que la bala del jugador. Y se creó un material azul fosforecente para que la gota se vea claramente.

<img width="1177" alt="Screenshot 2024-11-08 at 6 27 52 PM" src="https://github.com/user-attachments/assets/5d2aa8af-839f-4e28-b03d-e96fa0a20492">


### RainSpawners
Para poder generar lluvia en el juego se modifico el script de 'Spawner' de los enemies para que genere muchas gotas de lluvias en el minijuego. Se creó un objeto vacío llamado 'RainSpawner' y se le agregó un script con el mismo nombre.

<img width="1305" alt="Screenshot 2024-11-08 at 7 21 49 PM" src="https://github.com/user-attachments/assets/4bbd7781-af16-4dc6-8c9f-09c4273e4c35">

<img width="1114" alt="Screenshot 2024-11-08 at 7 39 53 PM" src="https://github.com/user-attachments/assets/dc33f5b2-2bdc-44b6-9fad-60e304248e00">

Para que el objeto de raindrop cumpla con las sus coalliciones respectivas(que la gota no afecte al enemigo, pero el enemigo si a la gota; que la gota haga efecto sobre el jugador y el jugador sobre la gota; y finalmente que la lluvia no afecte la trajectoria de las balas) se modifico la matriz de coaliciones en project settings -> Physics, para permitir que la lluvia no tenga efecto sobre la trayectoria del enemigo.

<img width="328" alt="Screenshot 2024-11-08 at 8 00 51 PM" src="https://github.com/user-attachments/assets/9818830c-756d-485f-bd6c-584567282a29">
<img width="355" alt="Screenshot 2024-11-08 at 8 02 15 PM" src="https://github.com/user-attachments/assets/f99726a8-5204-4020-909c-298cca95ca3d">

### Rain Manager
Se creo este rain manager para tener cuenta de cuantos raindrops hay en la escena
<img width="743" alt="Screenshot 2024-11-08 at 8 50 35 PM" src="https://github.com/user-attachments/assets/da9b79cd-19bc-43e5-887c-b342b7cc7877">

### Script de Rain y AutoDestroy en el prefab de raindrop
<img width="1089" alt="Screenshot 2024-11-08 at 8 51 13 PM" src="https://github.com/user-attachments/assets/669dd488-8367-42cb-9139-f0355a5d5ea3">
<img width="566" alt="Screenshot 2024-11-08 at 8 52 12 PM" src="https://github.com/user-attachments/assets/3ab994b7-7e43-49f9-b8ea-7abfc3e67e38">

### Efecto de lluvia
![ScreenRecording2024-11-08at8 23 42PM-ezgif com-video-to-gif-converter (1)](https://github.com/user-attachments/assets/09cebc6a-ea33-4ff5-a8c1-ecd1c706caa7)

## GameMode
Se inicializó un objeto vacío llamado GameMode para poder manejar las condiciones de ganar y perder del juego. Pues para que el jugador pierda su vida tiene que llegar a 0 y para que gane, el jugador debe de eliminar todos los enemigos y no deben de quedar rondas(waves) de enemigos. Para poder llevar a cabo esto, se creó un script con las condiciones de ganar y perder.

<img width="325" alt="Screenshot 2024-11-08 at 9 00 43 PM" src="https://github.com/user-attachments/assets/cdc39269-01e1-4ef3-b394-1e61164a9b75">

### Script de GameMode

<img width="1259" alt="Screenshot 2024-11-08 at 9 26 34 PM" src="https://github.com/user-attachments/assets/1b23cc30-a809-4bc1-a497-f43ec58921df">

### Condición de pérdida
Cuando el jugador cae al plano su vida va a 0 y por lo tanto muere.
![ScreenRecording2024-11-08at8 37 35PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/a473f637-56a1-4e0c-9b5c-dd05949eab60)

### Condición de ganar
Cuando se elimina al ultimo enemigo y no quedan mas waves de enemigos
![ScreenRecording2024-11-08at8 43 23PM-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/4b6c7919-9053-4166-b4fa-82781fcb725b)




