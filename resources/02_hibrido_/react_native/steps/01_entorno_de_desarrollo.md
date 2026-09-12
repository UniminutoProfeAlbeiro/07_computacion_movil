## Punto 1: Entorno de Desarrollo

1. [Instalar Visual Studio Code](#1-instalar-visual-studio-code)
2. [Instalar Node.js](#2-instalar-nodejs)
3. [Modificar Directivas en PowerShell](#3-modificar-directivas-en-powershell)
4. [Instalar Instalar Android Studio](#4-instalar-instalar-android-studio)
5. [Crear el Emulador de Android Studio](#5-crear-el-emulador-de-android-studio)
6. [Configurar las variables de Entorno del Sistema](#6-configurar-las-variables-de-entorno-del-sistema)
7. [Instalar Expo Go](#7-instalar-expo-go)

---
&nbsp;
## 1. Instalar Visual Studio Code
&nbsp;

1. [Desacargar Visual Studio Code](https://code.visualstudio.com/download)

2. Instalar Visual Studio Code. 
		
	En el asistente de instalación dejar marcado ✅ 'Agregar PATH...'.

3. Abrir Visual Studio Code

4. Instalar los siguientes extensiones en Visual Studio Code

```
Material Icon Theme
```
```
ES7 React/Redux/React-Native snippets
```
```
Simple React Snippets
```
```
Auto Close Tag
```
```
Paste JSON as Code
```
```
TypeScript importerM
```

5. Cerrar Visual Studio Code 

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 2. Instalar Node.js
&nbsp;

1. [Desacargar Node.js](https://nodejs.org/es/)

2. Instalar Node.js

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 3. Modificar Directivas en PowerShell
&nbsp;

1. Abrir PowerShell

2. Ejecutar el siguiente comando:
      
```powershell
Get-ExecutionPolicy
```

3. Si aparece 'Restricted', hay que cambiarla a 'Unrestricted' de la siguiente forma:

```powershell
Set-ExecutionPolicy -Scope CurrentUser
```
    cmdlet Set-ExecutionPolicy en la posición 1 de la canalización de comandos
    Proporcione valores para los parámetros siguientes:
    ExecutionPolicy: 

```powershell
Unrestricted
```

4. Verificar la versión de 'node' y 'npm':

```bash
node --version # Debe mostrar v18.x.x o superior
```

```bash
npm --version # Debe mostrar v9.x.x o superior
```

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 4. Instalar Instalar Android Studio
&nbsp;

1. [Desacargar Android Studio](https://developer.android.com/studio?hl=es-419)

2. Instalar Android Studio

'Next' /  ☑ 'Android Virtual Device' / 'Next' / 'Install' / 'Next'/ 'Finish'.


NOTA:

Si la instalación no sale como se espera porque hay una versión de Android Studio instalada, revise el siguiente enlace para desinstalarlo totalmente y repita los pasos 4.1 y 4.2: [Desinstalar completamente Android Studio](https://blog.buhoos.com/como-desinstalar-completamente-android-studio-de-windows-10/)

En caso que los archivos y/o carpetas no se dejen eliminar, descargue el siguiente programa para eliminar carpetas o archivos: [iobit-unlocker](https://www.iobit.com/es/iobit-unlocker.php#)

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 5. Crear el Emulador de Android Studio
&nbsp;

1. Seleccionar 'More Actions / Virtual Device Manager'

2. Seleccionar la opción '(+) Create Virtual Device' y buscar un emulador, por ejemplo, 'Pixel 6a' con el icono de Play Store.

4. Dar click a 'Finish / Finish'.

5. Ejecutar el Emulador dando clic en la punta de flecha (columna 'Actions', la primera vez demorará más tiempo)

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 6. Configurar las variables de Entorno del Sistema
&nbsp;

1. Buscar en el menú Windows 'Editar las variables de entorno del sistema' para enrutar al SDK de Java y Android SDK

2. Dar clic en 'Variables de entorno ...'

3. En las 'Variables de Sistema ...' dar clic en 'Nueva ...'

      Nombre de la variable:  JAVA_HOME
      Valor de la variable:   'Examinar Directorio': C:\Program Files\Android\Android Studio\jbr\bin

      Nombre de la variable:  ANDROID_HOME
      Valor de la variable:   'Examinar Directorio': C:\Users\{usuario_del_sistema}\AppData\Local\Android\Sdk

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 7. Instalar Expo Go
&nbsp;

1. Buscar en el menú Windows 'Editar las variables de entorno del sistema' para enrutar al SDK de Java y Android SDK

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
<div align="right">
  <table border="0">
    <tr>
      <td align="center"><a href="#"></a></td>
      <td align="center"><a href="../react_native.md">Menú Principal de React</a></td>
      <td align="center">2. <a href="#">Estructura del Proyecto</a></td>
    </tr>
  </table>
</div>

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->