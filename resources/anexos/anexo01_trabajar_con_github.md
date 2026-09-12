## ANEXO 01: Trabajar con GitHub

1. [Subir el proyecto a un repositorio 'Github'](#1-instalar-visual-studio-code)
2. [Clonar un Proyecto 'Github'](#2-instalar-nodejs)

---
&nbsp;
## 1. Subir el proyecto a un repositorio 'Github'
&nbsp;

Para evitar confusiones y seguir los pasos correctamente, la carpeta raíz del proyecto se llamará 'proyecto'.

1.1. Verificar que no haya una cuenta de 'Github' asociada al computador, para ello, debe abrir el 'Panel de Control', dar click en 'Cuentas de usuario / Administrar credenciales de Windows'. Si hay una cuenta asociada (Ver imagen), dar click sobre la cuenta y sobre la opción 'Quitar'. 

![Pantalla Principal Android](../02_hibrido_/react_native/steps/img/github/01_github.png)

NOTA:
De no funcionar este método porque no tiene acceso al Panel de control, pruebe abriendo el 'Windows PowerShell' y digite el siguiente comando:

      
```powershell
echo "protocol=https`nhost=github.com`n" | git credential-manager erase
```

02. Abrir su cuenta de 'Github' y en la parte superior derecha, dar click al 'Nombre de su cuenta / Your Repositories'. Dar click en 'New'.
		En el control de texto 'Repository name', escribir el nombre de la carpeta raíz de su proyecto (ejemplo, 'proyecto'. La carpeta raíz no debe 
		tener espacios, ni caracteres compuesto, ni caracteres especiales) y dar click en 'Create Repository'.

				⦿  Si no tiene cuenta en 'GitHub', debe crear una.

03. Click derecho sobre la carpeta raíz (ejemplo, 'proyecto') y seleccionar la opción 'Open Git Bash here'; si no se 
		encuentra la opción, hay que instalar 'Git'.

04. En el 'Git Bash' escribir lo siguiente:

				$ git config --global user.name "nombre de su cuenta"
				$ git config --global user.email "correo de su cuenta"

				$ git init
				$ git branch -M main
				$ git remote add origin https://github.com/SenaProfeAlbeiro/proyecto.git
				$ git add .
				$ git commit -m "Subiendo Proyecto"
				$ git push -u origin main

05. Va a aparecer una ventana denominada 'Connect to Github', dar click en la opción 'Sign in with your browser', dar click en 'Authentication 
		Succeeded'. Verificar que se haya abierto en el navegador en donde tiene la cuenta activa, de lo contrario hay que escribir nuevamente las
		credenciales de 'Github'. En el 'Git Bash' debe aparecer texto similar al siguiente:

				Enumerating objects: 3, done.
				Counting objects: 100% (3/3), done.
				Writing objects: 100% (3/3), 226 bytes | 226.00 KiB/s, done.
				Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
				To https://github.com/SenaProfeAlbeiro/proyecto.git
				* [new branch]      main -> main
				branch 'main' set up to track 'origin/main'.

06. Actualizar la ventana del navegador donde se encuentra abierta su cuenta de 'Github'

07. Para actualizar la información del proyecto en 'Github', en el 'Git bash' escribir los siguientes comandos:

				$ git add .
				$ git commit -m "Comentario del cambio"
				$ git push 

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 2. Clonar un Proyecto 'Github'
&nbsp;

2.1. [Desacargar Node.js](https://nodejs.org/es/)

2.2. Instalar Node.js

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>


---
Paso 2. [Estructura del Proyecto](02_estructura_del_proyecto.md)

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->