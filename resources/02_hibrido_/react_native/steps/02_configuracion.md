# 📝Punto 2: Configuración del Proyecto

1. **[Preparar del Proyecto](#1-iniciar-el-proyecto)**
2. **[Iniciar el Proyecto](#1-iniciar-el-proyecto)**
3. **[Ejecutar el Proyecto](#2-ejecutar-el-proyecto)**
4. **[Estructura de Carpetas y Archivos del Proyecto](#4-crear-la-estructura-de-carpetas-y-archivos-del-proyecto)**

<br>

---
## 1. Preparar el Proyecto
&nbsp;

#### 1.1. Descargar el '.ZIP' del Repositorio :

- Ir a [07_Computacion_movil](https://github.com/UniminutoProfeAlbeiro/07_computacion_movil/tree/main) y descargar el archivo '.ZIP'.

#### 1.2. Descomprimir el '.ZIP' y cambiar el nombre del proyecto.

#### 1.3. Abrir su cuenta Github y Crear un repositorio

- Colocar el nombre del proyecto al Repositorio Creado 
- En caso de no tener cuenta en Github, crear una ([Ver Anexo 01. Trabajar con Github](../../../anexos/anexo01_subir_proyecto_github.md)).

#### 1.4. Abrir el proyecto con Visual Studio Code.

#### 1.5. Abrir una terminal de Visual Studio Code e ingresar a la carpeta 'frontend':

	```bash
	cd frontend
	```

#### NOTA:

Puede cambiar el nombre y color de la Terminal de la siguiente forma:

- Cambiar el nombre de la terminal a 'frontend_mob', seleccionándola en la parte inferior derecha y presionando F2 / Rename...            
- Cambiar el color de la terminal 'frontend_mob', dando click derecho / Chage Color... / Seleccionar el color

#### 1.6. En la terminal de Visual Studio Code, crear el proyecto con el siguiente comando:

	```bash
	npx create-expo-app frontend_mob --template blank-typescript
	```

		Creating an Expo project using the blank-typescript template.

		√ Downloaded and extracted project files.
		> npm install
                    
#### 1.7. Modificar el 'package.json' 

- Modificar el código del 'package.json', para asegurar que el proyecto funcione correctamente. Se incluyen las dependencias necesarias para el proyecto, según se requiera para que funcione con o sin el emulador Android. 

- Para que funcione CON el Emulador:
                    
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

- Para que funcione SIN el Emulador:
                    
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

#### 1.8. En la terminal de Visual Studio Code ingresar al proyecto creado "frontend_mob" con el siguiente comando:

	```bash
	cd frontend_mob
	```

#### 1.9. En la terminal de Visual Studio Code instalar las dependencias necesarias para el proyecto, ya que se modificó el 'package.json' con el siguiente comando:

	```bash
	cd npm i
	```

<div align="right"><a href="#punto-2-estructura-del-proyecto">Volver al Menú</a></div>

---
## 2. Ejecutar el Proyecto
&nbsp;

2.1. CON el Emulador Android:

	```bash
	npm run android
	```

2.2. SIN el Emulador Android:

1. En el dispositivo de Android, ir a la tienda de Play Store, buscar 'Expo go' e instalarlo.
2. Abrir la aplicación 'Expo Go' en el dispositivo.
3. Ejecutar el sigiuente comando en la terminal de Visual Studio Code:

	```bash
	npx expo start --tunnel --clear
	```

4. Escanear el 'código QR' con el dispositivo. Los dos equipos deben estar en la misma red.


&nbsp;
#### NOTA:

Si tiene dificultades, abra el abra el puerto 3000 en Firewall con los siguiente pasos:

01.	Presione Windows + R, escriba wf.msc y presiona Enter															
02.	Vaya a "Reglas de entrada" en el panel izquierdo															
03.	Haga clic en "Acción" → "Nueva regla..."															
04.	Seleccione "Puerto" → Siguiente															
05.	En "Puertos locales específicos" escriba: 3000															
06.	Seleccione "Permitir la conexión" → Siguiente															
07.	Marque todas las opciones (Dominio, Privado, Público) → Siguiente															
08.	Póngale un nombre como "Puerto 3000 Backend" → Finalizar

<div align="right"><a href="#punto-2-estructura-del-proyecto">Volver al Menú</a></div>

---
## 3. Modificar el mensaje de inicio del proyecto
&nbsp;

3.1. En 'frontend_mob/App.tsx' modifique la línea 7 :

```tsx
 1    import { StatusBar } from 'expo-status-bar';
 2    import { StyleSheet, Text, View } from 'react-native';
 3  
 4    export default function App() {
 5      return (
 6        <View style={styles.container}>
 7          <Text>¡Hola Mundo!</Text>
 8          <StatusBar style="auto" />
 9        </View>
10      );
11    }
12  
13    const styles = StyleSheet.create({
14      container: {
15        flex: 1,
16        backgroundColor: '#fff',
17        alignItems: 'center',
18        justifyContent: 'center',
19      },
20    });
```

<div align="right"><a href="#punto-2-estructura-del-proyecto">Volver al Menú</a></div>

---
## 4. Crear la Estructura de Carpetas y Archivos del Proyecto
&nbsp;


	# C = Carpetas
	# A = Archivos

	proyecto/                                      		       # C. Proyecto móvil en React Native.
	└── frontend_mob/                                 		   # C. Carpeta raíz del proyecto en React Native.
			├── .expo/                                         # C. Configuraciones del proyecto utilizados por la herramienta 'Expo'
			├── assets/                                        # C. Recursos estáticos (imágenes, fuentes).
			├── node_modules/                                  # C. Dependencias (librerías) instaladas para el frontend_mob.
			├── src/                                           # C. Carpetas y archivos de la aplicación React Native.
			│   ├── data/                                      # C. Capa para obtención y manipulación de datos.
			│   │   ├── repositories/                          # C. Interfaces para acceder a diferentes fuentes de datos.
			│   │   │   ├── AuthRepository.tsx                 # A. Lógica para la autenticación.
			│   │   │   └── UserLocalRepository.tsx            # A. Gestión de datos del usuario a nivel local (AsyncStorage).
			│   │   └── sources/                               # C. Implementaciones concretas de las fuentes de datos (local, remota).
			│   │       ├── local/                             # C. Lógica para acceder a datos almacenados localmente.
			│   │       │   └── LocalStorage.tsx               # A. Interactua con el almacenamiento local (AsyncStorage).
			│   │       └── remote/                            # C. Interactua con la API del backend (clientes API).
			│   │           ├── api/                           # C. Clientes o servicios para realizar llamadas a la API.
			│   │           │   └── ApiDelivery.tsx            # A. Cliente para interactuar con la API relacionada con "delivery".
			│   │           └── models/                        # C. Estructuras de datos que se reciben de la API.
			│   │               └── ResponseApiDelivery.tsx	   # A. Tipo de la respuesta de la API de "delivery".
			│   ├── domain/                                    # C. Lógica de negocio y entidades del dominio (independiente).
			│   │   ├── entities/                              # C. Estructuras de los objetos del negocio (User).
			│   │   │   └── User.tsx                           # A. Entidad de usuario con sus propiedades (nombre, email).
			│   │   ├── repositories/                          # C. Interfaces para acceder a los datos (implementado en Data).
			│   │   │   ├── AuthRepository.tsx                 # A. Interfaz para las operaciones de autenticación.
			│   │   │   └── UserLocalRepository.tsx            # A. Interfaz para la gestión de datos locales del usuario.
			│   │   └── useCases/                              # C. Lógica de negocio específica de la aplicación (dominio/data).
			│   │       ├── auth/                              # C. Casos de uso relacionados con la autenticación (Login, Register).
			│   │       │   ├── LoginAuth.tsx                  # A. Lógica para el proceso de inicio de sesión del usuario.
			│   │       │   └── RegisterAuth.tsx               # A. Lógica para el proceso de registro de nuevos usuarios.
			│   │       └── userLocal/                         # C. Casos de uso relacionados con la gestión local del usuario.
			│   │           ├── GetUserLocal.tsx               # A. Obtener información del usuario almacenado localmente.
			│   │           ├── RemoveUserLocal.tsx            # A. Eliminar información del usuario almacenado localmente.
			│   │           └── SaveUserLocal.tsx              # A. Guardar la información del usuario localmente.
			│   └── presentation/                              # C. Capa de la interfaz y presentación de datos (components, views).
			│       ├── components/                            # C. Componentes de interfaz de usuario (inputs, buttons).
			│       │   ├── CustomTextInput.tsx                # A. Componente de entrada de texto personalizado con estilos.
			│       │   └── RoundedButton.tsx                  # A. Componente de botón con estilos de bordes redondeados.
			│       ├── hooks/                                 # C. Hooks personalizados para lógica de presentación reutilizable.
			│       │   └── useUserLocal.tsx                   # A. Hook personalizado para manipular la información local del usuario.
			│       ├── theme/                                 # C. Estilos y la temática visual general de la aplicación.
			│       │   └── AppTheme.tsx                       # A. Paleta de colores, tipografía y estilos consistentes.
			│       └── views/                                 # C. Pantallas o vistas principales de la aplicación.
			│           ├── home/                              # C. Archivos relacionados con la pantalla principal de la aplicación.
			│           │   ├── Home.tsx                       # A. Componente principal de la pantalla inicio (Home).
			│           │   ├── Styles.tsx                     # A. Estilos específicos para los componentes de la pantalla inicio.
			│           │   └── ViewModel.tsx                  # A. Lógica de presentación para la pantalla inicio.
			│           ├── profile/                           # C. Archivos relacionados con la pantalla de perfil del usuario.
			│           │   └── info/                          # C. Archivos relacionados con la información del perfil del usuario.
			│           │       ├── ProfileInfo.tsx            # A. Componente para mostrar la información del perfil del usuario.
			│           │       └── ViewModel.tsx              # A. Lógica de presentación para la información del perfil del usuario.
			│           └── register/                          # C. Archivos relacionados con la pantalla de registro de usuarios.
			│               ├── Register.tsx                   # A. Componente principal de la pantalla de registro de usuarios.
			│               ├── Styles.tsx                     # A. Estilos específicos para los componentes de la pantalla de registro.
			│               └── ViewModel.tsx                  # A. Lógica de presentación para la pantalla de registro de usuarios.
			├── .gitignore                                     # A. Archivos y carpetas que Git debe ignorar (node_modules, etc.).
			├── app.json                                       # A. Configuración utilizada por Expo para configurar la app.
			├── App.tsx                                        # A. Raíz de la aplicación React Native (punto de entrada UI).
			├── index.ts                                       # A. Punto de entrada para la aplicación React Native (fuera de Expo).
			├── package-lock.json                              # A. Registra las versiones exactas de las dependencias del frontend_mob.
			├── package.json                                   # A. Manifiesto del proyecto frontend_mob (nombre, dependencias, scripts).
			└── tsconfig.json                                  # A. Configuración para el compilador de TypeScript.

4.1. Copiar de este mismo proyecto las imágenes que se encuentra en [assets](../assets/). 

&nbsp;

NOTA:

Si está en Github, puede utilizar este recurso https://download-directory.github.io/ para descargar las imágenes pasándole el enlace

&nbsp;


4.2. Pegar las imágenes al proyecto, en la carpeta 'frontend/frontend_mob/assets'.

<div align="right"><a href="#-punto-1-entorno-de-desarrollo">Volver al Menú</a></div>

---
<div align="right">
  <table border="0">
    <tr>      
      <td align="center">1. <a href="01_entorno.md">Entorno de Desarrollo</a></td>
      <td align="center"><a href="../react_native.md">Menú Principal de React</a></td>
      <td align="center">2. <a href="03_frontend.md">Estructura del Proyecto</a></td>
    </tr>
  </table>
</div>

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->