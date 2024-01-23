# Markdown
Un archivo de instrucciones, documentación, paso a seguir. Sintaxis de marcas. El hermano menor del html. Con markdown no puedo construir aplicaciones.

## h2
### h3
#### h4
##### h5
###### h6

## Listas ordenadas

1. Hola
2. Que
3. Tal

## Lista desordenada

* Item
* Item
* Item

## Links

<https://google.com.ar>

## Imagenes

![git](_ref/git.png)

## Separador

---

## Código

```js
function sumar(a, b){
    return a + b
}
```

```php
$nombre = "Kevin"
```

# GIT

## Configurando GIT
Esta configuración se realiza una vez. Y todos los repositorios que yo cree a partir de esta configuración todos los commits van a estar "firmados" por los datos "name" y "email"

```sh
git config --global user.name "Kevin Okulczyk"
```

```sh
git config --global user.email "kevin.okulczyk@gmail.com"
```

## Configurar un repositorio con otros datos de name y email.
Por repositorio. Primero tiene que existir el repositorio

```sh
git init
```

```sh
git config --local user.name "Kevin Leonel"
```

```sh
git config --local user.email "kevin.leonel@gmail.com"
```

## Verificar que se haya hecho bien la configuración

```sh
git config --get-regexp user
```

## Inicializando un repositorio de git

```sh
git init
```

## GIT STATUS (Es en que estado están los archivos)

```sh
git status
git status --short #versión resumida.
```

### Estados de los archivos

* untracked: Archivos que no se agregaron aún al sistema de git.
* unmodified: No cambiaron desde el último commit.
* modified: Si cambiaron respecto del último commit.
* staged: Zona temporal de confirmación de cambios.

### Estructura virtual de GIT

* Working Directory (WS): Zona de trabajo, de intercambio de archivos.
* Staging Area (SA): Zona donde los archivos están preparados para ser parte de un commit.
* Local Repo (LR): El área donde se guardan todos los commit. Los diferentes estados o cambios guardados en el tiempo.

## GIT ADD
Muevo los archivos del  área del Working Directory al área del Staging Area

```sh
git add <nombre-archivo>
git add README.md
git add . # Agrego todos los archivos
```

## GIT COMMIT 

```sh
git commit -m "<Mensaje explicativo de los cambios que tiene dentro el commit>"
git commit -m "<Guardando el archivo README.md hasta estados de archivos y estructura>"
```

## GIT DIFF

Es ver la diferencia entre el archivo que fue modificado en (WD) con respecto a la versión del archivo que está guardado en (LR)

```sh
git diff # Para salir de este comando "q" -> quit
```
## Ver el listado de commits (Ver la caja de fotos)

```sh
git log
```
