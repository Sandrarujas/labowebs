# Ejercicio de Git - proyecto labowebs

> Realizado por Sandra Rujas

[TOC]

# Trabajo en local

1. **Inicializa un nuevo repositorio Git en una carpeta llamada "labowebs" y agrega los**
    **archivos proporcionados en el aula virtual. Renombra la rama master a `main` , si es**
    **necesario. Realiza el primer commit. Muestra el log del repositorio.**

- Si no tenemos creada la carpeta de laboweb deberemos ejecutar los siguientes comandos:

  ```bash
  	$ mkdir labowebs
  	$ cd labowebs
  ```

- Una vez dentro de la carpeta de laboweb, abrimos la terminal y tenemos que ejecutar los siguientes comandos:

  ```bash
  	$ git init
  	$ git add .
  ```

  ![image-20241114085252366](C:\Users\34615\AppData\Roaming\Typora\typora-user-images\image-20241114085252366.png)

  ![image-20241114085700660](./Ejercicio de Git - proyecto labowebs.assets/image-20241114085700660.png)

- Si tu rama aún no se llama main, deberéis ejecutar lo siguiente:

  ```bash
  	$ git branch -m master main
  ```

  ![image-20241114085925084](./Ejercicio de Git - proyecto labowebs.assets/image-20241114085925084.png)

- Realizamos el primer commit:

  ```bash
  	$ git commit -m "Agregando el primer commit: agregando archivos iniciales"
  ```

  ![image-20241114090203184](./Ejercicio de Git - proyecto labowebs.assets/image-20241114090203184.png)

- Y mostramos el log del repositorio:

  ```bash
  	$ git log 
  ```

  ![image-20241114090300961](./Ejercicio de Git - proyecto labowebs.assets/image-20241114090300961.png)

2. **Incluye un fichero .gitignore para que los ficheros `README.md , LICENCE.txt y`**
    **`passwords.txt` sean ignorados por el control de versiones. Realiza el commit y muestra** **los logs del repositorio en una línea.**

- Creamos el archivo en la carpeta:

  ![image-20241114090907860](./Ejercicio de Git - proyecto labowebs.assets/image-20241114090907860.png)

- Añadimos los ficheros citados anteriormente y guardamos:

  ![image-20241114090836652](./Ejercicio de Git - proyecto labowebs.assets/image-20241114090836652.png)

- Ahora volvemos a la consola de comandos para ejecutar lo siguiente:

  ```bash
  	$ git add .gitignore
  	$ git commit -m "Agregamos .gitignore para ignorar los ficheros README.md, LICENSE.txt, passwords.txt"
  ```

  ![image-20241114091342696](./Ejercicio de Git - proyecto labowebs.assets/image-20241114091342696-1731572023765-1.png)

 <img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241114091547819.png" alt="image-20241114091547819" style="zoom: 57%;" />

- Como podéis comprobar, me confundí al agregar el mensaje en el commit. Para remediar este error, podemos ejecutar el siguiente comando:

  ```bash
      $ git commit --amend -m "Nuevo mensaje de commit: Configuramos .gitignore para ignorar README.md, 	 LICENSE.txt y password.txt"
  ```

![image-20241114092006253](./Ejercicio de Git - proyecto labowebs.assets/image-20241114092006253.png)

<div style="page-break-after: always; break-after: page;"></div>

- Y por último, mostramos los logs en una sola línea:

  ```bash
  	$ git log --oneline
  ```

![image-20241114092111446](./Ejercicio de Git - proyecto labowebs.assets/image-20241114092111446.png)

  Para seguir con el ejercicio, debemos hacer unos cambios antes:

Deberemos modificar los documentos `index.html, contacto.html y script.js`, eliminando algunas partes que vamos a tener que incluir a continuación. Para ello, deberás borrar lo información necesaria y ejecutar los siguientes comando para poder proseguir con el ejercicio:

  ```bash
  	$ git add 
  	$ git commit -m "Commit extra para eliminar cositas que no debería estar en los documentos del 	index.html, contacto.html y script.js"
  ```

