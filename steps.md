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

## Creando los archivos necesarios

Lo primero que harémos es crear el archivo de **README** para que funcione de portada para nuestra evidencia.

Desde la carpeta de `evidencia` usamos el siguiente comando.

`echo "#Evidencia de <Aquí va su nombre>" > README.md`


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

`git branch <nombre de la rama> `
