# Curso de Git

---

## Division de un proyecto

---

1. _**Directorio de trabajo:**_ Es la carpeta de nuestra PC donde esta nuestro proyecto.
2. _**Área de ensayo**_ Es donde se cargan los archivos antes de pasar al repositorio local de nuestra PC.
3. _**Repositorio local:**_ Es el repositorio de nuestra PC donde se guardara nuestro proyecto, despues de pasar por el área de ensayo.
4. _**Repositorio Remoto**_ Es un paso adicional para subir nuestro repositorio local a un repositorio remoto como GitHub.

---

## Iniciar un proyecto

---

Para eso en consola escribimos:

```sh
git init
```

Esto solo se ejecutara una vez durante todo el proyecto.

Esto creara la rama _**(branch)**_ principal y tambien creara el repositorio local.

---

## Archivos que no tienen seguimiento.

---

En consola escribimos:

```sh
//Ver que archivos no han sido registrados
git status
```

tambien tenemos,

```sh
//Solo muestra los archivos modificados
git status -s
//Nos dara informacion si el archivo fue eliminado, creado o modificado
```

```sh
//Vemos informacion de la rama master
git status -s -b
//O tambien podemos usar
git status -sb
```

---

## Darle seguimiento a un archivo para agregarlo al área de ensayo (Area local).

---

En consola escribimos:

> Para seguir un solo archivo usamos:

```sh
git add nombreArchivo.extension
```

> Para seguir todos los archivos usamos:

```sh
git add .
```

---

## Pasar del Area Local al Repositorio local

---

Esto solo pasara los archivos que antes ya se les haya dado seguimiento con el comando _**git add**_.

En consola usamos

```sh
git commit -m "Aqui ira un mensaje para el commit"
```
