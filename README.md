# Guía para crear una rama y hacer cambios en Git

FECHA LIMITE: 15 de Agosto de 2023

Esta guía te enseñará cómo crear una nueva rama que parte de la rama master del Proyecto, hacer 5 commits diferentes en esa rama cada uno con cambios diferentes, y hacerles push a Github. Además, explicará cómo hacer un merge desde master a la nueva rama y cómo solucionar conflictos en caso de que ocurran. Por último, explicará cómo hacer un PULL REQUEST en Github.

NOTA: [EL PROYECTO A MODIFICAR SE ENCUENTRA HACIENDO CLICK AQUI](https://github.com/davidbo99/fast-api-git-example). ESTE PROYECTO DE GIT ACTUAL SOLAMENTE ES UNA GUIA

EVALUACION TEORICA: [ENTRE A ESTE ENLACE Y RESUELVA LA EVALUACION TEORICA](https://forms.gle/QFhdyiAxgpgjkKzb9).

## Creación de una nueva rama y hacer cambios

1. Asegúrate de que estás en la rama master escribiendo el siguiente comando en Git Bash:

```bash
git checkout master
```

2. Crea una nueva rama cuyo nombre sea su nombre y cambia a ella escribiendo el siguiente comando:

```bash
git checkout -b nueva-rama
```

3. Haz los cambios deseados en los archivos de tu proyecto. Puedes crear archivos y modificarlos.

4. Agrega los cambios al área de staging escribiendo el siguiente comando:

```bash
git add .
```

5. Haz commit de los cambios escribiendo el siguiente comando:

```bash
git commit -m "mensaje del commit"
```

6. Repite los pasos 3-5 para hacer 4 commits adicionales con cambios diferentes.

## Haciendo push de los cambios a Github

1. Haz push de la nueva rama a Github escribiendo el siguiente comando:

```bash
git push --set-upstream origin nueva-rama
```

## Haciendo un merge de master a la nueva rama

1. Cambia de vuelta a la rama master, trae los cambios nuevos de master y vuelve a la rama que creaste:

```bash
git checkout master
git pull
git checkout nueva-rama
```

2. Realiza un merge que viene desde master a tu nueva rama para obtener los cambios de los demas colaboradores y compañeros:

```bash
git merge master
```

3. Si hay conflictos, soluciónalos editando los archivos, luego agrega al area de staging y haz commit de los cambios como se realizo en la sección anterior.
Finaliza con un push.

```bash
git add .
git commit -m "solución de conflicto de merge"
git push
```


4. Ve a Github y crea un Pull Request seleccionando la nueva rama como la rama "compare" y la rama master como la rama "base".

- Asegúrate de incluir un título y un mensaje descriptivo para el Pull Request.
- Revisa los cambios y asegúrate de que todo parece correcto.
- Crea el Pull Request.
- Asigna al usuario davidbo99 como reviewer del PR.

Puedes usar esta guia como apoyo [Pull Request Guia](https://docs.github.com/es/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)


