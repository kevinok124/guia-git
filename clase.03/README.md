# Clase 03

## RAMAS (Branches)

![Ramas](_ref/ramas.png)

## SHOW-BRANCH

Nos muestra el último commit de cada rama

```sh
git show-branch
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

