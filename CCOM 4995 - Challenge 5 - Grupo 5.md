Carlos Aparicio Mestra  
Ian M. Pérez López  
Ramón E. Miranda Calderón  
CCOM 4995: Desarrollo de Vídeo Juegos
Grupo 5


# Challenge 5: Go Ahead and Jump

En este ejercicio, practicamos cómo usar el nuevo Sistema de Entrada de Unity para integrar movimientos como saltar, correr y sus variantes.


## Action Matrix 

| Action                     | Input Method                                   |
|---------------------------|------------------------------------------------|
| Horizontal movement        | A and D keys, Left and Right arrows, gamepad left stick |
| Vertical movement          | W and S keys, Up and Down arrows, gamepad left stick |
| Shoot                      | Left mouse button, gamepad right trigger      |
| Jump                       | Spacebar, gamepad A button                     |
| Look                       | Mouse movement, gamepad right stick           |
| Fast horizontal movement   | Shift + A/D keys, gamepad left stick (press)   |
| Fast vertical movement     | Shift + W/S keys, gamepad left stick (press)   |

# Creación de InputActions
En la carpeta de assets se creo un Input actions

<img width="246" alt="Screenshot 2024-12-17 at 10 19 13 PM" src="https://github.com/user-attachments/assets/f498a77d-fae2-4826-9445-57a85227f84a" />

## Player inspector
Luego de crear el InputActions, en el inspector del jugador se agrego un componente PlayerInput que nos permite agregar el input actions que creamos. De esta manera las acciones creadas le aplicarán al jugador.

<img width="335" alt="Screenshot 2024-12-17 at 10 13 43 PM" src="https://github.com/user-attachments/assets/2f46fba7-f725-4be4-aa0d-8889340192a5" />

# Acciones Creadas

<img width="875" alt="Screenshot 2024-10-14 at 12 01 58 AM" src="https://github.com/user-attachments/assets/45b99448-e824-4223-9623-07ec8234489a">

Se han definido varias acciones para controlar al jugador en Unity. Al presionar el botón del mouse, el personaje disparará (acción Fire). Para saltar, se utiliza la barra espaciadora (acción Jump). Manteniendo presionada la tecla Shift, el jugador correrá (acción Run). El movimiento horizontal se controla con las teclas A/D o las flechas izquierda/derecha (acción HorizontalMove), mientras que el movimiento vertical se realiza con W/S o las flechas arriba/abajo (acción VerticalMove). Finalmente, al mover el mouse, se ajusta la dirección de la vista del jugador (acción Look). 

# Gráfica con Nuevo Input System
## Variables

<img width="317" alt="variables VG 1" src="https://github.com/user-attachments/assets/eeba9769-a458-4b54-9917-9b98b971a3e7">

<img width="315" alt="variables VG 2" src="https://github.com/user-attachments/assets/71527ecf-bc2c-4128-869d-0facda17937f">

<img width="316" alt="Variables VG 3" src="https://github.com/user-attachments/assets/bce41990-2cdc-4550-990c-540306323ae8">

## Visual Graph

### Horizontal Move
Se usa un nodo, 'On Input System Event Float' asignado a HorizontalMove, del nuevo input system que lee el valor en x cuando se oprimen las llaves A y D. Este nodo devuelve el valor en el eje x. Se inicializa la variable movementValue con el output del nodo inicial 'On Input System Event Float'. movementValue se multiplica por la variable speed. El resultado se ingresa en el un nodo nuevo que traslada el la posicion del valor x del personaje. Permite al jugador moverse de hacia los lados

### Vertical Move 
Basicamente es la misma serie de nodos que en Horizontal Move pero el resultado de la multiplicación es ingresado en la posición del valor z en el nodo que traslada al personaje. Y el nodo inicial es 'On Input System Event Float' asignado a VerticalMove. Permite al jugador moverse hacia alfrente y atrás.

### Run
Se usa un nodo, 'On Input System Event Button' asignado a Run, del nuevo input system que detecta cuando se oprime la llave: Shift. Si se oprime shift, se inicializa variable isRunning que detecta si el personaje corre. Luego de un nodo condicional, se asigna el valor de runSpeed a la variable aumentoVelocidad mediante un nodo de tipo Set Variable. Luedo se inicializa la variable currentSpeed con el resultado de la multiplicación entre speed y aumentoVelocidad. currenApeed es ingresado al nodo que traslada la posición al valor z del personaje. Permite correr

