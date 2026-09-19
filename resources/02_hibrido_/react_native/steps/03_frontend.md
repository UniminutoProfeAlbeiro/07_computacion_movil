# 📝Punto 3: Frontend

3.1. **[Vista del Formulario de Autoregistro](#31-vista-del-formulario-de-autoregistro)**
<br>3.2. **[Vista del Formulario de Inicio de Sesión](#32-vista-del-formulario-de-inicio-de-sesión)**

<br>

**<div align="center"><a href="../react_native.md">Menú React Native</a></div>**

---
## 3.1. Vista del Formulario de Autoregistro
&nbsp;

#### 3.1.1. Estilos Globales

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar los estilos globales 'frontend_mob/src/presentation/theme/AppTheme.tsx':

```tsx
1    export const MyColors = {
2      background: '#EEEEEE',
3      primary: '#F4991A',
4      secondary: '#E14D2A',
5    }
```

#### 3.1.2. Componente controles tipo Texto

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar el componente para los controles de 'Texto' en 'frontend_mob/src/presentation/components/CustomTextInput.tsx':

```tsx
 1    import React from 'react';
 2    import { StyleSheet, View, Image, TextInput, KeyboardType } from 'react-native';
 3    
 4    interface Props {
 5      image: any;
 6      placeholder: string;
 7      value: string;
 8      keyboardType: KeyboardType;
 9      secureTextEntry?: boolean;
10      property: string, onChangeText: (property: string, value: any) => void,
11    }
12    
13    export const CustomTextInput = ({
14      image,
15      placeholder,
16      value,
17      keyboardType,
18      secureTextEntry = false,
19      property,
20      onChangeText
21    }: Props) => {
22      return (
23        <View style={styles.formInput}>
24          <Image style={styles.formIcon} source={image} />
25          <TextInput style={styles.formTextInput}
26            placeholder={placeholder}
27            keyboardType={keyboardType}
28            value={value}
29            onChangeText={text => onChangeText(property, text)}
30            secureTextEntry={secureTextEntry}
31          />
32        </View>
33      )
34    }
35    
36    const styles = StyleSheet.create({
37      formIcon: {
38        width: 25,
39        height: 25,
40        marginTop: 5,
41      },
42      formInput: {
43        flexDirection: 'row',
44        marginTop: 30,
45      },
46      formTextInput: {
47        flex: 1,
48        borderBottomWidth: 1,
49        borderBottomColor: '#AAAAAA',
50        marginLeft: 15,
51      }
52    })
```

<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En caso de no tener cuenta en Github, crear una (**[Ver Anexo 01. Trabajar con Github](../../../anexos/anexo01_trabajar_con_github.md)**).

#### 3.1.3. Componente controles tipo Botón

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Asociar el proyecto con Visual Studio Code
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Abrir una terminal de Visual Studio Code
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ▹ &nbsp;Cambiar el nombre de la terminal a **'frontend'**, seleccionándola en la parte inferior derecha y presionando 
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; F2 / Rename...
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ▹ &nbsp;Cambiar el color de la terminal **'frontend'**, dando click derecho / Chage Color... / Seleccionar el color
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Ingresar a la carpeta **'frontend'** y eliminar el archivo **'delete'**:

#### 3.1.4. Estilos Formulario de Autoregistro



#### 3.1.5. Lógica Pantalla de Autoregistro


#### 3.1.6. Presentación Pantalla de Autoregistro



#### 3.1.7. Ajustes Finales



**<div align="right"><a href="#punto-3-frontend">Volver al Menú</a></div>**

---
## 3.2. Vista del Formulario de Inicio de Sesión
&nbsp;

#### 3.2.1. Crear el Proyecto

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; En la terminal de Visual Studio Code, crear el proyecto con el siguiente comando:

```bash
npx create-expo-app frontend --template blank-typescript
```	

&nbsp;&nbsp;&nbsp;&nbsp;? Select an Expo SDK version: » - Use arrow-keys. Return to submit.<br>
&nbsp;&nbsp;&nbsp;&nbsp;> Latest (SDK 57) - Recommended for most projects **# <ins>Seleccionar esta opción**</ins><br>
&nbsp;&nbsp;&nbsp;&nbsp;Other SDK version…<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;Creating frontend using the blank-typescript template.<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;√ Downloaded and extracted project files.<br>
&nbsp;&nbsp;&nbsp;&nbsp;> npm install<br>
&nbsp;&nbsp;&nbsp;&nbsp;npm warn deprecated uuid@7.0.3: uuid@10 and below is no longer supported.  For ESM codebases, update to uuid@latest.  For<br>
&nbsp;&nbsp;&nbsp;&nbsp;CommonJS codebases, use uuid@11 (butbe aware this version will likely be deprecated in 2028).<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;added 467 packages, and audited 468 packages in 3m<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;45 packages are looking for funding<br>
&nbsp;&nbsp;&nbsp;&nbsp;  run `npm fund` for details<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;10 moderate severity vulnerabilities<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;To address issues that do not require attention, run:<br>
&nbsp;&nbsp;&nbsp;&nbsp;  npm audit fix<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;To address all issues (including breaking changes), run:<br>
&nbsp;&nbsp;&nbsp;&nbsp;npm audit fix --force<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;Run `npm audit` for details.<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;✅ Your project is ready!<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;To run your project, navigate to the directory and run one of the following npm commands.<br>
<br>
&nbsp;&nbsp;&nbsp;&nbsp;- cd frontend<br>
&nbsp;&nbsp;&nbsp;&nbsp;- npm run android<br>
&nbsp;&nbsp;&nbsp;&nbsp;- npm run ios # you need to use macOS to build the iOS project - use the Expo app if you need to do iOS development without a Mac<br>
&nbsp;&nbsp;&nbsp;&nbsp;- npm run web<br>
&nbsp;&nbsp;&nbsp;&nbsp;? You are creating a project inside of an existing Git repository. Skip initializing a new git repository? » (Y/n) **# <ins>Escribir YES**</ins><br>
&nbsp;&nbsp;&nbsp;&nbsp;npm notice<br>
&nbsp;&nbsp;&nbsp;&nbsp;npm notice New minor version of npm available! 11.9.0 -> 11.19.1<br>
&nbsp;&nbsp;&nbsp;&nbsp;npm notice Changelog: https://github.com/npm/cli/releases/tag/v11.19.1<br>
&nbsp;&nbsp;&nbsp;&nbsp;npm notice To update run: npm install -g npm@11.19.1<br>
&nbsp;&nbsp;&nbsp;&nbsp;npm notice<br>
<br>


**<div align="right"><a href="#punto-3-frontend">Volver al Menú</a></div>**

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