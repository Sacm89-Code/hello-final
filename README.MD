Nuestro proyecto proyecto Final!
Versión básica de la práctica final del curso de DevOps.

Se trata de una aplicación de SpringBoot con un único servicio REST que responde un mensaje de bienvenida en la url: http://localhost:8081
En el archivo gitignore, mantendremos el listado de todos los archivos con inforamacion sensible o que no deban subirse    al repositorio.

Para ponerlo en marcha, se proporciona un Dockerfile que utiliza una versión de openjdk16 para generar el ejecutable, y lo copia a una imagen con un un alpine con jre 16 donde se levanta la aplicación. Comandos a ejecutar:

    docker build -t hello-final:latest . Para construir la imagen
    docker run hello-final:latest. Para instanciar la imagen creada

Se proporciona también un fichero docker-compose.yaml, con el que puede instanciarse la imagen construida utilizando el comando: docker-compose up -d

Con el Jenkinsfile haremos un proceso CI/CD desde Jenkins Pipelines.

Started by user Simón Cervantes
Running as SYSTEM
Building in workspace /var/lib/jenkins/workspace/hello-final
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/hello-final/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/Sacm89-Code/hello-final.git # timeout=10
Fetching upstream changes from https://github.com/Sacm89-Code/hello-final.git
 > git --version # timeout=10
 > git --version # 'git version 2.17.1'
 > git fetch --tags --progress -- https://github.com/Sacm89-Code/hello-final.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
Checking out Revision dcf7fa4ba66f24f0a738f9d5f6044d3d9f8d9c34 (refs/remotes/origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f dcf7fa4ba66f24f0a738f9d5f6044d3d9f8d9c34 # timeout=10
Commit message: "fixing jenkins"
 > git rev-list --no-walk dcf7fa4ba66f24f0a738f9d5f6044d3d9f8d9c34 # timeout=10
[Gradle] - Launching build.
[hello-final] $ /var/lib/jenkins/workspace/hello-final/gradlew assemble
Downloading https://services.gradle.org/distributions/gradle-7.1.1-bin.zip
..........10%...........20%...........30%..........40%...........50%...........60%..........70%...........80%...........90%...........100%

Welcome to Gradle 7.1.1!

Here are the highlights of this release:
 - Faster incremental Java compilation
 - Easier source set configuration in the Kotlin DSL

For more details see https://docs.gradle.org/7.1.1/release-notes.html

Starting a Gradle Daemon (subsequent builds will be faster)

> Task :compileJava

> Task :processResources
> Task :classes

> Task :bootJarMainClassName

> Task :bootJar
> Task :jar
> Task :assemble

BUILD SUCCESSFUL in 3m 20s
5 actionable tasks: 5 executed

Build step 'Invoke Gradle script' changed build result to SUCCESS

Finished: SUCCESS

