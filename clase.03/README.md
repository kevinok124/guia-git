# Clase 03

## RAMAS (Branches)

![Ramas](_ref/ramas.png)

### Crear una rama

```sh
git branch <nombre-rama>
git branch dev
```

### Listar las ramas

```sh
git branch
```

### Moverme de rama

```sh
git switch <nombre-rama>
git switch dev
git switch - #~Tooglea (cambia) entre las últimas 2 ramas
```

### Crear una rama y moverme automáticamente a esa rama

```sh
git switch -c <nombre-rama>
git switch -c feature/switch
```

### Listado de todas las ramas

```sh
git branch -a
```

### Listado de todas las remotas

```sh
git branch -r
```

## GIT ALIAS

Son un acceso directo a comandos más extensos.

## Agregar un alias
```sh
# git s -> status -s
git config --global alias.s "status -s"
git config --global alias.l "log --oneline"
git config --global alias.ll "log --oneline --decorate --all --graph"
git config --global alias.c "commit -m" # git c "Mensaje"
```

### Listar los alias que tengo

```sh
git config --get-refexp alias
```

### Eliminar un alias

```sh
git config --global --unset alias.ll
git config --global --unset alias.c
```

### Agregar o quitar alias manualmente

```sh
git config --global -e
```

