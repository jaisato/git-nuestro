# Práctica Git

## Ejercicio 1

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?
git reset --hard HEAD~1
Se usa *git reset* para deshacer los cambios. Como se deben deshacer los cambios del último commit se usa *HEAD~1* que apunta al último commit realizado en el branch. Y para perder todos los cambios, incluso en el working copy, se usa la opción *--hard*.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?
git reflog
git reset --hard 8f91128
*Git reflog* para listar los últimos cambios realizados y encontrar el último commit a recuperar. *Git reset* para volver al estado del commit deseado (8f91128).

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?
git merge master
No causó ningún conflicto. La respuesta fue "Already up-to-date.". Porque la rama styled ya fue creada del último commit en master y master no contiene ningún commit nuevo.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?
Sí, porque se modificaron posteriormente las mismas líneas del mismo fichero *git-nuestro.md* en la rama *htmlify* mergeada.  

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?
No, porque git pudo hacer un "fast-forward" y cambiar el puntero de master directamente al último commit realizado en "styled", ya que el último commit realizado en master es padre del primer commit en styled y no se ha creado ninguna bifurcación o cambio posterior en master. 

- ¿Qué comando o comandos utilizaste en el paso 25?
git log --graph --decorate --pretty=oneline

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 
Sí, porque partimos de una "lista" donde no hay bifurcación que pueda dar conflictos entre ramas. Por tanto, el puntero en master podría cambiar y apuntar directamente al último commit realizado en title.

- ¿Qué comando o comandos utilizaste en el paso 27?
git reset HEAD~1

- ¿Qué comando o comandos utilizaste en el paso 28?
git checkout -- git-nuestro.md

- ¿Qué comando o comandos utilizaste en el paso 29? 
git branch -D title

- ¿Qué comando o comandos utilizaste en el paso 30?
*git reflog* para encontrar el commit del merge. Y *git reset --hard 1a88583* para volver a reestablecer el commit del merge.

- ¿Qué comando o comandos usaste en el paso 32?
*git log* para ver el 1r commit. Y *git reset --hard fe95d427fe340dfd22f63aa3dda18086f1d2946c* para reestablecer el commit inicial.

- ¿Qué comando o comandos usaste en el punto 33?
*git reflog* para encontrar el último commit con el título (merge). Y *git reset --hard 1a88583* para volver a reestablecer el commit del merge con el título.
