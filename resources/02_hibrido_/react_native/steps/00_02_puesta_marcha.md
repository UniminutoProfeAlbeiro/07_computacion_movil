## <h1 align="center">Puesta en Marcha del Proyecto</h1>

#### 1. Garantizar en el Computador el Entorno de Desarrollo (1. [Entorno de Desarrollo](steps/01_entorno.md)).

#### 2. Clonar el proyecto desde Github (Anexo 01. [Trabajar con Github](../../anexos/anexo01_trabajar_con_github.md)).

#### 3. Asociar el Proyecto con Visual Studio Code

#### 4. Cargar la Base de Datos

#### 5. Ejecutar el Backend

<br>&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Abrir otra terminal de Visual Studio Code
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ▹ &nbsp;Cambiar el nombre de la terminal a **'backend'**, seleccionándola en la parte inferior derecha y presionando 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; F2 / Rename...
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ▹ &nbsp;Cambiar el color de la terminal **'backend'**, dando click derecho / Chage Color... / Seleccionar el color

#### 6. Ejecutar el Frontend

<br>&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Abrir una terminal de Visual Studio Code
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ▹ &nbsp;Cambiar el nombre de la terminal a **'frontend'**, seleccionándola en la parte inferior derecha y presionando 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; F2 / Rename...
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ▹ &nbsp;Cambiar el color de la terminal **'frontend'**, dando click derecho / Chage Color... / Seleccionar el color



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

#### 7. Abrir otra terminal en 'Visual Studio Code' y ejecutar los siguientes comandos:

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

#### 8. Comprobar que se ejecute correctamente la aplicación.

**<div align="center"><a href="../react_native.md">Menú React Native</a></div>**

---

<div align="right">
  <table border="0">
    <tr>      
      <td align="center"><a href="00_01_preliminares.md">Entorno de Desarrollo de la Base de Datos</a></td>
      <td align="center"><a href="../react_native.md">Menú Principal de React</a></td>
      <td align="center"><a href="01_01_db_entorno.md">Entorno de Desarrollo de la Base de Datos</a></td>
    </tr>
  </table>
</div>
<!-- ![Pantalla Principal Android](img/01_android_studio.png) -->