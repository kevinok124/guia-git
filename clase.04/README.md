# Clase 04

## Buenas prácticas para creación de mensajes de commits

<htpps://medium.com/@jmz12/buenas-pr%C3%A1cticas-para-commits-5eb4c86b9a47>

## GIT TAG

## Listar tags

```sh
git tag
```

## Ver que se hizo y quien tagueo este tag

```sh
git show <nombre-tag>
```

## Crear un tag

```sh
git tag -a v1.0.0
git tag -a v1.0.0 -m "Versión 1.0.0" # -a:annotate | -m:message
```

## Subir tags al remoto

### NO LO USO: Subir todos los tags

```sh
git push --tags
```

### Subir tag por tag... Uno a uno

```sh
git push origin <nombre-tag>
git push origin v1-0-0
```

### Para listar los commit hasta la versión deseada

```sh
git log v2.0.0
```

### Borrar un tag

```sh
git tag -d <anotación-del-tag>
git tag -d v2.0.0
```

## GIT CHERRY PICK

```sh
git cherry-pick <hash>
git cherry-pick <hash>..<hash> # Sin incluir los bordes
git cherry-pick <hash>^..<hash> # Incluyendo los bordes
```