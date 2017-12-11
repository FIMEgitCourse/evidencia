# Pasos a seguir

Antes de iniciar :

**Copiar y pegar todos los comandos no funcionará del todo, hay que seguir las instrucciones y aplicar según sea el caso**

## Configuración de credenciales

Una vez que tenemos instalado **git** utilizando alguna de las [versiones](https://git-scm.com/downloads) procederemos a configurar nuestras credenciales.

Usaremos el comando `config` para establecer **nuestro nombre** de manera global para que funcione en todas las carpetas

`git config --global user.name "Mi nombre"`

Después lo hacemos pero ahora con **nuestro correo**.

`git config --global user.email yo@gmail.com`

## Iniciando un repositorio con Github

Accedemos a nuestra cuenta de [Github](https://github.com) y utilizaremos el botón rápido para crear repositorios.

![alt text](https://i.imgur.com/KIvja3W.png)

---

Y después le damos un nombre, deberá llamarse **evidencia** 

---

![evidencia](https://i.imgur.com/FcxOiQa.png)

---

Copiamos la liga a nuestro nuevo repositorio, la necesitaremos en el siguiente paso.

![nuevo repositorio](https://i.imgur.com/csyxp0n.png)

---

Desde la consola `Git Bash` creamos un nuevo repositorio en nuestra computadora.

`git init evidencia`

Nos dirá que se ha creado un repositorio vacío en una carpeta, nos movemos hacia esa carpeta.

`cd evidencia`

Agregamos la ruta de nuestro repositorio de Github ( para esto la copiamos desde github )

`git remote add nuestro_git https://github.com/<su usuario de git>/evidencia.git`

Ahora ya podemos iniciar a trabajar nuestro repositorio.

## Creando un primer commit

Lo primero que harémos es crear el archivo de **README** para que funcione de portada para nuestra evidencia.

Desde la carpeta de `evidencia` usamos el siguiente comando.

`echo "#Evidencia de <Aquí va su nombre>" > README.md`

Agregamos el archivo al control de versiones

`git add README.md`

Hacemos un commit inicial

`git commit -m "Primer commit"`

Y enviamos nuestros cambios a github

`git push nuestro_git master`

En este paso **es posible** que nos pidan nuestro usuario/contraseña de git, es normal.

Una vez que tenemos nuestro repositorio listo, iniciemos con los ejercicios.

## Trabajando nuestros archivos

Cada uno de los cinco ejercicios deberá cumplir con lo siguiente:

- Será añadido utilizando una `branch` y un `pull request`.
- Tendrá su propia carpeta con los siguientes elementos: 
   - Tendrá su archivo de README.md con su descripción
   - Tendrá el archivo del ejercicio **.c**
- Se harán dos commits:
   - El primer **commit** tendrá la descripción y el ejercicio
   - El segundo **commit** tendrá únicamente la descripción
   
A continuación se describe como realizar este proceso

Desde `Git Bash` accedemos a la carpeta de `evidencia` y creamos una nueva `branch`. Asegurese de usar un nombre de interes.

`git branch <nombre de la rama>`

Después nos movemos hacia esa rama

`git checkout <nombre de la rama>`

Y creamos la carpeta para nuestro primer ejercicio.

**Dentro de la carpeta** iniciaremos por poner nuestro archivo **README.md**

`touch README.md`

Y editamos el archivo para añadir la descripción de nuestro primer ejercicio.

Una vez que tenemos la descripción, **hay que poner el ejercicio en la carpeta**

Agregamos ambos archivos al control de versiones

`git add README.md`

`git add <nombre del archivo del ejercicio>`

y hacemos el primer **commit** que nos solicitan.

`git commit -m "Agrega la descripcion del ejercicio <nombre del ejercicio> junto con su solucion"`

Después quitamos del control de versiones el ejercicio

`git rm <nombre del archivo del ejercicio>`

Y añadimos el segundo **commit** que nos solicitan.

`git commit -m "Elimina la solucion del ejercicio <nombre del ejercicio>"`

Compartimos nuestros cambios

`git push nuestro_git <nombre de la rama>`

Desde Github creamos un pull request

![pull request](https://i.imgur.com/JDXNcZK.png) 

---

Hay que recordar que la flecha nos indica **hacia cual rama** estamos integrando los cambios

![cambios](https://i.imgur.com/i5aKgmv.png)

---

Una vez que creamos nuestro pull request, lo integramos usando cualquier método (`merge`, `squash`, `rebase`) y repetimos con los otros cuatro ejercicios restantes.

Al final tendrémos los resultados indicados en el [README](/README.md#resultados) de este repositorio.