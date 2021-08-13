Nuestro proyecto proyecto Final!
Versión básica de la práctica final del curso de DevOps.

Se trata de una aplicación de SpringBoot con un único servicio REST que responde un mensaje de bienvenida en la url: http://localhost:8081
En el archivo gitignore, mantendremos el listado de todos los archivos con inforamacion sensible o que no deban subirse    al repositorio.

Para ponerlo en marcha, se proporciona un Dockerfile que utiliza una versión de openjdk16 para generar el ejecutable, y lo copia a una imagen con un un alpine con jre 16 donde se levanta la aplicación. Comandos a ejecutar:

    docker build -t hello-final:latest . Para construir la imagen
    docker run hello-final:latest. Para instanciar la imagen creada

Se proporciona también un fichero docker-compose.yaml, con el que puede instanciarse la imagen construida utilizando el comando: docker-compose up -d

Con el Jenkinsfile haremos un proceso CI/CD desde Jenkins Pipelines.
