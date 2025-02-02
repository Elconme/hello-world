# hello-world

Un repositorio para empezar a usar Github y Github Actions con Java

## ¿Como probar en el cloud?

[![](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/gitt-3-pat/hello-world)

## Comandos git básicos
* git clone - Se emplea para clonar repositorios en un nuevo directorio. En nuestro caso esta acción
              se llevó a cabo desde Get from VCS, sin emplear el comando.
* git status - Muestra la información sobre la rama actual: si está actualizada, si se debe confirmar, enviar o
               recibir algo (pull) o si hay archivos creados, modificados o eliminados entre otras cosas.

               Logs:
                    PS C:\Users\Elena\IdeaProjects\hello-world> git status
                    On branch main
                    Your branch is up to date with 'origin/main'.

                    Changes to be committed:
                      (use "git restore --staged <file>..." to unstage)
                            deleted:    Conderana.txt
                            new file:   Practica0.txt

                    Changes not staged for commit:
                      (use "git add <file>..." to update what will be committed)
                      (use "git restore <file>..." to discard changes in working directory)
                            modified:   Practica0.txt

* git add - Incluye los cambios (creación, modificación o eliminación) realizados en el directorio local en el próximo commit.
            Puede realizarse un add genérico indicado por un punto (.) o uno concreto indicando el nombre del archivo en cuestión.

            Logs:
                PS C:\Users\Elena\IdeaProjects\hello-world> git add .
                warning: LF will be replaced by CRLF in Practica0.txt.
                The file will have its original line endings in your working directory

* git commit - Guarda los cambios realizados en el repositorio local junto con una breve descripción.
                Opción -m -> incluye una breve descripción de los cambios que se están realizando entre ""

           Logs:
               PS C:\Users\Elena\IdeaProjects\hello-world> git commit -m "Practica 0"
               [main d74bd32] Practica 0
                2 files changed, 69 insertions(+), 26 deletions(-)
                delete mode 100644 Conderana.txt
                create mode 100644 Practica0.txt

* git push - Carga contenido del repositorio local a un repositorio remoto en nuestro caso a nuestro repositorio hello world de Github

           Logs:
               PS C:\Users\Elena\IdeaProjects\hello-world> git push
               Enumerating objects: 4, done.
               Counting objects: 100% (4/4), done.
               Delta compression using up to 8 threads
               Compressing objects: 100% (3/3), done.
               Writing objects: 100% (3/3), 1.44 KiB | 1.44 MiB/s, done.
               Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
               remote: Resolving deltas: 100% (1/1), completed with 1 local object.
               To https://github.com/Elconme/hello-world.git
                  1b16956..d74bd32  main -> main

* git checkout - permite cambiar entre ramas y comprobar archivos y commits.

           Logs:
               PS C:\Users\Elena\IdeaProjects\hello-world> git checkout
               Your branch is ahead of 'origin/main' by 1 commit.
                 (use "git push" to publish your local commits)

** Comandos extra de interés **

* git branch - permite mostrar, crear y borrar ramas.
               En nuestro repositorio únicamente existe la rama main.
        Logs:
            PS C:\Users\Elena\IdeaProjects\hello-world> git branch
            * main

* git pull - se emplea para recibir actualizaciones del repositorio remoto, se trata de una especie de git push inverso

       Logs:
           PS C:\Users\Elena\IdeaProjects\hello-world> git pull
           Already up to date.

* git log - se emplea para explorar el historial de commits del repositorio, en particular, si añadimos
            --oneline se lanzará el log en una única línea, permitiendo seguir con mayor facilidad la
            secuencia de commits.

       Logs:
           PS C:\Users\Elena\IdeaProjects\hello-world> git log --oneline
           552a8d6 (HEAD -> main, origin/main, origin/HEAD) Practica0.txt
           466d2a4 Practica0.txt
           f9b8d47 Practica0.txt
           d74bd32 Practica 0
           1b16956 practica 0
           134f825 nombre
           48fe276 Merge pull request #1 from gitt-3-pat/feature/1
           5b68377 Primera iteracion

## Entorno de desarrollo JVM: 

    * Java 17
        Logs:
            java version "17.0.1" 2021-10-19 LTS
    * Maven
        Logs:
            [INFO] ------------------------------------------------------------------------
            [INFO] BUILD SUCCESS
            [INFO] ------------------------------------------------------------------------
            [INFO] Total time:  6.651 s
            [INFO] Finished at: 2022-01-21T19:23:56+01:00
            [INFO] ------------------------------------------------------------------------
