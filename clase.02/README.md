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