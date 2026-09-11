## Punto 2: Estructura del Proyecto

1. [Iniciar el Proyecto](#1-crear-la-carpeta-raíz-del-proyecto)
2. [Ejecutar 'frontend_mob' en el emulador Android](#2-ejecutar-frontend_mob-en-el-emulador-android)
3. [Ejecutar 'frontend_mob' en un dispositivo físico Android](#3-ejecutar-frontend_mob-en-un-dispositivo-físico-android)
4. [Modificar el mensaje de inicio del proyecto en 'frontend_mob/App.tsx'](#4-modificar-el-mensaje-de-inicio-del-proyecto-en-frontend_mobapptsx)
5. [Crear la Estructura de Carpetas y Archivos del Proyecto](#5-crear-la-estructura-de-carpetas-y-archivos-del-proyecto)


---
&nbsp;
## 1. Iniciar el Proyecto
&nbsp;

1.1. Descargar el '.ZIP' del Repositorio [07_Computacion_movil](https://github.com/UniminutoProfeAlbeiro/07_computacion_movil/tree/main) en GitHub (Download ZIP).

1.2. Descomprimir el '.ZIP' y cambiar el nombre del proyecto.

1.3. Abrir su cuenta Github y crear un repositorio con el nombre proyecto ([Ver anexo01_subir_proyecto_github](../../../anexos/anexo01_subir_proyecto_github.md)).

1.4. Abrir el proyecto con Visual Studio Code.

1.5. Abrir una terminal de Visual Studio Code para crear el proyecto con el siguiente comando:

```bash
npx create-expo-app frontend_mob --template blank-typescript
```

	Creating an Expo project using the blank-typescript template.

	√ Downloaded and extracted project files.
	> npm install
                    
1.6. Modificar el 'package.json' para que funcione con el Emulador:
                    
```bash
{
	"name": "frontend_mob",
	"version": "1.0.0",
	"main": "index.ts",
	"scripts": {
		"start": "expo start",
		"android": "expo start --android",
		"ios": "expo start --ios",
		"web": "expo start --web"
	},
	"dependencies": {
		"@react-native-async-storage/async-storage": "2.2.0",
		"@react-navigation/native": "^7.1.28",
		"@react-navigation/native-stack": "^7.10.1",
		"@react-navigation/stack": "^7.6.16",
		"axios": "^1.13.2",
		"expo": "~54.0.32",
		"expo-status-bar": "~3.0.9",
		"react": "19.1.0",
		"react-native": "0.81.5",
		"react-native-safe-area-context": "~5.6.0",
		"react-native-screens": "~4.16.0"
	},
	"devDependencies": {
		"@types/react": "~19.1.0",
		"typescript": "~5.9.2"
	},
	"private": true
}
```

1.7. Modificar el 'package.json' para que funcione sin el Emulador:
                    
```bash
{
	"name": "frontend_mob",
	"version": "1.0.0",
	"main": "index.ts",
	"scripts": {    
		"start": "expo start --tunnel --clear",
		"start:local": "expo start --host lan --clear",
		"start:offline": "expo start --offline --clear",
		"android": "echo 'NO USAR - Busca emulador' && exit 1",
		"ios": "echo 'NO USAR - Busca emulador' && exit 1",
		"web": "expo start --web"
	},
	"dependencies": {
		"@react-native-async-storage/async-storage": "2.2.0",
		"@react-navigation/native": "^7.1.28",
		"@react-navigation/native-stack": "^7.10.1",
		"@react-navigation/stack": "^7.6.16",
		"axios": "^1.13.2",
		"expo": "~54.0.32",
		"expo-status-bar": "~3.0.9",
		"react": "19.1.0",
		"react-native": "0.81.5",
		"react-native-safe-area-context": "~5.6.0",
		"react-native-screens": "~4.16.0"
	},
	"devDependencies": {
		"@types/react": "~19.1.0",
		"typescript": "~5.9.2"
	},
	"private": true
}

```

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 2. Ejecutar 'frontend_mob' en el emulador Android
&nbsp;

2.1. [Desacargar Node.js](https://nodejs.org/es/)

2.2. Instalar Node.js

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 3. Ejecutar 'frontend_mob' en un dispositivo físico Android
&nbsp;

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
## 4. Modificar el mensaje de inicio del proyecto en 'frontend_mob/App.tsx'
&nbsp;

4.1. [Desacargar Android Studio](https://developer.android.com/studio?hl=es-419)

4.2. Instalar Android Studio

      Dejar habilitado:   ☑ 'Android Virtual Device'.
      Dar clic a 'Don't send' / 'Next' / 'Next' / '☑ Acepto' / 'Finalizar'.


NOTA:

Si la instalación no sale como se espera porque hay una versión de Android Studio instalada, revise el siguiente enlace para desinstalarlo totalmente y repita los pasos 4.1 y 4.2: [Desinstalar completamente Android Studio](https://blog.buhoos.com/como-desinstalar-completamente-android-studio-de-windows-10/)

En caso que los archivos y/o carpetas no se dejen eliminar, descargue el siguiente programa para eliminar carpetas o archivos: [iobit-unlocker](https://www.iobit.com/es/iobit-unlocker.php#)

<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
&nbsp;
## 5. Crear la Estructura de Carpetas y Archivos del Proyecto
&nbsp;

5.1. Seleccionar 'More Actions / Virtual Device Manager'

5.2. Seleccionar la opción '(+) Create Virtual Device' y buscar un emulador que tenga los servicios de Google Service para probar las
    aplicaciones sin restricciones

5.3. Seleccionar, por ejemplo, 'Pixel 4' con el icono de Play Store

5.4. Dar click a 'Finish / Finish'.

5.5. Ejecutar el Emulador dando clic en la punta de flecha (columna 'Actions', la primera vez demorará más tiempo)


<div align="right"><a href="#punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
Paso 2. [Estructura del Proyecto](02_estructura_del_proyecto.md)

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->