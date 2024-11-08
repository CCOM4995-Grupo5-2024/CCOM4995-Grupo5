
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

