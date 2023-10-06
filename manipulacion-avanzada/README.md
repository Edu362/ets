<div align="justify">

# Manipulación Avanzada en Git

Eduardo González Expósito

## Indice
- [Trabajando con Git](#trabajando-con-git)
- [Ejercicio 1](#ejercicio1)
- [Ejercicio 2](#ejercicio2)
- [Ejercicio 3](#ejercicio3)
- [Ejercicio 4](#ejercicio4)
- [Ejercicio 5](#ejercicio5)
- [Ejercicio 6](#ejercicio6)
- [Ejercicio 7](#ejercicio7)
- [Ejercicio 8](#ejercicio8)
- [Ejercicio 9](#ejercicio9)

## Trabajando con Git <a name="trabajando-con-git"></a>

Para realizar el ejercicio clone el repositorio libro mediante el comando: 
__git clone https://github.com/jpexposito/libro.git__, y entre al directorio libro con el comando __cd libro__.


>Nota: __ls -la__, con este comando muestro el contenido del directorio

- salida:

```code
  total 28
  drwxrwxr-x  6 eduglezexp eduglezexp 4096 oct  6 11:17 .
  drwxr-x--- 25 eduglezexp eduglezexp 4096 oct  6 11:17 ..
  drwxrwxr-x  8 eduglezexp eduglezexp 4096 oct  6 11:17 .git
  drwxrwxr-x  2 eduglezexp eduglezexp 4096 oct  6 11:17 img
  drwxrwxr-x  2 eduglezexp eduglezexp 4096 oct  6 11:17 prueba2
  -rw-rw-r--  1 eduglezexp eduglezexp   66 oct  6 11:17 README.md
  drwxrwxr-x  2 eduglezexp eduglezexp 4096 oct  6 11:17 test
```

## Ejercicio 1 <a name="ejercicio1"></a>

- Para mostrar el historial de cambios del repositorio, usaremos el siguiente comando:

```code 
  git log
```
- salida:

```code 
  commit 1016a8a4e53ee1167750094aaac7d2018063a264 (HEAD -> main, origin/main, origin/HEAD)
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Wed Sep 27 15:50:15 2023 +0100

      se añade la segunda carpeta

  commit 3f26704336e8d586f91aca272c89218d96e61d98
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Wed Sep 27 15:21:53 2023 +0100

      mensaje

  commit 8a81c55462cc731099b5842f2cd38fbc47105d56
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Mon Oct 10 18:18:08 2022 +0100

      Se añade un título

  commit fbe91b280cfbc50352ee18627a4339d4aa7e91c4
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Mon Oct 10 18:14:01 2022 +0100

  :
```
>Nota: Recuerda pulsar __q__ para salir

- Para crear la carpeta capítulos y crear dentro de ella el fichero capitulo1.txt con el siguiente texto:

```code
  Git es un sistema de control de versiones ideado por Linus Torvalds.
```
- Usaremos el siguiente comando para crear la carpeta:

```code
  mkdir capitulos
```
- salida:

```code
  Aunque no nos muestre nada en la terminal, se ha creado la carpeta capitulos
```

- Usaremos el siguiente comando para crear el fichero __capitulo1.txt__ y añadirle el texto: Git es un sistema de control de versiones ideado por Linus Torvalds.

```code
  cat > capitulos/capitulo1.txt
  Git es un sistema de control de versiones ideado por Linus Torvalds.
```

- Cuando pulsemos enter, después de poner el comando __cat > capitulos/capitulo1.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -m "Añadido capítulo 1."
```
- salida:

```code
  [main e3f2ab0] Añadido capítulo 1.
  1 file changed, 1 insertion(+)
  create mode 100644 capitulos/capitulo1.txt
```

- Vuelvo a usar el comando __git log__ para ver el historial de cambios.
- salida:

```code
  commit e3f2ab0e84a36e5db0e07db93d7735778f6eba9c (HEAD -> main)
  Author: eduglezexp <eduex04@gmail.com>
  Date:   Fri Oct 6 12:37:17 2023 +0100

      Añadido capítulo 1.

  commit 1016a8a4e53ee1167750094aaac7d2018063a264 (origin/main, origin/HEAD)
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Wed Sep 27 15:50:15 2023 +0100

      se añade la segunda carpeta

  commit 3f26704336e8d586f91aca272c89218d96e61d98
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Wed Sep 27 15:21:53 2023 +0100

      mensaje

  commit 8a81c55462cc731099b5842f2cd38fbc47105d56
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Mon Oct 10 18:18:08 2022 +0100

      Se añade un título
  :
```
>Nota: recuerda usar Ctrl+D para salir.

## Ejercicio 2 <a name="ejercicio2"></a>

- Para crear el fichero capitulo2.txt en la carpeta capítulos con el siguiente texto:

```code
  El flujo de trabajo básico con Git consiste en: 1- Hacer cambios en el repositorio. 2- Añadir los cambios a la zona de intercambio temporal. 3- Hacer un commit de los cambios.
```

- Usamos el siguiente comando para crear la carpeta con el fichero y añadir el texto:

```code
  cat > capitulos/capitulo2.txt
  El flujo de trabajo básico con Git consiste en:
  1- Hacer cambios en el repositorio.
  2- Añadir los cambios a la zona de intercambio temporal.
  3- Hacer un commit de los cambios.
```
- Cuando pulsemos enter, después de poner el comando __cat > capitulos/capitulo2.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -m "Añadido capítulo 2."
```
- salida:

```code
  [main ef3211b] Añadido capítulo 2.
  1 file changed, 3 insertions(+)
  create mode 100644 capitulos/capitulo2.txt
```

- Ahora con HEAD, apuntamos al último cambio del repositorio. 

```code
  diff --git a/capitulos/capitulo1.txt b/capitulos/capitulo1.txt
  new file mode 100644
  index 0000000..7431f9e
  --- /dev/null
  +++ b/capitulos/capitulo1.txt
  @@ -0,0 +1 @@
  +Git es un sistema de control de versiones ideado por Linus Torvalds.
  diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
  new file mode 100644
  index 0000000..c3408d0
  --- /dev/null
  +++ b/capitulos/capitulo2.txt
  @@ -0,0 +1,3 @@
  +1- Hacer cambios en el repositorio.
  + 2- Añadir los cambios a la zona de intercambio temporal.
  + 3- Hacer un commit de los cambios.
```

## Ejercicio 3 <a name="ejercicio3"></a>

- Para crear el fichero capitulo3.txt en la carpeta capítulos con el siguiente texto:

```code
  Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
```

- Usamos el siguiente comando para crear la carpeta con el fichero y añadir el texto:

```code
  cat > capitulos/capitulo3.txt
  Git permite la creación de ramas lo que permite tener distintas versiones del mismo proyecto y trabajar de manera simultanea en ellas.
```
- Cuando pulsemos enter, después de poner el comando __cat > capitulos/capitulo3.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -m "Añadido capítulo 3."
```
- salida:

```code
  [main de2cf37] Añadido capítulo 3.
  1 file changed, 3 insertions(+)
  create mode 100644 capitulos/capitulo3.txt
```

- Para mostrar las diferencias entre la primera y la última versión del repositorio, uso los siguientes comandos:

```code
  git log 
  git diff <codigo hash de la primera version>..HEAD
```

- git log
- salida:

```code 
  commit de2cf3703add8cfbe6a1d3a1096d3b2851a9440f (HEAD -> main)
  Author: eduglezexp <eduex04@gmail.com>
  Date:   Fri Oct 6 16:36:26 2023 +0100

      Añadido capítulo 3.

  commit ef3211be31da01c7f85a3271c8d06316dcca96d7
  Author: eduglezexp <eduex04@gmail.com>
  Date:   Fri Oct 6 13:14:24 2023 +0100

      Añadido capítulo 2.

  commit e3f2ab0e84a36e5db0e07db93d7735778f6eba9c
  Author: eduglezexp <eduex04@gmail.com>
  Date:   Fri Oct 6 12:37:17 2023 +0100

      Añadido capítulo 1.

  commit 1016a8a4e53ee1167750094aaac7d2018063a264 (origin/main, origin/HEAD)
  Author: Joatham Pérez Expósito <jpe.gsc@gmail.com>
  Date:   Wed Sep 27 15:50:15 2023 +0100

      se añade la segunda carpeta
  :
```

- git diff HEAD~3..HEAD
- salida:

```code 
  diff --git a/capitulos/capitulo1.txt b/capitulos/capitulo1.txt
  new file mode 100644
  index 0000000..7431f9e
  --- /dev/null
  +++ b/capitulos/capitulo1.txt
  @@ -0,0 +1 @@
  +Git es un sistema de control de versiones ideado por Linus Torvalds.
  diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
  new file mode 100644
  index 0000000..c3408d0
  --- /dev/null
  +++ b/capitulos/capitulo2.txt
  @@ -0,0 +1,3 @@
  +1- Hacer cambios en el repositorio.
  + 2- Añadir los cambios a la zona de intercambio temporal.
  + 3- Hacer un commit de los cambios.
  diff --git a/capitulos/capitulo3.txt b/capitulos/capitulo3.txt
  new file mode 100644
  index 0000000..4a8b62a
  --- /dev/null
  +++ b/capitulos/capitulo3.txt
  @@ -0,0 +1,3 @@
  +Git permite la creación de ramas lo que permite tener distintas versiones del m
  :  
```
>Nota: Recuerda usar __q__ para salir.

## Ejercicio 4 <a name="ejercicio4"></a>

- Para crear el fichero índice.txt con la siguiente línea:

```code
  Indice de los cápitulos, con conceptos avanzados de git
```
- Usamos el siguiente comando para crear el fichero indice.txt:

```code
   cat > indice.txt
```
- Cuando pulsemos enter, después de poner el comando __cat > indice.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -m "Se crea el indice." 
   echo "Indice de los cápitulos, con conceptos avanzados de git" >> indice.txt
```
- salida:

```code
  [main 320ebb6] Se crea el indice.
  1 file changed, 2 insertions(+)
  create mode 100644 indice.txt
```

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
  [main 1bbe722] Añadido el índice .
  1 file changed, 1 insertion(+)
```

- Usamos el siguiente comando para ver el contenido del fichero indice.txt con anotaciones en cada línea con la información del commit que se introdujo.

```code
  320ebb60        (eduglezexp     2023-10-06 17:08:07 +0100       1)Indice de los cápitulos, con conceptos avanzados de git
```

## Ejercicio 5 <a name="ejercicio5"></a>

- Usamos el siguiente comando para crear la rama bibliografía:

```code
  Aunque no aparezca nada en la terminal, se ha creado la rama bibliografía
```

- Para mostrar las ramas del repositorio, uso este comando:

```code
  git branch -av  
```
- salida:

```code
    bibliografia        1bbe722 Añadido el índice .
  * main                1bbe722 [adelante 5] Añadido el índice .
    remotes/origin/1    3ea9800 se crea la carpeta img #1
    remotes/origin/HEAD -> origin/main
    remotes/origin/main 1016a8a se añade la segunda carpeta
```

## Ejercicio 6 <a name="ejercicio6"></a>

- Para crear el fichero capitulos/capitulo4.txt y añadir el texto siguiente, se usa el siguiente comando:

```code
  cat > capitulos/capitulo4.txt
  En este capítulo veremos cómo usar GitHub para alojar repositorios en remoto.
```

- Cuando pulsemos enter, después de poner el comando __cat > capitulos/capitulo4.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -m "Añadido capítulo 4."
```
- salida:

```code
  En la rama main
  Tu rama está adelantada a 'origin/main' por 6 commits.
    (usa "git push" para publicar tus commits locales)

  nada para hacer commit, el árbol de trabajo está limpio
```

- El siguiente comando nos muestra un __--log__ para ver el historial de cambios incluyendo todas las ramas, __--graph__ nos lo muestra como un gráfico y __--oneline__ nos muestra un commit por línea, 

```code 
  git log --graph --all --oneline
```
- salida:

```code
  * b56b473 (HEAD -> main) Añadido capítulo 4.
  * 1bbe722 (bibliografia) Añadido el índice .
  * 320ebb6 Se crea el indice.
  * de2cf37 Añadido capítulo 3.
  * ef3211b Añadido capítulo 2.
  * e3f2ab0 Añadido capítulo 1.
  * 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
  * 3f26704 mensaje
  * 8a81c55 Se añade un título
  * fbe91b2 closed #1
  * 3ea9800 (origin/1) se crea la carpeta img #1
  * 4dcb74b Initial commit
```

## Ejercicio 7 <a name="ejercicio7"></a>

- para cambiar a la rama bibliografía, usamos el siguiente comando:

```code
  git checkout bibliografia
```
- salida:

```code
  Cambiado a rama 'bibliografia'
```

- Para crear el fichero cat > bibliografia.txt, se usa el siguiente comando:

```code
  cat > bibliografia.txt
  - Chacon, S. and Straub, B. Pro Git. Apress.
```

- Cuando pulsemos enter, después de poner el comando __cat > bibliografia.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

```code
  Usare git add . para añadir el elemento.
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -m "Añadida primera referencia bibliográfica."
```
- salida:

```code
  [bibliografia 27ee86c] Añadida primera referencia bibliográfica.
  1 file changed, 1 insertion(+)
  create mode 100644 bibliografia.txt
```

- El siguiente comando nos muestra un __--log__ para ver el historial de cambios incluyendo todas las ramas, __--graph__ nos lo muestra como un gráfico y __--oneline__ nos muestra un commit por línea,

```code 
  git log --graph --all --oneline
```
- salida:

```code
  * 27ee86c (HEAD -> bibliografia) Añadida primera referencia bibliográfica.
  | * b56b473 (main) Añadido capítulo 4.
  |/  
  * 1bbe722 Añadido el índice .
  * 320ebb6 Se crea el indice.
  * de2cf37 Añadido capítulo 3.
  * ef3211b Añadido capítulo 2.
  * e3f2ab0 Añadido capítulo 1.
  * 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
  * 3f26704 mensaje
  * 8a81c55 Se añade un título
  * fbe91b2 closed #1
  * 3ea9800 (origin/1) se crea la carpeta img #1
  * 4dcb74b Initial commit
```

## Ejercicio 8 <a name="ejercicio8"></a>

- Para fusionar la rama bibliografía con la rama main, usaremos los siguientes comandos:

```code
  git checkout main
  git merge bibliografia
```

- Usamos __git checkout main__, para cambiar a la rama main.

- salida:

```code 
  Cambiado a rama 'main'
  Tu rama está adelantada a 'origin/main' por 6 commits.
  (usa "git push" para publicar tus commits locales)
```

- Usamos __git merge bibliografia__ para fusionar la rama.
- salida:

```code 
  Merge made by the 'ort' strategy.
  bibliografia.txt | 1 +
  1 file changed, 1 insertion(+)
  create mode 100644 bibliografia.txt
```

- El siguiente comando nos muestra un __--log__ para ver el historial de cambios incluyendo todas las ramas, __--graph__ nos lo muestra como un gráfico y __--oneline__ nos muestra un commit por línea,

```code 
  git log --graph --all --oneline
```
- salida:

```code
  *   6f1792b (HEAD -> main) Merge branch 'bibliografia'
  |\  
  | * 27ee86c (bibliografia) Añadida primera referencia bibliográfica.
  * | b56b473 Añadido capítulo 4.
  |/  
  * 1bbe722 Añadido el índice .
  * 320ebb6 Se crea el indice.
  * de2cf37 Añadido capítulo 3.
  * ef3211b Añadido capítulo 2.
  * e3f2ab0 Añadido capítulo 1.
  * 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
  * 3f26704 mensaje
  * 8a81c55 Se añade un título
  * fbe91b2 closed #1
  * 3ea9800 (origin/1) se crea la carpeta img #1
  * 4dcb74b Initial commit
```

- Usamos __git branch -d bibliografia__, para eliminar la rama bibliografia.
- salida:

```code
  Eliminada la rama bibliografia (era 27ee86c).
```

- El siguiente comando nos muestra un __--log__ para ver el historial de cambios incluyendo todas las ramas, __--graph__ nos lo muestra como un gráfico y __--oneline__ nos muestra un commit por línea,

```code 
  git log --graph --all --oneline
```
- salida:

```code
  *   6f1792b (HEAD -> main) Merge branch 'bibliografia'
  |\  
  | * 27ee86c Añadida primera referencia bibliográfica.
  * | b56b473 Añadido capítulo 4.
  |/  
  * 1bbe722 Añadido el índice .
  * 320ebb6 Se crea el indice.
  * de2cf37 Añadido capítulo 3.
  * ef3211b Añadido capítulo 2.
  * e3f2ab0 Añadido capítulo 1.
  * 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
  * 3f26704 mensaje
  * 8a81c55 Se añade un título
  * fbe91b2 closed #1
  * 3ea9800 (origin/1) se crea la carpeta img #1
  * 4dcb74b Initial commit
```

## Ejercicio 9 <a name="ejercicio9"></a>

- Para crear la rama bibliografía, usamos el siguiente comando:

```code
  git branch bibliografia
```
- salida:

```code 
  Aunque no se muestre en la terminal, se creo la rama bibliografía
```

- Para cambiar a la rama bibliografía, usamos el siguiente comando:

```code
  git checkout bibliografia
```
- salida:

```code
  Cambiado a rama 'bibliografia'
```
- Cambiar el fichero bibliografia.txt para que contenga las siguientes referencias:

```code
  Scott Chacon and Ben Straub. Pro Git. Apress.
  Ryan Hodson. Ry’s Git Tutorial. Smashwords (2014)
```

- Para eso usaremos el siguiente comando:

```code
  cat > bibliografia.txt
  - Scott Chacon and Ben Straub. Pro Git. Apress.
  - Ryan Hodson. Ry's Git Tutorial. Smashwords (2014)
```

- Cuando pulsemos enter, después de poner el comando __cat > bibliografia.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
   git commit -a -m "Añadida nueva referencia bibliográfica."
```
- salida:

```code
  [bibliografia 2419871] Añadida nueva referencia bibliográfica.
  1 file changed, 2 insertions(+), 1 deletion(-)
```

- Usamos __git checkout main__, para cambiar a la rama main.
- salida:

```code
  Cambiado a rama 'main'
  Tu rama está adelantada a 'origin/main' por 8 commits.
  (usa "git push" para publicar tus commits locales)
```

- Cambiar el fichero bibliografia.txt para que contenga las siguientes referencias:

```code
  Chacon, S. and Straub, B. Pro Git. Apress.
  Loeliger, J. and McCullough, M. Version control with Git. O’Reilly.
```

- Para ello, usaremos el siguiente comando:

```code
  cat > bibliografia.txt
  - Chacon, S. and Straub, B. Pro Git. Apress.
  - Loeliger, J. and McCullough, M. Version control with Git. O'Reilly.
```

- Cuando pulsemos enter, después de poner el comando __cat > bibliografia.txt__, nos dejara introducir el texto, recuerda usar el Ctrl+D para salir.

- Añado un mensaje de lo hecho, con el siguiente comando:__

```code
   git commit -a -m "Añadida nueva referencia bibliográfica."
```
- salida:

```code
  [main 4ac7d74] Añadida nueva referencia bibliográfica.
  1 file changed, 2 insertions(+), 1 deletion(-)
```

- Usamos __git merge bibliografia__ para fusionar la rama.
- salida:

```code 
  Auto-fusionando bibliografia.txt
  CONFLICTO (contenido): Conflicto de fusión en bibliografia.txt
  Fusión automática falló; arregle los conflictos y luego realice un commit con el resultado.
```

- Para resolver el conflicto con el fichero bibliografia.txt con las referencias, usaremos el siguiente comando:

```code
  git add bibliografia.txt
```

- salida: 

```code
  En la rama main
  Tu rama está adelantada a 'origin/main' por 9 commits.
    (usa "git push" para publicar tus commits locales)

  Todos los conflictos resueltos pero sigues fusionando.
    (usa "git commit" para concluir la fusión)

  Cambios a ser confirmados:
	  modificados:     bibliografia.txt
```

- Añado un mensaje de lo hecho, con el siguiente comando:

```code
  git commit -a -m "Solucionado conflicto bibliografía."
```
- salida:

```code
  git commit -a -m "Solucionado conflicto bibliografía."
```

- El siguiente comando nos muestra un __--log__ para ver el historial de cambios incluyendo todas las ramas, __--graph__ nos lo muestra como un gráfico y __--oneline__ nos muestra un commit por línea,

```code 
  git log --graph --all --oneline
```
- salida:

```code
  *   95911d7 (HEAD -> main) Solucionado conflicto bibliografía.
  |\  
  | * 2419871 (bibliografia) Añadida nueva referencia bibliográfica.
  * | 4ac7d74 Añadida nueva referencia bibliográfica.
  |/  
  *   6f1792b Merge branch 'bibliografia'
  |\  
  | * 27ee86c Añadida primera referencia bibliográfica.
  * | b56b473 Añadido capítulo 4.
  |/  
  * 1bbe722 Añadido el índice .
  * 320ebb6 Se crea el indice.
  * de2cf37 Añadido capítulo 3.
  * ef3211b Añadido capítulo 2.
  * e3f2ab0 Añadido capítulo 1.
  * 1016a8a (origin/main, origin/HEAD) se añade la segunda carpeta
  * 3f26704 mensaje
  * 8a81c55 Se añade un título
  * fbe91b2 closed #1
  * 3ea9800 (origin/1) se crea la carpeta img #1
  * 4dcb74b Initial commit
```

</div>