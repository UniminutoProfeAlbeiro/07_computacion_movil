# Punto 1: Entorno de Desarrollo

1. [Instalar Visual Studio Code](#1-instalar-visual-studio-code)
2. [Instalar Nodejs](#2-instalar-nodejs)
3. [Modificar Directivas en PowerShell](#3-modificar-directivas-en-powershell)
4. [Instalar Instalar Android Studio](#4-instalar-instalar-android-studio)
5. [Crear el Emulador den Android Studio](#)
6. [Configurar las variables de Entorno del Sistema](#)
---



## 1. Instalar Visual Studio Code 
<div align="right"><a href="#">Volver al Menú</a></div><br>



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

---
<br>

## 2. Instalar Node.js

2.1. [Desacargar Node.js](https://nodejs.org/es/)

2.2. Instalar Node.js

---
<br>

## 3. Modificar Directivas en PowerShell

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

```powershell
node --version # Debe mostrar v18.x.x o superior
```

```powershell
npm --version # Debe mostrar v9.x.x o superior
```

---
<br>

## 4. Instalar Instalar Android Studio

4.1. Abrir PowerShell



---
<br>

Paso 2. [Estructura del Proyecto](steps/02_estructura_del_proyecto.md)