![image-20241114092649430](./Ejercicio de Git - proyecto labowebs.assets/image-20241114092649430.png)

- Mostramos el log en una línea con los nuevos datos que hemos modificado:

  ![image-20241114092957057](./Ejercicio de Git - proyecto labowebs.assets/image-20241114092957057.png)

3. **En el repositorio, crea los archivos `README.md , LICENCE.txt y passwords.txt` con algún contenido. Muestra el estado del repositorio. Muestra el listado de archivos ignorados.**

- Creamos los archivos y les añadimos contenido:

  ![image-20241114093417741](./Ejercicio de Git - proyecto labowebs.assets/image-20241114093417741.png)

![image-20241114093552583](./Ejercicio de Git - proyecto labowebs.assets/image-20241114093552583.png)

<div style="page-break-after: always; break-after: page;"></div>

- Mostramos el estado del repositorio:

  ```bash
  	$ git status
  ```

![image-20241114093732813](./Ejercicio de Git - proyecto labowebs.assets/image-20241114093732813.png)

- Mostramos el listado de los archivos ignorados:

  ```bash
  	$ git ls-files --others -i --exclude-standard
  ```

![image-20241114093839191](./Ejercicio de Git - proyecto labowebs.assets/image-20241114093839191.png)

4. **Crea una rama `feature-estilos` . Cámbiate a ella.**

   ```bash
   $  git checkout -b feature-estilos
   ```

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241114094141287.png" alt="image-20241114094141287" style="zoom: 50%;" />

- Modifica el archivo estilos.css :

​		- Propiedad color del body y de h2 : De #2a2a2a a #015743.

![image-20241114094425396](./Ejercicio de Git - proyecto labowebs.assets/image-20241114094425396.png)



​		- Propiedad background-color de header y footer: De #2a75ff a #11b24f



![image-20241114094546743](./Ejercicio de Git - proyecto labowebs.assets/image-20241114094546743.png)

<div style="page-break-after: always; break-after: page;"></div>

- Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el
  mensaje "actualizados estilos a azules".

```bash
 $ git status
 $ git add .
 $ git commit -m "Actualizamos el color del body, h2 y el fondo del header y el footer de colores 		azulados a verdosos."
```

![image-20241114094647376](./Ejercicio de Git - proyecto labowebs.assets/image-20241114094647376.png)

![image-20241114094806801](./Ejercicio de Git - proyecto labowebs.assets/image-20241114094806801.png)

![image-20241114095012572](./Ejercicio de Git - proyecto labowebs.assets/image-20241114095012572.png)

5. **Vuelve a la rama `main` . En el archivo `index.html` añade un comentario donde se indique tu nombre como autor de la página. Comprueba el estado del repositorio. Añade los cambios, realiza un commit con el mensaje ' añadido autor en index'. Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'.**
   
   - Volvemos a la rama main:

   ```bash
   $ git checkout main
   ```
   
   ![image-20241114095638965](./Ejercicio de Git - proyecto labowebs.assets/image-20241114095638965.png)

   - Añadimos comentario con nuestro nombre:

   ![image-20241114095853884](./Ejercicio de Git - proyecto labowebs.assets/image-20241114095853884.png)

   - Volvemos a nuestra terminal y ejecutamos los siguientes comandos:

   ```bash
   $ git add .
   $ git commit -m "añadido autor en index. En concreto, en el footer."
   ```
   
   ![image-20241114100037850](./Ejercicio de Git - proyecto labowebs.assets/image-20241114100037850.png)

   - Mostramos los logs en una línea, gráficamente y con decoración:

   ```bash
   $  git log --oneline --graph --decorate
   ```
   
   ![image-20241114100233401](./Ejercicio de Git - proyecto labowebs.assets/image-20241114100233401.png)

   <div style="page-break-after: always; break-after: page;"></div>

6. **Fusiona la rama `feature-estilos` en la rama `main` . Muestra los logs del repositorio en una línea, gráficamente y con 'decoración'.**
   
   - No aseguramos de que estamos en la rama main antes de todo:
   
   ```bash
   $ git checkout main 
   ```
   
   ![image-20241114100739001](./Ejercicio de Git - proyecto labowebs.assets/image-20241114100739001.png)
   
   - Una vez comprobamos que estamos en dicha rama, fusionamos ambas:

