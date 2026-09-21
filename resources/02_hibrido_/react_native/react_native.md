###  <h2 align="center">REACT NATIVE</h2>

I.  &nbsp;&nbsp;&nbsp; **Database**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. **[Entorno de Desarrollo de la Base de Datos](steps/01_01_db_entorno.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. **[Configuración de la Base de Datos](steps/01_02_db_config.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. **[Codificación de la Base de Datos](steps/01_03_db_code.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. **[Ejecución de la Base de Datos](steps/01_04_db_ejecucion.md)**

II. &nbsp;&nbsp; **Backend**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. **[Entorno de Desarrollo del Backend](steps/02_01_backend_entorno.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. **[Configuración del Backend](steps/02_02_backend_config.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. **[Codificación del Backend](steps/02_03_backend_code.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;4. **[Pruebas del Backend con Postman](steps/02_04_backend_pruebas_postman.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;5. **[Documentación del Backend con Swagger](steps/02_05_backend_doc_swagger.md)**

III.&nbsp;&nbsp; **Frontend Móvil**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1. **[Entorno de Desarrollo del Frontend](steps/03_01_frontend_entorno.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;2. **[Configuración del Frontend](steps/03_02_frontend_config.md)**
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;3. **[Codificacion del Frontend](steps/03_03_frontend_code.md)**

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