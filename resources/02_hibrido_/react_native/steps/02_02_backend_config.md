## <h1 align="center">II. Backend</h1>
## 2. Configuración

2.1. **[Preparar del backend](#21-preparar-el-proyecto)**
<br>2.2. **[Iniciar el backend](#22-iniciar-el-proyecto)**
<br>2.3. **[Configurar el backend](#23-ejecutar-el-backend)**
<br>2.4. **[Estructurar el backend](#24-configurar-el-backend)**
<br>2.5. **[Ejecutar el backend](#25-estructurar-el-backend)**

**<div align="center"><a href="../react_native.md">Menú React Native</a></div>**

---
## 2.1. Preparar el backend
&nbsp;

#### 2.1.1. Ingresar a la carpeta "backend"

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Ingresar a la carpeta **'backend'** y eliminar el archivo **'delete'**:
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Abrir una terminal de Visual Studio Code ('Terminal / New Terminal' ó 'Ctrl + Shift + ñ')
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la terminal ir a la carpeta "backend" con el siguiente comando:

```bash
cd backend
```

#### 2.1.2. Personalizar la Terminal

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Cambiar el nombre de la terminal a **'backend'**, seleccionándola en la parte inferior derecha y presionando F2 / Rename...
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Cambiar el color de la terminal **'backend'**, dando click derecho / Chage Color... / Seleccionar el color
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Cambiar el icono de la terminal **'backend'**, dando click derecho / Chage Icon... / Seleccionar el icono

**<div align="right"><a href="#punto-2-configuración-del-proyecto">Volver al Menú</a></div>**

---
## 2.2. Iniciar el backend
&nbsp;

#### 2.2.1. Crear el 'package.json'

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la Terminal de 'Visual Studio Code' digitar lo siguiente:

```powershell
ni package.json -ItemType File -Force
```

**<div align="right"><a href="#punto-2-configuración-del-proyecto">Volver al Menú</a></div>**

---
## 2.3. Configurar el backend
&nbsp;

#### 2.2.1. Configurar el 'package.json'

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Copiar y pegar el siguiente código en el archivo 'package.json':

```json
 1  {
 2    "name": "api_nodejs_express",
 3    "version": "1.0.0",
 4    "description": "",
 5    "main": "index.js",
 6    "scripts": {
 7      "start": "node server.js",
 8      "dev": "nodemon index.js",
 9      "test": "echo \"Error: no test specified\" && exit 1"
10    },
11    "keywords": [
12      "api",
13      "nodejs",
14      "express"
15    ],
16    "author": "Albeiro Ramos",
17    "license": "MIT",
18    "dependencies": {
19      "bcryptjs": "^3.0.2",
20      "cors": "^2.8.5",
21      "dotenv": "^17.2.3",
22      "express": "^4.21.2",
23      "http": "^0.0.1-security",
24      "jsonwebtoken": "^9.0.2",
25      "morgan": "^1.10.0",
26      "mysql": "^2.18.1",
27      "passport": "^0.7.0",
28      "passport-jwt": "^4.0.1",
29      "swagger-jsdoc": "^6.2.8",
30      "swagger-ui-express": "^5.0.1"
31    },
32    "devDependencies": {
33      "nodemon": "^3.1.11"
34    }
35  }
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Instalar las dependencias:

```bash
npm i
```

**<div align="right"><a href="#punto-2-configuración-del-proyecto">Volver al Menú</a></div>**

---
## 2.4. Estructurar el backend
&nbsp;

#### 2.4.1. Modificar el archivo 'package.json' 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Parar la ejecución del backend, presionando **Ctrl + C** en la terminal de Visual Studio Code.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Incluir en el código del 'package.json' las dependencias para asegurar que el backend funcione correctamente:
                    
```json
 1    {
 2      "name": "frontend",
 3      "version": "1.0.0",
 4      "main": "index.ts",
 5      "dependencies": {
 6        "expo": "~57.0.23",
 7        "expo-status-bar": "~57.0.1",
 8        "react": "19.2.3",
 9        "react-dom": "19.2.3",
10        "react-native": "0.86.3",
11        "react-native-web": "^0.21.2",
12        "@react-native-async-storage/async-storage": "2.2.0",
13        "@react-navigation/native": "^7.1.28",
14        "@react-navigation/native-stack": "^7.10.1",    
15        "@react-navigation/stack": "^7.6.16",
16        "axios": "^1.13.2",
17        "react-native-safe-area-context": "~5.6.0",
18        "react-native-screens": "~4.16.0"    
19      },
20      "devDependencies": {
21        "@expo/ngrok": "^4.1.3",
22        "@types/react": "~19.2.2",
23        "typescript": "~6.0.3"
24      },
25      "scripts": {
26        "start": "expo start --tunnel --clear",
27        "start:local": "expo start --host lan --clear",
28        "start:offline": "expo start --offline --clear",
29        "android": "expo start --android",
30        "ios": "expo start --ios",
31        "web": "expo start --web"
32      },
33      "private": true
34    }
```

#### 2.4.2. Instalar las dependencias del backend:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Actualizar las dependencias incluidas en el **'package.json'** desde la terminar de Visual Studio Code el siguiente comando:

```bash
npm i
```

**<div align="right"><a href="#punto-2-configuración-del-proyecto">Volver al Menú</a></div>**

---
## 2.5. Ejecutar el backend
&nbsp;

#### 2.5.1. Estructura del backend:

	# C = Carpetas
	# A = Archivos

	proyecto/                                      		     # C. Proyecto móvil en React Native.
	└── frontend/                                     		 # C. Carpeta raíz del backend en React Native.
			├── .claude/                                     # C. Importaciones al proyecto que vienen de 'Claude'
			├── .expo/                                       # C. Configuraciones del backend utilizados por 'Expo'
			├── assets/                                      # C. Recursos estáticos (imágenes, fuentes).
			├── node_modules/                                # C. Dependencias (librerías) instaladas para el frontend.
			├── src/                                         # C. Carpetas y archivos de la aplicación React Native.
			│   ├── data/                                    # C. Capa para obtención y manipulación de datos.
			│   │   ├── repositories/                        # C. Interfaces para acceder a diferentes fuentes de datos.
			│   │   │   ├── AuthRepository.tsx               # A. Lógica para la autenticación.
			│   │   │   └── UserLocalRepository.tsx          # A. Gestión de datos del usuario a nivel local (AsyncStorage).
			│   │   └── sources/                             # C. Implementaciones  de las fuentes de datos (local, remota).
			│   │       ├── local/                           # C. Lógica para acceder a datos almacenados localmente.
			│   │       │   └── LocalStorage.tsx             # A. Interactua con el almacenamiento local (AsyncStorage).
			│   │       └── remote/                          # C. Interactua con la API del backend (clientes API).
			│   │           ├── api/                         # C. Clientes o servicios para realizar llamadas a la API.
			│   │           │   └── ApiDelivery.tsx          # A. Cliente para interactuar la API con "delivery".
			│   │           └── models/                      # C. Estructuras de datos que se reciben de la API.
			│   │               └── ResponseApiDelivery.tsx	 # A. Tipo de la respuesta de la API de "delivery".
			│   ├── domain/                                  # C. Lógica de negocio y entidades del dominio (independiente).
			│   │   ├── entities/                            # C. Estructuras de los objetos del negocio (User).
			│   │   │   └── User.tsx                         # A. Entidad de usuario con sus propiedades (nombre, email).
			│   │   ├── repositories/                        # C. Interfaces para acceder a los datos (implementado en Data).
			│   │   │   ├── AuthRepository.tsx               # A. Interfaz para las operaciones de autenticación.
			│   │   │   └── UserLocalRepository.tsx          # A. Interfaz para la gestión de datos locales del usuario.
			│   │   └── useCases/                            # C. Lógica de negocio de la aplicación (dominio/data).
			│   │       ├── auth/                            # C. Casos de uso para la autenticación (Login, Register).
			│   │       │   ├── LoginAuth.tsx                # A. Lógica para el proceso de inicio de sesión del usuario.
			│   │       │   └── RegisterAuth.tsx             # A. Lógica para el proceso de registro de nuevos usuarios.
			│   │       └── userLocal/                       # C. Casos de uso relacionados con la gestión local del usuario.
			│   │           ├── GetUserLocal.tsx             # A. Obtener información del usuario almacenado localmente.
			│   │           ├── RemoveUserLocal.tsx          # A. Eliminar información del usuario almacenado localmente.
			│   │           └── SaveUserLocal.tsx            # A. Guardar la información del usuario localmente.
			│   └── presentation/                            # C. Capa de interfaz y presentación de datos (components, views).
			│       ├── components/                          # C. Componentes de interfaz de usuario (inputs, buttons).
			│       │   ├── CustomTextInput.tsx              # A. Componente de entrada de texto personalizado con estilos.
			│       │   └── RoundedButton.tsx                # A. Componente de botón con estilos de bordes redondeados.
			│       ├── hooks/                               # C. Hooks personalizados para lógica de presentación reutilizable.
			│       │   └── useUserLocal.tsx                 # A. Hook para manipular la información local del usuario.
			│       ├── theme/                               # C. Estilos y la temática visual general de la aplicación.
			│       │   └── AppTheme.tsx                     # A. Paleta de colores, tipografía y estilos consistentes.
			│       └── views/                               # C. Pantallas o vistas principales de la aplicación.
			│           ├── home/                            # C. Archivos relacionados con la pantalla principal.
			│           │   ├── Home.tsx                     # A. Componente principal de la pantalla inicio (Home).
			│           │   ├── Styles.tsx                   # A. Estilos para los componentes de la pantalla inicio.
			│           │   └── ViewModel.tsx                # A. Lógica de presentación para la pantalla inicio.
			│           ├── profile/                         # C. Archivos relacionados con el perfil del usuario.
			│           │   └── info/                        # C. Archivos relacionados con el perfil del usuario.
			│           │       ├── ProfileInfo.tsx          # A. Componente para mostrar información del perfil del usuario.
			│           │       └── ViewModel.tsx            # A. Lógica de presentación para el perfil del usuario.
			│           └── register/                        # C. Archivos relacionados con la pantalla de registro de usuarios.
			│               ├── Register.tsx                 # A. Componente principal de la pantalla de registro de usuarios.
			│               ├── Styles.tsx                   # A. Estilos para los componentes de la pantalla de registro.
			│               └── ViewModel.tsx                # A. Lógica de presentación para la pantalla registro de usuarios.
			├── .gitignore                                   # A. Archivos y carpetas que Git debe ignorar.
			├── AGENTS.md                                    # A. Archivo específico para trabajar con Agentes de Claude.
			├── app.json                                     # A. Configuración utilizada por Expo para configurar la app.
			├── App.tsx                                      # A. Raíz de la aplicación React Native (punto de entrada UI).
			├── CLAUDE.md                                    # A. Contexto para los asistentes de IA (como Claude Code)
			├── index.ts                                     # A. Punto de entrada para la aplicación React Native.
			├── LICENSE                                      # A. Define qué se puede y qué no puede hacer en el código.
			├── package-lock.json                            # A. Registra las versiones de las dependencias del frontend.
			├── package.json                                 # A. Manifiesto del frontend (nombre, dependencias, scripts).
			└── tsconfig.json                                # A. Configuración para el compilador de TypeScript.


#### 2.5.2. Crear la Estructura del backend:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Crear las **Carpetas** y **Archivos** del backend, copiando el siguiente código:

```bash
mkdir -p src/data
mkdir -p src/data/repositories
ni src/data/repositories/AuthRepository.tsx -ItemType File -Force
ni src/data/repositories/UserLocalRepository.tsx -ItemType File -Force
mkdir -p src/data/sources
mkdir -p src/data/sources/local
ni src/data/sources/local/LocalStorage.tsx -ItemType File -Force
mkdir -p src/data/sources/remote
mkdir -p src/data/sources/remote/api
ni src/data/sources/remote/api/ApiDelivery.tsx -ItemType File -Force
mkdir -p src/data/sources/remote/models
ni src/data/sources/remote/models/ResponseApiDelivery.tsx -ItemType File -Force
mkdir -p src/domain
mkdir -p src/domain/entities
ni src/domain/entities/User.tsx -ItemType File -Force
mkdir -p src/domain/repositories
ni src/domain/repositories/AuthRepository.tsx -ItemType File -Force
ni src/domain/repositories/UserLocalRepository.tsx -ItemType File -Force
mkdir -p src/domain/useCases
mkdir -p src/domain/useCases/auth
ni src/domain/useCases/auth/LoginAuth.tsx -ItemType File -Force
ni src/domain/useCases/auth/RegisterAuth.tsx -ItemType File -Force
mkdir -p src/domain/useCases/userLocal
ni src/domain/useCases/userLocal/GetUserLocal.tsx -ItemType File -Force
ni src/domain/useCases/userLocal/RemoveUserLocal.tsx -ItemType File -Force
ni src/domain/useCases/userLocal/SaveUserLocal.tsx -ItemType File -Force
mkdir -p src/presentation
mkdir -p src/presentation/components
ni src/presentation/components/CustomTextInput.tsx -ItemType File -Force
ni src/presentation/components/RoundedButton.tsx -ItemType File -Force
mkdir -p src/presentation/hooks
ni src/presentation/hooks/useUserLocal.tsx -ItemType File -Force
mkdir -p src/presentation/theme
ni src/presentation/theme/AppTheme.tsx -ItemType File -Force
mkdir -p src/presentation/views
mkdir -p src/presentation/views/home
ni src/presentation/views/home/Home.tsx -ItemType File -Force
ni src/presentation/views/home/Styles.tsx -ItemType File -Force
ni src/presentation/views/home/ViewModel.tsx -ItemType File -Force
mkdir -p src/presentation/views/profile
mkdir -p src/presentation/views/profile/info
ni src/presentation/views/profile/info/ProfileInfo.tsx -ItemType File -Force
ni src/presentation/views/profile/info/ViewModel.tsx -ItemType File -Force
mkdir -p src/presentation/views/register
ni src/presentation/views/register/Register.tsx -ItemType File -Force
ni src/presentation/views/register/Styles.tsx -ItemType File -Force
ni src/presentation/views/register/ViewModel.tsx -ItemType File -Force

```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Pegar el código en la terminal (Verificar que esté en **..\frontend>**) y presione la tecla **ENTER**.

#### 2.5.3. Cargar las imágenes del backend a la carpeta '../frontend/assets':

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Copiar las imágenes del backend que se encuentran en la carpeta: 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **../resources/02_hibrido_/react_native/assets**.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Pegar las imágenes en la carpeta **'../frontend/assets'**. 

**<div align="right"><a href="#punto-2-configuración-del-proyecto">Volver al Menú</a></div>**

---
<div align="right">
  <table border="0">
    <tr>      
      <td align="center">1. <a href="01_entorno.md">Entorno de Desarrollo</a></td>
      <td align="center"><a href="../react_native.md">Menú Principal de React</a></td>
      <td align="center">3. <a href="03_frontend.md">Frontend</a></td>
    </tr>
  </table>
</div>

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->