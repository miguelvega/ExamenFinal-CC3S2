## Produce un conflicto de fusión (merge) en algún repositorio de tus actividades realizadas. Establece los pasos y comandos que usas para resolver un conflicto de fusión en Git. Si intentas git push y falla con un mensaje como : Non-fast-forward (error): failed to push some refs esto significa que algún archivo contiene un conflicto de fusión entre la versión de tu repositorio y la versión del repositorio origen. Para este ejercicio debes presentar el conflicto dado, los pasos y comandos para resolver el problema y las solución.Primero, realiza un git pull para obtener los cambios más recientes del repositorio remoto

Usamremos el repositorio de PraticaCalificada5

Primero, realizamos un git pull para obtener los cambios más recientes del repositorio remoto.

![Captura de pantalla de 2023-12-13 07-38-09](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/e5116743-57c9-4b9d-b9cd-9cb2666bd18c)

Creamos una nueva rama llamada miguelvega nos movemos hacia esa rama con el comando git checkout -b miguelvega 

![Captura de pantalla de 2023-12-13 07-38-18](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/1096f363-023d-465e-9d3f-a35660e1dcd9)

Luego realizamos los cambios y lo guardamos.
Tanto git como github detectara un conflicto si hay cambios en la misma parte del código en la que hemos realizado modificaciones, en este caso
hemos realizados modificaciones en el controlador, con lo cual podemos saber que parte del codigo podemos modificar y arreglar dichos comflictos.


![Captura de pantalla de 2023-12-13 08-21-07](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/7a05ef94-f97a-414a-b905-336efae74596)


podemos hacer un merge pull request cuando esta de color verde, es decir cuando los conflictos se han solucionado.


![Captura de pantalla de 2023-12-13 07-39-43](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/479afcd3-e961-494e-b245-9e4417391fc5)

Asi como tambien un git merge main si estamos ubicados en la rama miguelvega 


![Captura de pantalla de 2023-12-13 08-30-24](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/3267d236-85c9-4eea-80ce-45bc2583b1a2)

