---
title: Copinchapedia Offline
description: Copinchapedia Offline
published: true
date: 2020-12-15T22:17:27.185Z
tags: copinchapedia
editor: markdown
dateCreated: 2020-12-15T22:10:49.449Z
---

# Copinchapedia Offline


## Exploración de versión fuera de línea

Luego de la charla con motivo del DOTS, se pensó en una variante de la Copinchapedia

Las tecnologías que vamos a empezar! a explorar serán:

 * [TiddlyWiki]().
 * [Fossil](./fossil).
 * [Markdown](./markdown)
 * Y migraremos desde Wiki.js

## Instalación de Software


Instalaremos el gestor de paquetes [Scoop](https://scoop.sh/).

1. Abrimos PowerShell.
2. Escrimos lo siguiente

    ```bash=
    iwr -useb get.scoop.sh | iex
    ```
   **Nota*: En caso de que nos diga que requiere de unos permisos particulares, 
   escribimos:
   
   ```bash=
   Set-ExecutionPolicy RemoteSigned -scope CurrentUser
   ```
   
## Fossil


### Instalación

Una vez hayamos instalado scoop, desde PowerShell escribimos:

```bash=
scoop install fossil
```

## Repositorio

La Copinchapedia tiene un repositorio de Fossil para guardar su contenido
y colaborar con el mismo.

La ubicación es:

https://mutabit.com/repos.fossil/copincha/

Si navegamos los archivo (Files) en la opción vista de arbol (Tree View) veremos algo como esto:

![upload_030ce64117e58e9cfde32770c785bd1e.png](/c9ff8db944e24aba92a57cbb1e89bd0e.png)

Hay varias formas de descargar el contenido.

Una es crear este enlace:

  * Repositorio base + `zip`
  * https://mutabit.com/repos.fossil/copincha/zip

La otra posibilidad, si se tiene Fossil, se conoce como clonar el repositorio.
Para eso hacemos lo siguiente

  1. Abrimos PowerShell
  2. Creamos una carpeta para el repositorio:

     ```bash=
     mkdir Desktop/Copincha
     ```

  3. Nos ubicamos en la carpeta que acabamos de crear:

     ```bash=
     cd Desktop/Copincha
     ```

  4. Clonamos el repositorio desde su ubicación en Internet a un archivo en
     nuestro disco duro:
     
     ```bash=
     fossil clone https://mutabit.com/repos.fossil/copincha/ copincha.fossil
     ```
     
     Puede que Fossil nos pida que aceptemos la identidad del provedor de 
     repositorios y que si queremos recordar esta decisión 
     
     :::info
     El nombre del repositorio puede ser cualquiera, pero por convención suelen
     terminar en `.fossil`. En este archivo es como un arhivo comprimido 
     (por ejemplo los `.zip`) todos archivos y también su historia.
     Donde lo pasemos, viajará con nosotr@s, incluyendo 
     :::
     
  5. Abrimos el archivo `.fossil` con el siguiente comando:

     ```bash=
     fossil open --force copincha.fossil
     ```

Fossil contiene u peuqeño servidor web incluido de manera que podemos ver
lo mismo que está en Internet, pero en nuestras propias máquinas.
Para lanzarlo, desde una carpeta donde tengamos abierto un repositorio,
ejecutamos este comando:

```bash=
fossil ui
```

### Agregar archivos

La manera clásica de trabajar es hacer cambios locales al repositorio
(en nuestra propia máquina) y luego sincronizarlos con Internet.
Veámoslo a continuación.

Agregamos un archivo a la carpeta de contenidos. Y luego desde el PowerShell
hacemos:

```bash=
fossil add contenidos/{arhivo.md}
```

Reemplazando lo que está en los corchetes por el nombre del archivo (y sin
incluir los corchetes).
Por ejemplo `pruebas.md` el comando sería:

```bash=
fossil add contenidos/pruebas.md
```

Debe salir similar a este:

```bash=
ADDED contenidos/prubas.md
```

:::info
:::


## Hacer un _commit_

Una vez hemos agregado los archivos para hacer que sus cambios hagan
parte del histórico, hacemos un _commit_.

Ubicados en PowerShell o Terminarl, en la carpeta donde tenemos _abierto_ el 
repositorio, ejecutamos el siguiente comando:

```bash=
fossil commit -m "{comentario personalizado}."
```

donde `{comentario personalizado}` lo cambiamos por lo que queramos decir
que describa los cambios que queremos enviar al repositorio.
Por ejemplo:

```bash=
fossil commit -m "Agregando archivo de pruebas."
```

Nos dirá que cambio fue exitoso y **si no nos hemos registrado en el 
repositorio remoto**, nos dira que el cambio ha sido únicamente local.

Recarguemos la línea de tiempo en el navegador en nuestra máquina local
(luego de ejecutar `fossil ui`) y veremos el cambio que acabamos de hacer.

El siguiente paso será sincronizar los repositorios locales y remotos.

## Sincronización de repositorios

:::info
La sincronización se hace una sola vez y luego 
:::


Para sincronizar dos repositorios debemos tener un usuario en un
repositorio, que sirve para coordinar los demas repositorios
(pero podría hacerse entre pares en una intranet por ejemplo).

Entramos a:

https://mutabit.com/repos.fossil/copincha/register

y llenamos los datos.
Luego le pedimos a alguno de los administradores que nos de permisos de
Desarrollador (y eventualmente para subir archivos no versionados).
El listado de capacidades del nuevo usuario debe lucir así:

![09682bb7f0ec419c9f2ede397e2734d7.png](/09682bb7f0ec419c9f2ede397e2734d7.png)

:::info
**Importante** Los derechos de *Admin* Administrador y *Setup* deben otorgarse
de manera moderada, pues se usan para dar la mayor cantidad de privilegios
sobre el repositorio y capacidad de gestionar a otros usuarios.
:::

Una vez tengamos los permisos de desarrollador lo que hacemos es que
sincronizamos nuestro repositorio local y el remoto.

```bash=
fossil sync https://{usuario}@mutabit.com/repos.fossil/copincha/
```

Por ejemplo si el usuario es `colabora` el comando debería ser:

```bash=
fossil sync https://colabora@mutabit.com/repos.fossil/copincha/
```


Nos pedirá la contraseña con la que nos registramos en el repositorio.

Si miramos la [línea de tiempo del servidor](https://mutabit.com/repos.fossil/copincha/timeline) 
veremos:

## Actualizaciones

Para ello sólo hacemos 



## Archivos no versionados

Son archivos que están en el repositorio pero de los cuales no se controlan
versiones y por tanto no se tiene registro de los cambios.
Son útiles para guardar los llamados archivos _raster_ (imágnes, audio,
video, PDF) que no se pueden representar bien mediante el texto plano
(como sí ocurre Markdown, SVG, HTML).

:::info
Lo idea es que los archivos más pesados, (ejp audio y video) se encuentren
fuera del repositorio.
:::

Para subir archivos no versionados crearemos una carpeta donde estén
todos ellos.
Nuestra manera de organizar la información será así:

```bash=
contenidos/
medios/
```

Para tener esta jerarquía vamos a hacer lo siguente:

```bash=
mkdir medios
```

Y arrastramos o copiamos un archivo de imagen allí, por ejemplo
`copincha-logo.png`, con lo cual nuestro contenid debería verse así

```bash=
contenidos/
medios/
  copincha-logo.png
```

Agregaremos esa imágen como archivo no versionado:

```bash=
fossil uv add medios/copincha-logo.png
```

Y luego subimos el archivo no versionado con este comando:

```bash=
fossil uv sync -v
```

Nos indicará que la operación de sincronización terminó y podremos ver
el archiv no versionado:

 * ubicación remota: https://mutabit.com/repos.fossil/copincha/uv 
 * ubicación local: https://localhost:8080/copincha/uv

Hay dos formas de hacer vínculos a estos archivos, con su dirección absoluta
y con su dirección relativa.

 * La absoluta es: https://mutabit.com/repos.fossil/copincha/uv/medios/08a285e31f40435b910a3006f59caeab.jpg

Con lo cual se puede hacer un enlace de imáge así:

`![](https://mutabit.com/repos.fossil/copincha/uv/medios/08a285e31f40435b910a3006f59caeab.jpg)`

Lo que mostraría esto:

![](https://mutabit.com/repos.fossil/copincha/uv/medios/08a285e31f40435b910a3006f59caeab.jpg)


## Administración del repositorio

