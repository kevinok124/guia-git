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

# GIST en Github
Me permite compartir código, pasar snippets a otras personas o información que quiero compartir

<https://cli.github.com>

Secretos -> Solo la persona que tenga el link puede verlo. No son privados.
Públicos -> Se van a indexar en los motores de búsqueda.

Pueden tener varios archivos y sus revisiones

# Trabajando en forma colaborativa con proyectos Open Source (Pull Request y Fork)

1. Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original) [CREAR FORK]
2. Me clono el fork desde mi cuenta github
3. Trabajo normalmente. Subo los cambios (A repo propio)
4. En el pull request de mi fork voy a ver la pestaña Pull Request. Creo un nuevo Pull Request.
---
5. Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la url del repositorio
7. Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

    git remote add upstream <URL-repositorio-original>

8. Me traigo los cambios del repositorio original a mi repo local

    git pull upstream <la-rama-donde-me-quiero-traer>

9. Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

    git push origin <rama-a-actualizar>

## GITHUB CLI
Es un herramienta para interacturar con los repositorios remotos de GITHUB

<https://cli.github.com/>