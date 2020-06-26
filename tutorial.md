# Curso de Git

## Division de un proyecto

1. _**Directorio de trabajo:**_ Es la carpeta de nuestra PC donde esta nuestro proyecto.
2. _**Área de ensayo**_ Es donde se cargan los archivos antes de pasar al repositorio local de nuestra PC.
3. _**Repositorio local:**_ Es el repositorio de nuestra PC donde se guardara nuestro proyecto, despues de pasar por el área de ensayo.
4. _**Repositorio Remoto**_ Es un paso adicional para subir nuestro repositorio local a un repositorio remoto como GitHub.

## Iniciar un proyecto

Para eso en consola escribimos:

```ps
git init
```

Esto solo se ejecutara una vez durante todo el proyecto.

Esto creara la rama _**(branch)**_ principal y tambien creara el repositorio local.

## Archivos que no tienen seguimiento.

En consola escribimos:

```ps
//Ver que archivos no han sido registrados
git status
```

tambien tenemos,

```ps
//Solo muestra los archivos modificados
git status -s
//Nos dara informacion si el archivo fue eliminado, creado o modificado
```

```ps
//Vemos informacion de la rama master
git status -s -b
//O tambien podemos usar
git status -sb
```

## Darle seguimiento a un archivo para agregarlo al área de ensayo (Area local).

En consola escribimos:

> Para seguir un solo archivo usamos:

```ps
git add nombreArchivo.extension
```

> Para seguir todos los archivos usamos:

```ps
git add .
```

## Pasar del Area Local al Repositorio local

Esto solo pasara los archivos que antes ya se les haya dado seguimiento con el comando _**git add**_.

En consola usamos

```ps
git commit -m "Aqui ira un mensaje para el commit"
```

## Mostrar una lista de los commits

Tenemos varias formas para mostrar una lista de los commits

> Muestra en una linea los commit realizados

```ps
git log --oneline
```

> Muestra en una linea los commit realizados pero mas elegantes

```ps
git log --oneline --decorate --all --graph
```

## Viajar a traves de los commit

Vamos a conocer como podemos movernos entre los diferentes commit que tengamos registrados, supongamos que tenemos los siguientes commit:

- f82f457 (HEAD -> master) mas comandos agregados
- f52f3da nuevos comandos en fundamentos.md
- e4ab8af mi primer commit

> Viajamos al commit en específico f52f3da y eliminamos los cambios futuros

```ps
//Este es el metodo principal
git reset --hard f52f3da
```

_**Nota1 :**_ Con esto pondremos el HEAD en la direccion del commit indicado y ya no mostraremos los que se encuentran por encima de el.

_**Nota 2:**_ Si queremos regresar a un commit superior tendriamos que recordar su identificador.

> Viajamos al commit en específico f52f3da

```ps
git reset --mixed f52f3da
```

> Muestra todos los cambios incluso si borramos los commit

```ps
git reflog
```

> Viajamos al commit en específico f52f3da y podemos restaurar los archivos

```ps
git reset --hard f52f3da
```

## Repositorio remoto

Para trabajar con github tenemos que poner la direccion URL del repositorio remoto con .git al final

```ps
git remote add origin https://github.com/malagamiguel/iniciogit.git
```

Para subir mi repositorio local al repositorio remoto usamos:

```ps
git push --force origin master
```

Listado de los git remote

```ps
git remote -v
```

Eliminar los git remote

```ps
git remote rm nombreDelRemote
```