```bash
	$ git merge feature-estilos
```

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241114100922304.png" alt="image-20241114100922304" style="zoom:50%;" />

​	- Mostramos los logs con las especificaciones del enunciado:

```bash
	$ git log --oneline --graph --decorate
```

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241114101042481.png" alt="image-20241114101042481" style="zoom: 40%;" />



# Trabajo en remoto

1. **Continúa con el repositorio labowebs . Añade el repositorio a Sourcetree.**

   <img src="./Ejercicio de Git - proyecto labowebs.assets/01_add.png" alt="01_add" style="zoom: 50%;" />

   <div style="page-break-after: always; break-after: page;"></div>

   **1:** Le damos a la opción de Add para añadir un repositorio ya existente, en este caso, el nuestro se llama labowebs.

   **2:** Buscamos el repositorio en nuestro ordenador.

   **3:** Pulsamos add para finalmente añadirlo.

   

   ![image-20241115090644477](./Ejercicio de Git - proyecto labowebs.assets/image-20241115090644477.png)

2. **Crea un repositorio remoto y sube al remoto los ficheros de tu repositorio local. Debes subir todas las ramas.**

     Creamos un repositorio en nuestra cuenta de **Github**:

  ![image-20241115091044050](./Ejercicio de Git - proyecto labowebs.assets/image-20241115091044050.png)

- Copiamos la url del nuevo repositorio, que en mi caso es la siguiente: https://github.com/Sandrarujas/labowebs.

- Ahora nos vamos a la aplicación de **Sourcetree** y seguimos los siguientes pasos:

  <img src="./Ejercicio de Git - proyecto labowebs.assets/01_add-1731659884439-2.png" alt="01_add" style="zoom:80%;" />

​	**1:** Le damos a la opción de Add.

​	**2:** Buscamos la carpeta en nuestro ordenador donde tenemos nuestro ejercicio.

​	**3:** Finalmente le damos a Add. Y nos aparece la siguiente imagen:

![02_añadido](./Ejercicio de Git - proyecto labowebs.assets/02_añadido.png)

<div style="page-break-after: always; break-after: page;"></div>

-  Le damos a la opción de Remote y seguidamente realizamos las siguientes acciones (sigue la flecha):

![03_remote](./Ejercicio de Git - proyecto labowebs.assets/03_remote.png)

  ![03_remote_2](./Ejercicio de Git - proyecto labowebs.assets/03_remote_2.png)

<div style="page-break-after: always; break-after: page;"></div>

- Añadimos un nombre, la URL o Path del repositorio de Git y nuestro username:

  ![03_remote_3](./Ejercicio de Git - proyecto labowebs.assets/03_remote_3.png)

  ![03_remote_4](./Ejercicio de Git - proyecto labowebs.assets/03_remote_4.png)

  <div style="page-break-after: always; break-after: page;"></div>

- Debemos comprobar que en **Sourcetree** nos aparece lo siguiente:

  ![03_remote_5](./Ejercicio de Git - proyecto labowebs.assets/03_remote_5.png)

Ahora es momento de subir los cambios al repositorio de **Git** desde la aplicación:

- En la barra principal, clickamos en Push.
- Seleccionamos todas las ramas (Select All) y le damos al botón de Push.

<img src="./Ejercicio de Git - proyecto labowebs.assets/03_remote_6.png" alt="03_remote_6" style="zoom: 50%;" />

​        <img src="./Ejercicio de Git - proyecto labowebs.assets/03_remote_7.png" alt="03_remote_7" style="zoom:50%;" />

- Nos vamos a la página de **Git** para comprobar que los cambios han sido realizados correctamente:![03_remote_8](./Ejercicio de Git - proyecto labowebs.assets/03_remote_8.png)

  <div style="page-break-after: always; break-after: page;"></div>

3. **Crea una rama `feature-index`. Añade el siguiente código dentro de la `<section class="about">` .Añade los cambios y crea un commit. Sube los cambios al remoto.**

