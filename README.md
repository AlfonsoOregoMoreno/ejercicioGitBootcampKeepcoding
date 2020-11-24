# ejercicio 1 Git

## Preparativos: 
echo "# ejercicioGitBootcampKeepcoding" >> README.md

git init

git add README.md

git commit -m "first commit"

git branch -M master

git remote add origin https://github.com/AlfonsoOregoMoreno/ejercicioGitBootcampKeepcoding.git

git push -u origin master

## Enunciados y respuestas: 
Se deberá entregar a través del formulario de prácticas indicando la URL del repositorio. En el repositorio, deberá existir un archivo readme.md con las respuestas a las siguientes preguntas:

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?  
**git reset --hard HEAD~1**   
Porque con "--hard" sí se "afecta" al WC. Sin usar ese modificador nos quedamos con los cambios recientes, que no es lo que se nos pide. 

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?  
Para averiguar el Hash del commit al que quiero volver: **git reflog**   
Para restaurar la versión del fichero "git-nuestro.md", ya que quiero la que estaba en el commit recuperado (con estilos): **git restore git-nuestro.md**

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?  
No, porque la rama "styled" y "master" están actualmente en la misma "lista", y podríamos localizar cualquier commit de "master" desplazándonos por los commits de "styled". 

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?  
Sí, porque hay varias líneas con cambios en las versiones del fichero "git-nuestro.md" de ambas ramas. 

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?  
No, porque es un “merge” fast-forward (de 2 ramas que forman una “lista”, no una “bifurcación”).  

- ¿Qué comando o comandos utilizaste en el paso 25?  
**git log --graph --oneline**

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?   
Sí, porque “title” y “master” ya formaban una lista, tras haberse hecho el “merge” de “master” y “styled”. 

- ¿Qué comando o comandos utilizaste en el paso 27?  
**git reset HEAD~1** (porque ya estaba en master, y quiero ir un commit atrás). 

- ¿Qué comando o comandos utilizaste en el paso 28?  
**git restore git-nuestro.md** (y hemos perdido el título que se añadió). 

- ¿Qué comando o comandos utilizaste en el paso 29?  
**git branch -D title**

- ¿Qué comando o comandos utilizaste en el paso 30?  
**git reflog** Para localizar el Hash del commit que me interesa   
**git reset 25524a0** Para cambiar a ese commit (que es el del merge que quiero rehacer)   
**git restore git-nuestro.md** Para deshacer la eliminación del título  

- ¿Qué comando o comandos usaste en el paso 32?  
**git log** Para buscar el Hash correspondiente  
**git reset 066e0a1** Para cambiar al commit  
**git diff HEAD** Para verificar cuáles son las diferencias en el contenido del fichero   
**git restore git-nuestro.md** Para descartar los añadidos al poema  

- ¿Qué comando o comandos usaste en el punto 33?  
**git reflog** Para localizar el Hash del commit que me interesa  
**git reset b58272c** Para cambiar al commit  
**git diff HEAD** Para verificar cuáles son las diferencias en el contenido del fichero  
**git restore git-nuestro.md** Para recuperar los estilos y título  

