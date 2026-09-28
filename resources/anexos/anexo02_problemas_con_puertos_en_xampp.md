## ANEXO 02: Problemas de Puertos con Xampp

1. [Cambiar los puertos de 'Apache' en 'XAMPP'](#1-cambiar-los-puertos-de-apache-en-xampp)
2. [Cambiar los puertos de 'MySQL' en 'XAMPP'](#2-cambiar-los-puertos-de-mysql-en-xampp)

<br>

**<div align="center"><a href="../../README.md">Menú Principal</a></div>**

---
## 1. Cambiar los puertos de 'Apache' en 'XAMPP'
&nbsp;

#### 1.1. Ir al archivo de configuración 'httpd.conf' de 'Apache' 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la misma línea del servicio 'Apache' dar click en 'Config / Apache (httpd.conf)'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B'). Se abrirá un 'Bloc de Notas'.

#### 1.2. En el Bloc de Notas

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B').
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la ventana emergente y en el control de texto 'Buscar: ', escribir '80' y dar click en 'Buscar siguiente'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Reemplazar todos los valores donde se encentre el puerto '80' con el puerto nuevo de trabajo, por ejemplo, '8080'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'cancelar' y guardar los cambios en el archivo.

#### 1.3. Iniciar el servicio 'Apache' en el puerto nuevo de trabajo

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En el Panel de control de XAMPP dar click en 'start' de 'Apache' para iniciar el servicio.

#### 1.5. En el navegador:

```
http://localhost:8080/proyecto/
```

<div align="right"><a href="#anexo-02-problemas-de-puertos-con-xampp">Volver al Menú</a></div>

---
## 2. Cambiar los puertos de 'MySQL' en 'XAMPP'
&nbsp;

#### 2.1. En el Panel de control de XAMPP y en la misma línea del servicio 'MySQL' dar click en 'Config / my.ini'.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Abrir el 'Panel de Control'
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'Cuentas de usuario / Administrar credenciales de Windows'. 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Si hay una cuenta asociada (Ver imagen), click sobre la cuenta y la opción 'Quitar'. 

#### 2.2. Se abrirá un 'Bloc de Notas'. Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B').

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Verificar que tenga por lo menos un archivo, ya que Github no guarda carpetas, solo archivos.

#### 2.3. En la ventana emergente y en el control de texto 'Buscar: ', escribir '3306' y dar click en 'Buscar siguiente'.

#### 2.4. Reemplazar todos los valores donde se encentre el puerto '3306' con el puerto nuevo de trabajo, por ejemplo, '3308'. Dar click en 'cancelar' y guardar los cambios en el archivo.

#### 2.5. En el Panel de control de XAMPP y en la misma línea del servicio 'Apache' dar click en 'Config / Apache (php.ini)'.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click al 'Nombre de su cuenta / Your Repositories'. 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'New'. 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En 'Repository name', escribir el nombre de la carpeta raíz de su proyecto (ejemplo, 'proyecto'). 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; La carpeta raíz no debe tener espacios, ni caracteres compuestos, ni caracteres especiales
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'Create Repository'.

#### 2.6. Se abrirá un 'Bloc de Notas'. Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B').

#### 2.7. En la ventana emergente y en el control de texto 'Buscar: ', escribir '3306' y dar click en 'Buscar siguiente'.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Va a aparecer una ventana denominada 'Connect to Github'
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en la opción 'Sign in with your browser'
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'Authentication Succeeded'. 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Escribir las credenciales de 'Github'. 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En el 'Git Bash' debe aparecer texto similar al siguiente:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enumerating objects: 3, done.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Counting objects: 100% (3/3), done.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Writing objects: 100% (3/3), 226 bytes | 226.00 KiB/s, done.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To https://github.com/SenaProfeAlbeiro/proyecto.git
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* [new branch]      main -> main
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;branch 'main' set up to track 'origin/main'.


#### 2.8. Reemplazar todos los valores donde se encentre el puerto '3306' con el puerto nuevo de trabajo, por ejemplo, '3308'. Dar click en 'cancelar' y guardar los cambios en el archivo.


#### 2.9. En el Panel de control de XAMPP y en la misma línea del servicio 'Apache' dar click en 'Config / phpMyAdmin (config.inc.php)'.

#### 2.10. Buscar la línea '$cfg['Servers'][$i]['host'] = '127.0.0.1;' y agregar el puerto nuevo '3308' de la siguiente forma:

```
$cfg['Servers'][$i]['host'] = '127.0.0.1:3308';
```

#### 2.11. En el Panel de control de XAMPP dar click en 'start' de 'MySQL' para iniciar el servicio.

#### 2.12. Comprobar que quedó de la forma correcta a través del navegador, con el siguiente enlace:

```
http://localhost:8080/phpmyadmin/
```

<div align="right"><a href="#anexo-02-problemas-de-puertos-con-xampp">Volver al Menú</a></div>

---
<div align="right">
  <table border="0">
    <tr>
      <td align="center"><a href="../../README.md">Menú Principal</a></td>
      <td align="center">1. <a href="anexo01_trabajar_con_github.md">Trabajar con Github</a></td>
    </tr>
  </table>
</div>

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->