# 📝Punto 3: Frontend

3.1. **[Vista del Formulario de Autoregistro](#31-vista-del-formulario-de-autoregistro)**
<br>3.2. **[Vista del Formulario de Inicio de Sesión](#32-vista-del-formulario-de-inicio-de-sesión)**

<br>

**<div align="center"><a href="../react_native.md">Menú React Native</a></div>**

---
## 3.1. Vista del Formulario de Autoregistro
&nbsp;

#### 3.1.1. Estilos Globales

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar los estilos globales 'frontend/src/presentation/theme/AppTheme.tsx':

```tsx
1    export const MyColors = {
2      background: '#EEEEEE',
3      primary: '#F4991A',
4      secondary: '#E14D2A',
5    }
```

#### 3.1.2. Componente controles tipo Texto

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar el componente para los controles de tipo **'Texto'** en 'frontend/src/presentation/components/CustomTextInput.tsx':

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

#### 3.1.3. Componente controles tipo Botón

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar el componente para controles tipo **'Botón'** en 'frontend/src/presentation/components/RoundedButton.tsx':

```tsx
 1    import React from 'react'
 2    import { TouchableOpacity, Text, StyleSheet } from 'react-native'
 3    import { MyColors } from '../theme/AppTheme';
 4    
 5    interface Props {
 6      text: string;
 7      onPress: () => void,
 8    }
 9    
10    export const RoundedButton = ({ text, onPress }: Props) => {
11      return (
12        <TouchableOpacity
13          style={styles.RoundedButton}
14          onPress={() => onPress()}
15        >
16          <Text style={styles.textButton}>{text}</Text>
17        </TouchableOpacity>
18      )
19    }
20    
21    const styles = StyleSheet.create({
22      RoundedButton: {
23        width: '100%',
24        height: 40,
25        backgroundColor: MyColors.primary,
26        alignItems: 'center',
27        justifyContent: 'center',
28        borderRadius: 10,
29      },
30      textButton: {
31        color: 'white',
32      }
33    });
```

#### 3.1.4. Estilos Formulario de Autoregistro

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar los estilos del Formulario de Autoregistro de 'frontend/src/presentation/views/register/Styles.tsx':

```tsx
 1    import { StyleSheet } from "react-native";
 2    
 3    const RegisterStyles = StyleSheet.create({
 4      container: {
 5        flex: 1,
 6        backgroundColor: 'black',
 7      },
 8      imageBackground: {
 9        width: '100%',
10        height: '100%',
11        opacity: 0.7,
12        bottom: '30%',
13      },
14      logoContainer: {
15        position: 'absolute',
16        alignSelf: 'center',
17        top: '5%',
18        alignItems: 'center',
19      },
20      logoImage: {
21        width: 100,
22        height: 100,
23      },
24      logoText: {
25        color: 'white',
26        textAlign: 'center',
27        fontSize: 20,
28        marginTop: 10,
29        fontWeight: 'bold',
30      },
31      form: {
32        width: '100%',
33        height: '70%',
34        backgroundColor: 'white',
35        position: 'absolute',
36        bottom: 0,
37        borderTopLeftRadius: 40,
38        borderTopRightRadius: 40,
39        padding: 30,
40      },
41      formText: {
42        fontWeight: 'bold',
43        fontSize: 16,
44      },
45      formIcon: {
46        width: 25,
47        height: 25,
48        marginTop: 5,
49      },
50      formInput: {
51        flexDirection: 'row',
52        marginTop: 25,
53      },
54      formTextInput: {
55        flex: 1,
56        borderBottomWidth: 1,
57        borderBottomColor: '#AAAAAA',
58        marginLeft: 15,
59      },
60      formRegister: {
61        flexDirection: 'row',
62        justifyContent: 'center',
63        marginTop: 10,
64      },
65      formRegisterText: {
66        fontStyle: 'italic',
67        color: 'orange',
68        borderBottomWidth: 1,
69        borderBottomColor: 'orange',
70        fontWeight: 'bold',
71        marginLeft: 10,
72      },
73    });
74    
75    export default RegisterStyles;
```

#### 3.1.5. Lógica Pantalla de Autoregistro

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar los estados de los controles del Formulario de Autoregistro en 'frontend/src/presentation/views/register/ViewModel.tsx':

```tsx
 1    import { useState } from "react";
 2  
 3    const RegisterViewModel = () => {
 4      const [values, setValues] = useState({
 5        name: '',
 6        lastname: '',
 7        phone: '',
 8        email: '',
 9        password: '',
10        confirmPassword: '',
11      });
12  
13      const onChange = (property: string, value: any) => {
14        setValues({ ...values, [property]: value });
15      };
16  
17      const register = () => {
18        console.log(JSON.stringify(values));
19      };
20  
21      return {
22        ...values,
23        onChange,
24        register
25      };
26    }
27  
28    export default RegisterViewModel;
```

#### 3.1.6. Presentación Pantalla de Autoregistro

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Codificar Formulario de Autoregistro en 'frontend/src/presentation/views/register/Register.tsx':

```tsx
 1    import React from 'react';
 2    import styles from './Styles';
 3    import { Text, View, Image, ScrollView } from 'react-native';
 4    import { CustomTextInput } from '../../components/CustomTextInput';
 5    import { RoundedButton } from '../../components/RoundedButton';
 6    import useViewModel from './ViewModel';
 7  
 8    export const RegisterScreen = () => {
 9  
10      const { name, lastname, phone, email, password, confirmPassword, onChange, register } = useViewModel();
11  
12      return (
13        <View style={styles.container}>
14          <Image
15            source={require('../../../../assets/chef.jpg')}
16            style={styles.imageBackground}
17          />
18          <View style={styles.logoContainer}>
19            <Image
20              source={require('../../../../assets/logo.png')}
21              style={styles.logoImage}
22            />
23            <Text style={styles.logoText}>FOOD APP</Text>
24          </View>
25          <View style={styles.form}>
26            <ScrollView>
27              <Text style={styles.formText}>REGÍSTRATE</Text>
28              <CustomTextInput
29                image={require('../../../../assets/user.png')}
30                placeholder='Nombres'
31                keyboardType='default'
32                property='name'
33                onChangeText={onChange}
34                value={name}
35              />
36              <CustomTextInput
37                image={require('../../../../assets/my_user.png')}
38                placeholder='Apellidos'
39                keyboardType='default'
40                property='lastname'
41                onChangeText={onChange}
42                value={lastname}
43              />
44              <CustomTextInput
45                image={require('../../../../assets/email.png')}
46                placeholder='Correo Electrónico'
47                keyboardType='email-address'
48                property='email'
49                onChangeText={onChange}
50                value={email}
51              />
52              <CustomTextInput
53                image={require('../../../../assets/phone.png')}
54                placeholder='Teléfono'
55                keyboardType='numeric'
56                property='phone'
57                onChangeText={onChange}
58                value={phone}
59              />
60              <CustomTextInput
61                image={require('../../../../assets/password.png')}
62                placeholder='Contraseña'
63                keyboardType='default'
64                property='password'
65                onChangeText={onChange}
66                value={password}
67                secureTextEntry={true}
68              />
69              <CustomTextInput
70                image={require('../../../../assets/confirm_password.png')}
71                placeholder='Confirmar Contraseña'
72                keyboardType='default'
73                property='confirmPassword'
74                onChangeText={onChange}
75                value={confirmPassword}
76                secureTextEntry={true}
77              />
78              <View style={{ marginTop: 10 }}>
79                <RoundedButton text='CONFIRMAR' onPress={() => register()} />
80              </View>
81            </ScrollView>
82          </View>
83        </View>
84      );
85  
86    }
```

#### 3.1.7. Ajustes Finales

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Modificar la raíz del proyecto en 'frontend/App.tsx':

```tsx
 1    import * as React from 'react';
 2    import { NavigationContainer } from '@react-navigation/native';
 3    import { createNativeStackNavigator } from '@react-navigation/native-stack';
 4    import { RegisterScreen } from './src/presentation/views/register/Register';
 5  
 6    export type RootStackParamList = {
 7      RegisterScreen: undefined;
 8    }
 9  
10    const Stack = createNativeStackNavigator<RootStackParamList>();
11  
12    const App = () => {
13      return (
14        <NavigationContainer>
15          <Stack.Navigator screenOptions={{ headerShown: false }}>
16            <Stack.Screen
17              name="RegisterScreen"
18              component={RegisterScreen}
19              options={{
20                headerShown: true,
21                title: "Registro",
22              }}
23            />
24          </Stack.Navigator>
25        </NavigationContainer>
26      );
27    };
28  
29    export default App;
```

#### 3.1.8. Ejecutar la App

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Ejecutar la terminal el siguiente comando:

```bash
npm run web # Web
```

### Nota:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ● &nbsp; Recuerde los demás comandos:

```bash
npm run android # Emulador de Android
```

```bash
npx expo start --tunnel --clear # Túnel para sortear restricciones de red
```

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