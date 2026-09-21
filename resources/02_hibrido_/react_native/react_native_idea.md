###  <h2 align="center">REACT NATIVE</h2>


I.  &nbsp;&nbsp;&nbsp; **[Database](steps)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. **Entorno de Desarrollo**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. **Configuración del Proyecto**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. **Codificar la Base de Datos**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. **Ejecutar la Base de Datos**

II. &nbsp;&nbsp; **[Backend](steps/)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. **Entorno de Desarrollo**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. **Configuración del Proyecto**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. **Codificar la API**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. **Pruebas de la API con Postman**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5. **Documentación con Swagger**

III.&nbsp;&nbsp; **[Frontend Móvil](steps/01_frontend_mob.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. **[Entorno de Desarrollo](steps/01_01_entorno.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. **[Configuración del Proyecto](steps/02_config_proj.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. **Autoregistro**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. **Iniciar Sesión**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. **Cerrar Sesión**

**<div align="center"><a href="../../../README.md">Menú Principal</a></div>**

---
## 📝 Puesta en Marcha del Proyecto
&nbsp;

#### 1. Garantizar en el Computador el Entorno de Desarrollo (1. [Entorno de Desarrollo](steps/01_entorno.md)).

#### 2. Clonar el proyecto desde Github (Anexo 01. [Trabajar con Github](../../anexos/anexo01_trabajar_con_github.md)).

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
      <td align="center">1. <a href="steps/01_entorno.md">Entorno de Desarrollo</a></td>
    </tr>
  </table>
</div>

<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->