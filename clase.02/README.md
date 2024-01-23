# Clase 02

## .gitignore
Es un archivo que me permite indicarle a git que ignore un archivo, una carpeta.
Se crea en la raíz del proyecto.

## .gitkeep
Me permite darle seguimiento a carpetas que no tiene ningún archivo, ni necesitan tener algún archivo al subirlo. O sea me permite darle segumiento a carpetas vacías.

## Corregir el mensaje del último commit.

```sh
git commit --amend -m <nuevo-mensaje-o-mensaje-corregido>
```

## GIT RESTORE
Me permite recuperar información que está guardada en el repo y además me permite mover los archivos entre el área de working directory y staging area.


```sh
git restore --staged <archivo> # Sacar del staging area los cambios y dejarlos en el working directory
git store --staged README.md
```

```sh
git restore --staged <archivo> # Recuperar del último commit un archivo en específico
git store --staged README.md
```

## Ver información de los commits

```sh
git show <hash>
git show 10769e2
```

## Agregando y subiendo al remoto nuestros cambios (Nuestro repositorio)

## Crer repositorio

## Configurar en el local la url del remoto
> Agrego url del remoto
```sh
git remote add <alias> <url>
git remote add origin https://github.com/kevinok124/guia-git.git

```

> Quito url del remoto
```sh
git remote remove <alias>
git remote remove origin
```

## Git PUSH: Subir al remoto
Subir al remoto los cambios locales

```sh
# La primera vez que subo una rama al remoto
git push -u <remoto> <rama-local>
git push -u origin main

## La segunda y subsiguientes
git push
```

## GIT FETCH: Trae la metadata del repositorio remoto al local
Me actualiza la metadata del repositorio local con la metadata del repositorio remoto

```sh
git fetch
```

## GIT PULL: Me trae los cambios ocurridos en los archivos

```sh
git pull
```

## Ver ramas locales y remotas

```sh
git branch -av
```
