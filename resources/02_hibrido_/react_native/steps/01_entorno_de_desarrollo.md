## Punto 1: Entorno de Desarrollo

1. [Instalar Visual Studio Code](#1-instalar-visual-studio-code)
2. [Instalar Nodejs](#2-instalar-nodejs)
3. [Modificar Directivas en PowerShell](#3-modificar-directivas-en-powershell)
4. [Instalar Instalar Android Studio](#4-instalar-instalar-android-studio)
5. [Crear el Emulador den Android Studio](#)
6. [Configurar las variables de Entorno del Sistema](#)

---
&nbsp;
&nbsp;


## 1. Instalar Visual Studio Code
<br>

1.1. [Desacargar Visual Studio Code](https://code.visualstudio.com/download)

1.2. Instalar Visual Studio Code

      En el asistente de instalación dejar marcado ✅ 'Agregar PATH...'.

1.3. Abrir Visual Studio Code

1.4. Instalar los siguientes extensiones en Visual Studio Code

      Material Icon Theme
      ES7 React/Redux/React-Native snippets
      Simple React Snippets
      Auto Close Tag
      Paste JSON as Code
      TypeScript importerM

1.5. Cerrar Visual Studio Code 

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
&nbsp;

## 2. Instalar Node.js
<br>

2.1. [Desacargar Node.js](https://nodejs.org/es/)

2.2. Instalar Node.js

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
&nbsp;

## 3. Modificar Directivas en PowerShell
<br>

3.1. Abrir PowerShell

3.2. Ejecutar el siguiente comando:
      
```powershell
Get-ExecutionPolicy
```

3.3. Si aparece 'Restricted', hay que cambiarla a 'Unrestricted' de la siguiente forma:

```powershell
Set-ExecutionPolicy -Scope CurrentUser
```
    cmdlet Set-ExecutionPolicy en la posición 1 de la canalización de comandos
    Proporcione valores para los parámetros siguientes:
    ExecutionPolicy: 

```powershell
Unrestricted
```

3.4. Verificar la versión de 'node' y 'npm':

```bash
node --version # Debe mostrar v18.x.x o superior
```

```bash
npm --version # Debe mostrar v9.x.x o superior
```

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
&nbsp;

## 4. Instalar Instalar Android Studio
<br>

4.1. [Desacargar Android Studio](https://developer.android.com/studio?hl=es-419)

4.2. Instalar Android Studio

      Dejar habilitado:   ☑ 'Android Virtual Device'.
      Dar clic a 'Don't send' / 'Next' / 'Next' / '☑ Acepto' / 'Finalizar'.


NOTA:

Si la instalación no sale como se espera porque hay una versión de Android Studio instalada, revise el siguiente enlace para desinstalarlo totalmente y repita los pasos 4.1 y 4.2: [Desinstalar completamente Android Studio](https://blog.buhoos.com/como-desinstalar-completamente-android-studio-de-windows-10/)

En caso que los archivos y/o carpetas no se dejen eliminar, descargue el siguiente programa para eliminar carpetas o archivos: [iobit-unlocker](https://www.iobit.com/es/iobit-unlocker.php#)

<br>
4.3. Instalar Android Studio
<br>

![Pantalla Principal Android](img/01_android_studio.png)

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
Paso 2. [Estructura del Proyecto](02_estructura_del_proyecto.md)