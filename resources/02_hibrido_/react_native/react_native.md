###  <h2 align="center">REACT NATIVE</h2>

1. [Entorno de Desarrollo](steps/01_entorno_de_desarrollo.md)
2. [Configuración del Proyecto](steps/02_estructura_del_proyecto.md)
3. [Fronend](steps/03_vista_del_formulario_de_registro.md)
**3.1. Vista del Formulario de Registro**
3.2. Vista del Formulario de Inicio de Sesión
4. [Backend](steps/05_api_restfull_de_usarios.md)
4.1 API de Usuarios
5. [Integración Backend - Frontend](steps/05_api_restfull_de_usarios.md)
5.1. Registrar un Usuario
5.2. Iniciar Sesión
5.3. Cerrar Sesión
6. [Pruebas de Software](steps/05_api_restfull_de_usarios.md)

---

&nbsp;
## 📝 Puesta en Marcha del Proyecto
&nbsp;

#### 1. Garantizar en el Computador el Entorno de Desarrollo (1. [Entorno de Desarrollo](steps/01_entorno_de_desarrollo.md)).

#### 2. Clonar el proyecto desde Github (Anexo 01. [Trabajar con Github](resources/anexos/anexo01_trabajar_con_github.md)).

#### 3. Abrir el proyecto en Visual Studio Code.

#### 4. Abrir una terminal en 'Visual Studio Code' y ejecutar los siguientes comandos:

```powershell
ipconfig
```
#### NOTA:
Tomar en cuenta la 'ipconfig' del **'node_js/server.js'** y **'my-app/src/Data/sources/remote/api/apiDelivery.tsx'** ya que deben coincidir
```powershell
cd backend
```
```powershell
npm i
```
```powershell
node index.js
```

#### 5. Abrir otra terminal en 'Visual Studio Code' y ejecutar los siguientes comandos:

```powershell
cd frontend_mob
```
```powershell
npm install -g expo-cli exp
```
```powershell
npm i
```
```powershell
npm run android
```

#### 6. Comprobar que se ejecute correctamente la aplicación.

<div align="right"><a href="#react-native">Volver al Menú</a></div>

---

<div align="right">
  <table border="0">
    <tr>      
      <td align="center"><a href="../../../README.md">Menú Principal</a></td>
      <td align="center">1. <a href="steps/01_entorno_de_desarrollo.md">Entorno de Desarrollo</a></td>
    </tr>
  </table>
</div>

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->