### Look
Se usa un nodo, 'On Input System Event Vector2' asignado a Look que lee el valor de Vector2. Se usa un nodo para obtener el valor de x en el Vector2. Ese valor es multiplicado por la variable rotationSpeed y ese resultado es asignado a la variable lookValue. El valor de look value es assignado a la posicón y del nodo 'Transform Rotate'. Permite rotar la pantalla con el movimiento del mouse.

### Fire
Se usa un nodo, 'On Input System Event Button' asignado a Fire que lee el 'left click' del mouse o 'touch pad' cada vez que se haga 'Left Click'. Cuando esto ocurre, se crea una instancia del prefab Bullet. Permite que el jugador dispare balas.

### Jump
Se usa un nodo, 'On Input System Event Button' asignado a Jump. Este nodo conecta a un nodo condicional que si determina que el jugador está en el piso (isGrounded) se conecta a otro nodo de tipo 'rigid body: Add Force' que hace mover al personaje imitando el efecto de brincar cuando recibe el valor de upForce en la posición y. Cuando de aplica esta fuerza, la variable isGrounded toma valor falso. Para determinar si el personaje esta en el piso, se toma la variable de rb y se asigna a un nodo 'On collision enter', resultado de ese nodo se compara (en un nodo de comparación) con el literal "Ground". Entonces la variable isGrounded toma un valor cierto. Permite al jugador brincar.

<img width="1029" alt="vg1" src="https://github.com/user-attachments/assets/6c4741f3-059d-477e-a6e4-9a859dcd0968">

<img width="1102" alt="vg2" src="https://github.com/user-attachments/assets/23671453-cd7c-4f21-8672-79fb8f880621">

<img width="1054" alt="vg3" src="https://github.com/user-attachments/assets/dc141b4d-cc89-4e9a-b415-adf612b3051b">

<img width="1002" alt="vg4" src="https://github.com/user-attachments/assets/541a3333-14e4-4b49-abd6-96430e4a12a8">



## Ejecución en Video Juego de Visual Graph
![PlayerMovementGameplsyVG-ezgif com-optimize](https://github.com/user-attachments/assets/b2d94dc4-8296-46e6-98f9-1d6bee2566c2)


## Ejecución de Nodos en Visual graph
### Awake y Mover
![Awakeymove gif](https://github.com/user-attachments/assets/190f5151-c64d-4820-8bd0-44a740603802)

### Brincar y Correr
![Jumpyrun-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/d2029dea-59f4-4b9a-ba38-3966c730767a)


## Mirar y Disparar
![lookyfire-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/adf639b5-a052-4854-84be-d38a30584466)


# Creación del Script en C#

<img width="1043" alt="Screenshot 2024-10-13 at 11 11 25 PM" src="https://github.com/user-attachments/assets/48ee05e2-66b9-4895-9253-1482d7da2532">
<img width="850" alt="Screenshot 2024-10-13 at 11 11 43 PM" src="https://github.com/user-attachments/assets/4236dc07-8501-49f5-af0d-346ee143fd53">
<img width="922" alt="Screenshot 2024-10-13 at 11 11 54 PM" src="https://github.com/user-attachments/assets/a325fa5d-28ed-477b-bb44-16e2b645a48f">
<img width="1271" alt="Screenshot 2024-10-13 at 11 12 22 PM" src="https://github.com/user-attachments/assets/e550f083-8d25-44db-8fb2-074e69179a7b">
<img width="1177" alt="Screenshot 2024-10-13 at 11 12 36 PM" src="https://github.com/user-attachments/assets/1679c3bc-6f04-45b1-8bf1-c9887096e25c">


El script en C# llamado playerControls controla el movimiento, la rotación, el salto, el sprint, y las acciones de disparo de un personaje en Unity, utilizando el nuevo sistema de Input. Este script ajusta las animaciones del personaje según su estado y maneja su lógica de físicas mediante un Rigidbody. El movimiento horizontal y vertical se controla a través de métodos específicos que modifican las animaciones y las direcciones en las que el personaje se mueve, mientras que la rotación del personaje se ajusta según la entrada del jugador. El script también permite realizar saltos dobles, gestionando un contador de saltos y verificando si el personaje está en el suelo para reiniciar el conteo. La acción de disparo se maneja con una corrutina que permite un disparo continuo mientras el botón está presionado, instanciando un proyectil desde un punto específico. Además, hay un mecanismo de sprint que aumenta la velocidad del personaje cuando se activa. El Update se encarga de actualizar el movimiento del personaje y su rotación en cada cuadro, aplicando las animaciones correspondientes cuando el personaje se encuentra quieto.


### Script en Uso
![ScreenRecording2024-10-13at11 18 01PM-ezgif com-optimize](https://github.com/user-attachments/assets/7cc57ca9-37d5-42bf-a714-1dbc6b96e00f)
