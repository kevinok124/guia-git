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

## SHOW-BRANCH
Nos muestra el último commit de cada rama

```sh
git show-branch
```

### Para borrar una rama

```sh
git branch -d <nombre-rama>
git branch -d dev

## Y si tengo una rama que nunca fue fusionada con otra.
git branch -D <nombre-rama>
git branch -D dev # Fuerza el borrado.
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

## STASH

Es una pila de almacenamiento que nos otorga GIT. Permite registrar temporalmente cambios que están en el working directory o en el staging area. Cuando recupero un stash lo que estoy haciendo es volcando el contenido del stash en el WD.
Esto me va a permitir navegar entre ramas, sin tener que estar haciendo un commit para liberar las diferentes áreas.


## Listar un stash
```sh
git stash list
```

## Recuperar el último stash
Me recupera el último stash y si no hay conflictos lo borra.
```sh
git stash pop
```

## Recuperar un stash en específico
Me recupera el último stash y si no hay conflictos lo borra.

```sh
git stash apply  # Va a aplicar el último
git stash apply 5
git stash apply tash@{5}
```

## Borra un stash en específico

```sh
git stash drop # El drop borra el último
git stash drop 3 
git stash drop stash@{3}
```

## Aplico un stash en una nueva rama

git stash branch<nombre-rama>

## Ver el contenido de un stash

```sh
git stash show -p stash@{1}
```

## Limpiar todos los stash

```sh
git stash clear
```