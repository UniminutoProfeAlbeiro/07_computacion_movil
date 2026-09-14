###  <h2 align="center">REACT NATIVE</h2>

1. [Entorno de Desarrollo](steps/01_entorno_de_desarrollo.md)
2. [Estructura del Proyecto](steps/02_estructura_del_proyecto.md)
3. [Vista del Formulario de Registro](steps/03_vista_del_formulario_de_registro.md)
4. [Vista del Formulario de Inicio de Sesión](steps/04_vista_del_formulario_de_inicio_de_sesion.md)
5. [API Restfull de Usuarios](steps/05_api_restfull_de_usarios.md)
6. [Registrar un Usuario](steps/06_registrar_un_usuario.md)
7. [Iniciar Sesión](steps/07_iniciar_sesion.md)
8. [Cerrar Sesión](steps/08_cerrar_sesion.md)

---

## 📝 Puesta en Marcha del Proyecto

### 1. Garantizar en el Computador el Entorno de Desarrollo 

- Ver el Apartado 1. [Entorno de Desarrollo](steps/01_entorno_de_desarrollo.md).

2. Clonar el proyecto desde Github (Anexo 01. [Trabajar con Github](resources/anexos/anexo01_trabajar_con_github.md)).

3. Abrir el proyecto en Visual Studio Code.

4. Abrir una terminal en 'Visual Studio Code' y ejecutar los siguientes comandos:

```powershell
ipconfig
```
NOTA:
Tomar en cuenta la 'ipconfig' del 'node_js/server.js' y 'my-app/src/Data/sources/remote/api/apiDelivery.tsx' ya que deben coincidir
```powershell
cd backend
```
```powershell
npm i
```
```powershell
node index.js
```

5. Abrir otra terminal en 'Visual Studio Code' y ejecutar los siguientes comandos:

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

6. Comprobar que se ejecute correctamente la aplicación.

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