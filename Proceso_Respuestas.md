## Parte 1 

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


## Parte 2

En  este ejercicio usarás TDD para desarrollar la funcionalidad RottenPotatoes que permite al usuario buscar una película en TMDb. Específicamente, usarás TDD para crear un controlador, que recibe la solicitud del usuario, y un modelo que en realidad llama al servicio TMDb remoto para obtener información sobre la película especificada.
Utiliza la carpeta comprimida dado en la evaluación. 
Asegúrate de ejecutar bundle install --without para configurar todas las dependencias. Aquí trabajarás con TMDb API y Guard para automatizar el flujo de trabajo (puedes utilizar algunas otras si crees necesario) . También utilizarás Faraday, unalibreríacliente HTTP, para realizar llamadas API. Edita el Gemfile para incluir las siguientes gemas:

```
gem 'faraday'  
group :test do
  gem 'rails-controller-testing'
  gem 'guard-rspec'                 
end

```

Ejecutamos bundle install nuevamene

 ![Captura de pantalla de 2023-12-13 08-53-05](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/c8814240-3d0f-4082-9826-d7075bcf1f19)

Luego ejecuta Rails generate rspec:install para asegurarte de que los archivos que RSpec que necesitas estén en su lugar.

![Captura de pantalla de 2023-12-13 08-57-56](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/eaa751fd-997a-4e1f-8eaf-27f7f4273520)

Edita el archivo spec/rails_helper.rb para incluir require 'byebug' en la parte superior, de modo que puedas acceder al depurador según sea necesario para que las pruebas funcionen.

![Captura de pantalla de 2023-12-13 08-59-38](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/bfa74963-e04b-44fd-8dfd-a7fc69689068)

Ejecuta el paquete exec guard init rspec para configurar los archivos necesarios para Guard, lo que dará como resultado la creación de un nuevo Guardfile. Agrega ese archivo a tu repositorio.

![Captura de pantalla de 2023-12-13 09-00-25](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/2df63d50-84a8-46d0-8714-dab851547d4b)

Configura la base de datos con el comando habitual 

![Captura de pantalla de 2023-12-13 09-08-45](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/18ed5c79-6b3b-4a70-910d-d396b7d448ef)

Cargamos las semillas en la base de datos con el comando y ejecutamos el servidor para mostrar que todo este bien.


![Captura de pantalla de 2023-12-13 09-13-26](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/89e34d05-2c8e-46e2-80a4-81e530912a53)

Ampliaremos RottenPotatoes con un formulario que permita al usuario buscar en The Open Movie Database (TMDb) una película para agregar a RottenPotatoes.

Agregamos las lineas de codigo faltantes en el archivo.Primero los parámetros del formulario con los que se debe enviar y segundo un botón que nos lleva de regreso a la página de inicio.

![Captura de pantalla de 2023-12-13 09-40-39](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/06b7b00a-b162-4b15-8703-855568047cc9)

Cremos la funcion search_tmdb que sera nuestra acción del controlador que manejará el envío del formulario dada en la vista anterior..
![Captura de pantalla de 2023-12-13 09-42-15](https://github.com/miguelvega/ExamenFinal-CC3S2/assets/124398378/c81a0f27-3894-4572-8825-246cd4487793)
