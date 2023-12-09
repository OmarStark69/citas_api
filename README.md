#### **Tecnologias** :
[![tecnologias.png](https://i.postimg.cc/Hs85bj73/tecnologias.png)](https://postimg.cc/xcYc2f5b)


# Proyecto:
Este proyecto busca optimizar la gestión médica al ofrecer una solución tecnológica eficiente y completa que mejore la captura, almacenamiento y visualización de información médica, contribuyendo así a una atención más efectiva y organizada.
#### *Citas Medicas* :health_worker:  : 
```
El proyecto se basa en la creación de un aplicativo web con una REST API en Java utilizando SpringBoot. Se implementarán formularios HTML interactivos para la captura de datos de pacientes, doctores y citas médicas. Los formularios serán validados utilizando Java para garantizar la integridad de los datos ingresados. Se almacenará la información en una base de datos MySQL mediante operaciones POST y se visualizará de manera ordenada y accesible mediante operaciones GET en diferentes páginas web.
```
### OBJETIVO:
```
Desarrollar un aplicativo web robusto y eficiente que permita la gestión integral de información de pacientes, doctores y citas médicas a través de formularios interactivos, almacenamiento en una base de datos MySQL y visualización clara mediante páginas web generadas dinámicamente.
```
### *Justificación y Problemática Solucionada* :hospital: :
```
La gestión de información en entornos médicos suele ser compleja y crucial para la eficiencia del servicio. La falta de una plataforma integrada puede llevar a errores en los registros, dificultades en la ubicación de datos y problemas en la asignación de citas médicas. Este proyecto aborda estas problemáticas al ofrecer un sistema centralizado donde la información de pacientes, doctores y citas se captura de manera precisa, se almacena de forma segura en una base de datos y se presenta de manera clara y organizada en páginas web, facilitando así la gestión integral del sistema de atención médica.
```
### 1. Clonar el repositorio:
1. Crea una carpeta en tu escritorio o en tu lugar de trabajo.
2. Ingresar a la carpeta creada.
3.  Abrir Git Bash.
4.  Usar los siguientes comandos:
- Si estas usando Vistual estudio code:
 ```
git init
git clone https://github.com/RaulAJaimes/java-citasmedicas-springboot.git
code .
```
- Si usas Netbeans:
 ```
git init
git clone https://github.com/RaulAJaimes/java-citasmedicas-springboot.git
```
y luego usa este comando:
```
netbeans /Users/tuUsuario/Proyectos/MiProyecto
```
Recuerda que es la ruta donde esta la carpeta de tu proyecto ejemplo:
Esta es la ruta de mi proyecto:
```
C:\Users\Pepito\Desktop\java-citasmedicas-springboot
```
En el disco loca **C** esta mi proyeco y esta es la ruta para llegar a el. _**Abriendo las siguientes carpetas**_:
- Users.
  - Pepito (Mi usuario).
    - Desktop (escritorio)
      - mi carpeta de proyecto : _**java-citasmedicas-springboot**_

Por lo tanto el comando quedaria así:
```
netbeans /Users/Pepito/Desktop/java-citasmedicas-springboot
```
Esto permitira abrir Netbeans y cargar el proyecto.

### 2. Instalar las dependencias con Maven: ##

- El proyecto usa como Gestor de Dependencias: **Maven**, por tanto, encontrarás un archivo pom.xml.
- Abre una terminal en este directorio y ejecuta el siguiente comando:
```
mvn clean install
```
Este comando limpiará el proyecto **(_clean_)** y luego descargará las dependencias actualizadas y las construirá **(_install_)**.

### _*2.1 Si  quieres actualizar dependencias:*_
Utiliza el siguiente comando para actualizar las dependencias:
```
mvn clean install -U
```
- *clean*: Limpia cualquier compilación anterior y elimina archivos generados.
    - *install*: Descarga las dependencias, las instala en tu repositorio local de Maven y construye el proyecto.
       - *U*: Forzar la actualización de dependencias, descargando las versiones más recientes aunque estén en caché.
         
## _**NOTA_**: Configuración de la Base de Datos

Recuerda que el proyecto usa como gestor de base de datos MySql, y la encontraras en la carpeta:
   ```
   database.citas
   ```
`pero si decides crear tu base de datos no se te olvide lo siguiente:`

  En el archivo 
  ```application.properties``` 
  en la ruta: ```src/main/resources```, 
  ajusta la configuración:
  ```
  spring.datasource.url=jdbc:mysql://localhost:3306/nombre_de_la_base_de_datos
  spring.datasource.username=usuario_de_mysql
  spring.datasource.password=contraseña_de_mysql
  ```
  Reemplaza: 
  - ```nombre_de_la_base_de_datos``` 
  - ```usuario_de_mysql``` 
  - ```contraseña_de_mysql```
  
  Por los que has elegido usar en tu proyecto

`**Explicación más detallada de la configuración que se realiza en esos archivos:**`

```spring.datasource.url``` 
Esta propiedad indica la URL de conexión a la base de datos. 
En este caso, apunta a una base de datos MySQL en localhost en el puerto 3306. 
Deberás reemplazar ```nombre_de_la_base_de_datos``` con el nombre de tu base de datos.

```spring.datasource.username``` y ```spring.datasource.password``` 
Aquí se especifican las credenciales de usuario y contraseña para acceder a la base de datos MySQL. 
Deberás reemplazar ```usuario_de_mysql``` y ```contraseña_de_mysql``` con las credenciales reales.

Estas configuraciones permiten que la aplicación Spring Boot se conecte a la base de datos MySQL y 
realice operaciones utilizando estas credenciales y la URL proporcionada.

## Tu puerto es diferente al puerto por defecto ```port:3306```
  
```Paso 1:``` **Abrir el Archivo de Configuración**

  -  Navega hasta el archivo de configuración:
     - Abre tu proyecto y dirígete a la ruta src/main/resources.
        - **Encuentra el archivo de configuración** :
           - Busca y abre el archivo ```application.properties```

```Paso 2:``` **Cambiar el Puerto en la URL de Conexión**
        En _application.properties_:
        
        ```
        spring.datasource.url=jdbc:mysql://localhost:PUERTO/nombre_de_la_base_de_datos
        
        ```
  Reemplaza ```PUERTO``` con el número de puerto que estás utilizando en tu configuración de MySQL.

```Paso 3:``` **Reiniciar la Aplicación**
  
    - Reinicia tu aplicación Spring Boot para aplicar los cambios.
      Esto asegurará que la aplicación utilice el nuevo puerto de conexión para interactuar con la base de datos MySQL.

```Paso 4:``` **Verificación:**
  
Para verificar que la aplicación está utilizando el puerto correcto:

        - Ejecuta tu aplicación y comprueba si se conecta a la base de datos sin errores.
        - Si tu aplicación tiene logs o consola,
          busca mensajes de éxito o errores relacionados con la conexión a la base de datos 
          para confirmar que se estableció correctamente.
         
## 3. Configurar y Ejecutar el Proyecto

3.a. Abre el proyecto clonado en tu IDE preferido.
3.b. La versión mostrada en la terminal usando el comando:
```
javac -version

Es la versión del compilador Java en tu sistema.
Puede ser diferente de la versión específica del JDK configurada para este proyecto.
 ```
3.c. **conocer la configuración exacta del JDK utilizada por el proyecto:**
 - 3.c.1. Abre el archivo ```pom.xml``` en un editor de texto.
 - 3.c.2. Busca la sección
   ```
   <properties>
   o
   <java.version>
   ```
   Allí encontrarás la configuración de la versión del JDK utilizada por el proyecto.
                   
3.d. Revisar el archivo de configuración del proyecto proporciona detalles precisos sobre la versión del JDK que el proyecto está usando y puede ser diferente de la configuración del compilador en tu entorno local.

3.e. Verifica que se cargue correctamente sin errores en el IDE.

## 3.1 Entender la Estructura del Proyecto:

- Explora la estructura de directorios del proyecto. 
  - Los archivos fuente estarán en
       ``` src/main/java  ``` y los recursos en ``` src/main/resources ```.
    - Identifica la clase principal de Spring Boot. Por lo general, tiene la anotación  ```@SpringBootApplication```. Esta clase inicia la aplicación Spring Boot.

## 3.2 Ejecutar el Proyecto:

- Configura el entorno con el JDK adecuado en tu IDE.
   - Ejecuta la aplicación desde el IDE buscando y ejecutando la clase principal (aquella anotada con ```@SpringBootApplication```).
      - Verifica que la aplicación se inicie sin problemas y no aparezcan errores en la consola del IDE.

     






