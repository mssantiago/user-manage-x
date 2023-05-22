# UserManageX

UserManageX es una poderosa aplicación de gestión de usuarios diseñada para simplificar y optimizar el proceso de administración de usuarios en tu organización. Con UserManageX, puedes crear, editar y eliminar perfiles de usuario de manera eficiente, asignar y revocar permisos, y controlar el acceso a diferentes sistemas y recursos con facilidad.


## Features

- Crear usuarios
- Eliminar usuarios
- Actualizar usuarios
- Obtener informacion de usuarios

## Arquitectura

Sigue una arquitectura de capas para mantener una estructura clara y modular. La arquitectura de capas ayuda a separar las responsabilidades y promueve la reutilización del código. 

- Capa de presentación: Esta capa se encarga de la interfaz de usuario y las interacciones con los usuarios. Aquí se manejaría la lógica relacionada con la representación visual de los datos y la interacción con las solicitudes del usuario, utilizando tecnologías como HTML, CSS y JavaScript.

- Capa de rutas (Route Layer): En esta capa, se definen las rutas de la aplicación y se gestionan las solicitudes HTTP entrantes. Express proporciona un enfoque basado en middleware para definir y gestionar las rutas, lo que facilita el enrutamiento de las solicitudes a los controladores adecuados.

- Capa de controladores (Controller Layer): Los controladores son responsables de manejar las solicitudes y las respuestas HTTP. Aquí se implementa la lógica de negocio relacionada con las operaciones de gestión de usuarios. Los controladores reciben los datos de la capa de rutas, realizan las operaciones necesarias en la capa de servicios y envían las respuestas adecuadas.

- Capa de servicios (Service Layer): La capa de servicios contiene la lógica de negocio principal de la aplicación. Aquí se definen y se implementan las operaciones relacionadas con la gestión de usuarios, como crear, actualizar, eliminar y consultar perfiles de usuario. Los servicios se encargan de interactuar con la capa de persistencia para realizar operaciones en la base de datos.

- Capa de persistencia (Persistence Layer): Esta capa se encarga de interactuar con la base de datos o cualquier otro medio de almacenamiento de datos. Puede utilizar un ORM (Object-Relational Mapping) o un ODM (Object-Document Mapping) para realizar operaciones de lectura y escritura en la base de datos de manera más sencilla.

La arquitectura de capas proporciona una separación clara de responsabilidades, lo que facilita la mantenibilidad, escalabilidad y pruebas de la aplicación. Permite que cada capa se enfoque en su tarea específica, lo que hace que el código sea más modular y reutilizable.

## Tech

UserManageX utiliza una serie de proyectos de código abierto para funcionar correctamente:

- [Angular] - HTML enhanced for web apps!
- [markdown-it] - Markdown parser done right. Fast and easy to extend.
- [Twitter Bootstrap] - great UI boilerplate for modern web apps
- [node.js] - evented I/O for the backend
- [Express] - fast node.js network app framework [@tjholowaychuk]
- [Breakdance](https://breakdance.github.io/breakdance/) - HTML
to Markdown converter

## Installation

UserManageX requiere [Node.js](https://nodejs.org/) v10+ to run.

Instale las dependencias y devDependencies e inicie el servidor.

```sh
cd UserManageX
npm i
node app
```


## Docker

UserManage es muy fácil de instalar e implementar en un contenedor Docker.

De forma predeterminada, Docker expondrá el puerto 8080, así que cámbielo dentro del
Dockerfile si es necesario. Cuando esté listo, simplemente use el Dockerfile para
construir la imagen.

```sh
cd dillinger
docker build -t <youruser>/dillinger:${package.json.version} .
```

Esto creará la imagen de dillinger y extraerá las dependencias necesarias.
Asegúrese de cambiar `${package.json.version}` con el actual
versión de Dillinger.

Una vez hecho esto, ejecute la imagen de Docker y asigne el puerto a lo que desee en
tu anfitrión. En este ejemplo, simplemente asignamos el puerto 8000 del host a
puerto 8080 del Docker (o cualquier puerto que haya estado expuesto en el Dockerfile):

```sh
docker run -d -p 8000:8080 --restart=always --cap-add=SYS_ADMIN --name=dillinger <youruser>/dillinger:${package.json.version}
```


```sh
127.0.0.1:8000
```


   [dill]: <https://github.com/joemccann/dillinger>
   [git-repo-url]: <https://github.com/joemccann/dillinger.git>
   [john gruber]: <http://daringfireball.net>
   [df1]: <http://daringfireball.net/projects/markdown/>
   [markdown-it]: <https://github.com/markdown-it/markdown-it>
   [Ace Editor]: <http://ace.ajax.org>
   [node.js]: <http://nodejs.org>
   [Twitter Bootstrap]: <http://twitter.github.com/bootstrap/>
   [jQuery]: <http://jquery.com>
   [@tjholowaychuk]: <http://twitter.com/tjholowaychuk>
   [express]: <http://expressjs.com>
   [Angular]: <http://angularjs.org>
   [Gulp]: <http://gulpjs.com>

   [PlDb]: <https://github.com/joemccann/dillinger/tree/master/plugins/dropbox/README.md>
   [PlGh]: <https://github.com/joemccann/dillinger/tree/master/plugins/github/README.md>
   [PlGd]: <https://github.com/joemccann/dillinger/tree/master/plugins/googledrive/README.md>
   [PlOd]: <https://github.com/joemccann/dillinger/tree/master/plugins/onedrive/README.md>
   [PlMe]: <https://github.com/joemccann/dillinger/tree/master/plugins/medium/README.md>
   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
