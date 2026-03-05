# Comandos utilizados

## Clonar el repositorio
git clone https://github.com/rubenaraujorcloud/masteruah.git
cd masteruah

## Añadir README y commit inicial
git add README.md
git commit -m "commit inicial"
git push -u origin main

## Añadir fichero 1.txt
git add 1.txt
git commit -m "Añadido fichero 1.txt"
git push

## Crear tag v0.1
git tag v0.1
git push origin v0.1

## Crear rama v0.2
git checkout -b v0.2

## Añadir fichero 2.txt en la rama v0.2
git add 2.txt
git commit -m "Añadido 2.txt en rama v0.2"
git push -u origin v0.2

## Merge directo
git checkout main
git merge v0.2
git push

## Crear conflicto de merge
git checkout main
git add 1.txt
git commit -m "Hola en 1.txt en main"

git checkout v0.2
git add 1.txt
git commit -m "Adios en 1.txt en v0.2"

git checkout main
git merge v0.2

## Arreglar conflicto
git add 1.txt
git commit -m "Conflicto resuelto"
git push

## Listado de ramas
git branch --merged
git branch --no-merged

## Crear tag v0.2
git tag v0.2
git push origin refs/tags/v0.2

## Borrar rama v0.2
git branch -d v0.2
git push origin --delete refs/heads/v0.2

## Ver historial
git log --oneline --decorate --graph --all