- Creamos la rama:![03_remote_9](./Ejercicio de Git - proyecto labowebs.assets/03_remote_9.png)

  ![03_remote_10](./Ejercicio de Git - proyecto labowebs.assets/03_remote_10.png)

- Añadimos el código a la sección `"about"` (para ello he utilizado Visual Studio Code) y guardamos los cambios (podemos utiilizar Ctl+s para hacerlo de forma rápida):

  ![image-20241115094805652](./Ejercicio de Git - proyecto labowebs.assets/image-20241115094805652.png)
  
  <div style="page-break-after: always; break-after: page;"></div>
  
-  Nos vamos de nuevo a la aplicación y comprobamos que hay un "commit" incompleto:

  ![image-20241119092313614](./Ejercicio de Git - proyecto labowebs.assets/image-20241119092313614.png)

- En la barra principal clickamos encima de "commit" y nos aparece lo siguiente:

![image-20241115095245331](./Ejercicio de Git - proyecto labowebs.assets/image-20241115095245331.png)

- Deberemos darle a la opción de (+) que ves en la foto anterior, para pasar los cambios del área de Staging. A continuación, escribiremos un comentario para el commit (En este caso he puesto lo siguiente "Modificamos index: sección about" y le finalmente le damos al botón de commit.

  ![image-20241115095341134](./Ejercicio de Git - proyecto labowebs.assets/image-20241115095341134.png)

-  Si se produce el commit, deberá aparecer la siguiente información en el panel de **Sourcetree**:

![image-20241115095442649](./Ejercicio de Git - proyecto labowebs.assets/image-20241115095442649.png)

  Ahora, subiremos los cambios al repositorio remoto de **Git**. Seguimos los siguientes pasos: 

- Clickamos Push del panel principal, seleccionamos la rama en la hemos modificado los datos, y le damos al botón de Push.

  ![image-20241115095600866](./Ejercicio de Git - proyecto labowebs.assets/image-20241115095600866.png)

  Resultado:

![image-20241115100548169](./Ejercicio de Git - proyecto labowebs.assets/image-20241115100548169.png)

  ![image-20241115095659106](./Ejercicio de Git - proyecto labowebs.assets/image-20241115095659106.png)

4. **En el repositorio local, fusiona la rama `feature-index` en la rama `main` .**

   ![image-20241115100239364](./Ejercicio de Git - proyecto labowebs.assets/image-20241115100239364.png)

   Otra opción (paso por paso):

   <img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241115101049176.png" alt="image-20241115101049176" style="zoom:80%;" />

   ![image-20241119092141333](./Ejercicio de Git - proyecto labowebs.assets/image-20241119092141333.png)

   ![image-20241115101259055](./Ejercicio de Git - proyecto labowebs.assets/image-20241115101259055.png)

   ![image-20241115101349892](./Ejercicio de Git - proyecto labowebs.assets/image-20241115101349892.png)

   Comprobamos en **Github**:

   ![image-20241115101501425](./Ejercicio de Git - proyecto labowebs.assets/image-20241115101501425.png)

   <div style="page-break-after: always; break-after: page;"></div>

5. **Edita el fichero `contacto.html` . Borra unas líneas. Muestra los ficheros con cambios pendientes y las diferencias. Añade los cambios y haz un commit.**
   
     - En este caso, he borrado el header (aparece en la siguiente fotografía):

​              <img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241115101833067.png" alt="image-20241115101833067"  />

- Realizamos el "commit" siguiendo los pasos que hemos realizado anteriormente:

![image-20241119093248358](./Ejercicio de Git - proyecto labowebs.assets/image-20241119093248358.png)

![image-20241115101941940](./Ejercicio de Git - proyecto labowebs.assets/image-20241115101941940.png)

-  Por último, realizamos el Push (siguiendo también los pasos que hemos hecho en ejercicios anteriores):

  ![image-20241115102026653](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102026653.png)

  ![image-20241115102102476](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102102476.png)

- Comprobamos en **Git** lo cambios:

  ![image-20241115102155636](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102155636.png)

6. **Te das cuenta del error. Deshaz el commit anterior. Captura el estado actual del repositorio.**

     Le damos botón derecho sobre el commit. Opción de Reserve para deshacer el commit que hemos hecho:

  ![image-20241115102559918](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102559918.png)

  ![image-20241115102630963](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102630963.png)![image-20241115102716542](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102716542.png)



- Hacemos Push para subir los cambios al repositorio de **Git**:

  ![image-20241115102827695](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102827695.png)

  ![image-20241115102901997](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102901997.png)

- Comprobamos que se ha subido correctamente:

  

  ![image-20241115102954476](./Ejercicio de Git - proyecto labowebs.assets/image-20241115102954476.png)

  <div style="page-break-after: always; break-after: page;"></div>

- Y por último, comprobamos que lo hemos revertido:

  <img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119093704118.png" alt="image-20241119093704118" style="zoom:67%;" />

  

7. **Crea una rama `feature-mapa` . Incluye este código en el archivo `contacto.html` . Añade los cambios. Realiza un commit. Sube los cambios al remoto. Muestra en el remoto los cambios del archivo contacto.html en la rama `feature-mapa`. Asegurarse de que contacto.html queda con TODAS sus líneas.**

- Creamos la rama nueva `"feature-mapa"` y añadimos el código anterior en `"contacto.html"`.

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241115103346198.png" alt="image-20241115103346198" style="zoom: 80%;" />

​                                        <img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241115103515363.png" alt="image-20241115103515363" style="zoom:67%;" />

- Realizamos el commit:

![image-20241115103616598](./Ejercicio de Git - proyecto labowebs.assets/image-20241115103616598.png)

  ![image-20241115103706046](./Ejercicio de Git - proyecto labowebs.assets/image-20241115103706046.png)

![image-20241115103738515](./Ejercicio de Git - proyecto labowebs.assets/image-20241115103738515.png)

- Como en anteriores acciones, debemos hacer un Push para subir los cambios al repositorio remoto de Git:

![image-20241115103842630](./Ejercicio de Git - proyecto labowebs.assets/image-20241115103842630.png)

![image-20241115104055411](./Ejercicio de Git - proyecto labowebs.assets/image-20241115104055411.png)



8. **En GitHub, en la rama `main` , fusiona la rama `feature-mapa` . Baja los cambios del remoto a local. Deja los dos repositorios sincronizados.**

****  ![image-20241115104610937](./Ejercicio de Git - proyecto labowebs.assets/image-20241115104610937.png)



  ![image-20241115104446530](./Ejercicio de Git - proyecto labowebs.assets/image-20241115104446530.png)

![image-20241115104838544](./Ejercicio de Git - proyecto labowebs.assets/image-20241115104838544.png)



Lo he hecho desde **Sourcetree**, pero desde **Github** tendríamos que seguir los siguientes pasos:

​	**1:**Vamos a nuestro repositorio en Github.

​	**2:** Cambiamos a la rama `main` desde el menú de ramas.

​	**3:** Abrimos un Pull Request desde la rama `feature-mapa` hacia `main`:

- Vamos a la pestaña **Pull Requests**.

- Creamos un nuevo PR seleccionando `feature-mapa` como la rama de origen y `main` como la rama de destino.

- Revisamos los cambios y confirmamos la fusión (merge) si todo está correcto.

  ![image-20241119101338590](./Ejercicio de Git - proyecto labowebs.assets/image-20241119101338590.png)

![image-20241119101133434](./Ejercicio de Git - proyecto labowebs.assets/image-20241119101133434.png)

![image-20241119101107011](./Ejercicio de Git - proyecto labowebs.assets/image-20241119101107011.png)

# Conflictos

1. **Crea una rama `hotfix-js` . Cámbiate a ella. Añade este código en el fichero `script.js`. Confirma el cambio y haz un commit. (Fíjate en los números de línea...)**
   
     ![image-20241119101809726](./Ejercicio de Git - proyecto labowebs.assets/image-20241119101809726.png)
     
     <div style="page-break-after: always; break-after: page;"></div>
     
     - Añadimos el código al fichero de js:
     
     <img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119103143764.png" alt="image-20241119103143764" style="zoom: 67%;" />
     
     - Una vez guardamos el fichero de nuevo, nos vamos a **Sourcetree** a realizar el "commit":
     
     ![image-20241119102418399](./Ejercicio de Git - proyecto labowebs.assets/image-20241119102418399.png)
     
     ![image-20241119102619322](./Ejercicio de Git - proyecto labowebs.assets/image-20241119102619322.png)
     
     ![image-20241119102656330](./Ejercicio de Git - proyecto labowebs.assets/image-20241119102656330.png)
     
     <div style="page-break-after: always; break-after: page;"></div>
     
2. **Vuelve a la rama `main` . En el fichero `script.js` en las mismas líneas que en la cuestión anterior, añade el código siguiente. Confirma el cambio y haz un commit.**
   
     - Volvemos a la rama `main`: 
     
     ![image-20241119103025635](./Ejercicio de Git - proyecto labowebs.assets/image-20241119103025635.png)
     
     - Cambiamos el código:
     
     ![image-20241119103422578](./Ejercicio de Git - proyecto labowebs.assets/image-20241119103422578.png)
     
     - En **Sourcetree** realizamos el commit:
     
     ![image-20241119103502262](./Ejercicio de Git - proyecto labowebs.assets/image-20241119103502262.png)
     
     ![image-20241119103705537](./Ejercicio de Git - proyecto labowebs.assets/image-20241119103705537.png)
     
     <div style="page-break-after: always; break-after: page;"></div>
     
     - Como siempre, subimos los cambios también a **Github** a través de un Push:
     
     ![image-20241119103925902](./Ejercicio de Git - proyecto labowebs.assets/image-20241119103925902.png)
     
     
     
3. **Fusiona la rama `hotfix-js` en `main` . Debe producirse un conflicto. Resuélvelo. Cuando termines la resolución del conflicto sube los cambios al remoto - Deja los repositorios sincronizados.**

- Fusionamos las ramas:

![image-20241119104109284](./Ejercicio de Git - proyecto labowebs.assets/image-20241119104109284.png)

![image-20241119104152468](./Ejercicio de Git - proyecto labowebs.assets/image-20241119104152468.png)

- Al darle al botón de Aceptar nos salta el siguiente recuadro mostrándonos que tenemos un conflicto:

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119104240945.png" alt="image-20241119104240945" style="zoom: 67%;" />

- Esto es lo que nos sale en el panel principal de la aplicación:

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119104608376.png" alt="image-20241119104608376" style="zoom: 67%;" />

- Y esto, en el fichero js:

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119104710612.png" alt="image-20241119104710612" style="zoom: 67%;" />

- Desde dicho documento debemos elegir la solución que queremos para nuestro proyecto.

Yo he elegido lo siguiente:

- Primero he comparado los cambios que hay entre ambos y he borrado las líneas que no necesitaba:

![image-20241119104905255](./Ejercicio de Git - proyecto labowebs.assets/image-20241119104905255.png)

![image-20241119105052506](./Ejercicio de Git - proyecto labowebs.assets/image-20241119105052506.png)

<div style="page-break-after: always; break-after: page;"></div>

- Seguidamente, realizamos el último commit:

![image-20241119105253230](./Ejercicio de Git - proyecto labowebs.assets/image-20241119105253230.png)

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119105403785.png" alt="image-20241119105403785" style="zoom:50%;" />

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119105536218.png" alt="image-20241119105536218" style="zoom: 67%;" />

- Y por último, lo subimos al repositorio remoto:

<img src="./Ejercicio de Git - proyecto labowebs.assets/image-20241119105630935.png" alt="image-20241119105630935" style="zoom:67%;" />

<div style="page-break-after: always; break-after: page;"></div>

  # Subida de documentación

 En la carpeta del proyecto labowebs añade una carpeta docs . Copia en esa carpeta el fichero markdown y la carpeta con las imágenes. Incluye también el pdf . Añade todo al repositorio. Súbelo al remoto.

![image-20241119192636620](./Ejercicio de Git - proyecto labowebs.assets/image-20241119192636620.png)

