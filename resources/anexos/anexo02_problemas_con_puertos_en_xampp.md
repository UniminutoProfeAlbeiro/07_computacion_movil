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

#### 2.1. Ir al archivo de configuración 'Config / my.ini'.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la misma línea del servicio 'MySQL' dar click en 'Config / my.ini'.

#### 2.2. En el Bloc de Notas

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B').
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la ventana emergente y en el control de texto 'Buscar: ', escribir '3306' y dar click en 'Buscar siguiente'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Reemplazar todos los valores donde se encentre el puerto '3306' con el puerto nuevo de trabajo, por ejemplo, '3308'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'cancelar' y guardar los cambios en el archivo.

#### 2.3. Ir al archivo de configuración 'php.ini' de 'Apache' 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la misma línea del servicio 'Apache' dar click en 'Config / Apache (php.ini)'.

#### 2.4. En el Bloc de Notas

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B').
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la ventana emergente y en el control de texto 'Buscar: ', escribir '3306' y dar click en 'Buscar siguiente'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Reemplazar todos los valores donde se encentre el puerto '3306' con el puerto nuevo de trabajo, por ejemplo, '3308'.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'cancelar' y guardar los cambios en el archivo.

#### 2.5. Ir al archivo de configuración 'config.inc.php' de 'Apache'

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la misma línea del servicio 'Apache' dar click en 'Config / Apache (config.inc.php)'.

#### 2.6. En el Bloc de Notas

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en la opción 'Edición / Buscar...' (o presionar las teclas 'CTRL + B').
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la ventana emergente y en el control de texto 'Buscar: ', escribir '$cfg['Servers'][$i]['host'] = '127.0.0.1;'
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Agregar el puerto nuevo '3308' de la siguiente forma:

```
$cfg['Servers'][$i]['host'] = '127.0.0.1:3308';
```

<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Dar click en 'cancelar' y guardar los cambios en el archivo.

#### 2.7. Iniciar el servicio 'MySQL' en el puerto nuevo de trabajo

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En el Panel de control de XAMPP dar click en 'start' de 'MySQL' para iniciar el servicio.

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