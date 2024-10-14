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


# C# Input System

## Horizontal and Vertical Movement

![image](https://github.com/user-attachments/assets/b339d51d-f756-4a08-a232-dd0cf953ef34)

![image](https://github.com/user-attachments/assets/045364cb-d0dc-4e6f-8731-d37d86c2c35e)

![gif1](https://github.com/user-attachments/assets/f7fdad4a-e551-423f-b45e-4201311ef312)


## Shoot 

![image](https://github.com/user-attachments/assets/b1937e8e-a7d2-48ab-923c-139f46f6bc80)

![image](https://github.com/user-attachments/assets/4796d9aa-d022-4521-8d79-661c77723eb7)

![gif2](https://github.com/user-attachments/assets/16fba9f6-51c0-49a2-b5e2-9fde491a9108)


# Script Graph

## Horizontal and Vertical Movement

![gif3](https://github.com/user-attachments/assets/5a90e003-58d2-4a19-8cfe-8de66f78156b)

## Shoot 

![gif4](https://github.com/user-attachments/assets/e13a4977-1939-4ac3-9a3e-f267f995be64)

# Visual Graph with New Input System
## Variables

<img width="317" alt="variables VG 1" src="https://github.com/user-attachments/assets/eeba9769-a458-4b54-9917-9b98b971a3e7">

<img width="315" alt="variables VG 2" src="https://github.com/user-attachments/assets/71527ecf-bc2c-4128-869d-0facda17937f">

<img width="316" alt="Variables VG 3" src="https://github.com/user-attachments/assets/bce41990-2cdc-4550-990c-540306323ae8">

## Visual Graph

<img width="1029" alt="vg1" src="https://github.com/user-attachments/assets/6c4741f3-059d-477e-a6e4-9a859dcd0968">

<img width="1102" alt="vg2" src="https://github.com/user-attachments/assets/23671453-cd7c-4f21-8672-79fb8f880621">

<img width="1054" alt="vg3" src="https://github.com/user-attachments/assets/dc141b4d-cc89-4e9a-b415-adf612b3051b">

<img width="1002" alt="vg4" src="https://github.com/user-attachments/assets/541a3333-14e4-4b49-abd6-96430e4a12a8">



## In game execution of Visual Graph
![PlayerMovementGameplsyVG-ezgif com-optimize](https://github.com/user-attachments/assets/b2d94dc4-8296-46e6-98f9-1d6bee2566c2)


## Execution of nodes in Visual graph
### Awake and Move's
![Awakeymove gif](https://github.com/user-attachments/assets/190f5151-c64d-4820-8bd0-44a740603802)

### Jump and run
![Jumpyrun-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/d2029dea-59f4-4b9a-ba38-3966c730767a)


## Look and Fire
![lookyfire-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/adf639b5-a052-4854-84be-d38a30584466)


# creación del script en c#

<img width="1043" alt="Screenshot 2024-10-13 at 11 11 25 PM" src="https://github.com/user-attachments/assets/48ee05e2-66b9-4895-9253-1482d7da2532">
<img width="850" alt="Screenshot 2024-10-13 at 11 11 43 PM" src="https://github.com/user-attachments/assets/4236dc07-8501-49f5-af0d-346ee143fd53">
<img width="922" alt="Screenshot 2024-10-13 at 11 11 54 PM" src="https://github.com/user-attachments/assets/a325fa5d-28ed-477b-bb44-16e2b645a48f">
<img width="1271" alt="Screenshot 2024-10-13 at 11 12 22 PM" src="https://github.com/user-attachments/assets/e550f083-8d25-44db-8fb2-074e69179a7b">
<img width="1177" alt="Screenshot 2024-10-13 at 11 12 36 PM" src="https://github.com/user-attachments/assets/1679c3bc-6f04-45b1-8bf1-c9887096e25c">


El script en C# llamado playerControls controla el movimiento, la rotación, el salto, el sprint, y las acciones de disparo de un personaje en Unity, utilizando el nuevo sistema de Input. Este script ajusta las animaciones del personaje según su estado y maneja su lógica de físicas mediante un Rigidbody. El movimiento horizontal y vertical se controla a través de métodos específicos que modifican las animaciones y las direcciones en las que el personaje se mueve, mientras que la rotación del personaje se ajusta según la entrada del jugador. El script también permite realizar saltos dobles, gestionando un contador de saltos y verificando si el personaje está en el suelo para reiniciar el conteo. La acción de disparo se maneja con una corrutina que permite un disparo continuo mientras el botón está presionado, instanciando un proyectil desde un punto específico. Además, hay un mecanismo de sprint que aumenta la velocidad del personaje cuando se activa. El Update se encarga de actualizar el movimiento del personaje y su rotación en cada cuadro, aplicando las animaciones correspondientes cuando el personaje se encuentra quieto.


###script en uso
![ScreenRecording2024-10-13at11 18 01PM-ezgif com-optimize](https://github.com/user-attachments/assets/7cc57ca9-37d5-42bf-a714-1dbc6b96e00f)
