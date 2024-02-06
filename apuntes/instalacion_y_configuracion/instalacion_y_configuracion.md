# Instalación y configuración de entorno de trabajo

## Tipos de instalación de SASS

- Instalación global en el sistema operativo
- **Haciendo uso de Node.js**(la mas común y la que utilizaremos)
- Dart SASS
- Javascript API

## Instalación

En **Visual Studio Code**, instalaremos las siguientes extensiones:

- Live Sass Compiler
- SCSS IntelliSense
- Sass (.sass only)

*Live Sass Compiler* es la extensión que nos permitirá compilar SASS

## Configuración de entorno de trabajo

1. En nuestra carpeta principal creamos nuestro archivo `index.html`
2. Creamos nuestra carpeta `css`, esta será nuestra carpeta de **salida** (output); está carpeta no la tocaremos ya que aquí es donde se generará el archivo css que tendrá todos nuestros estilos.
3. Creamos nuestra carpeta `scss`, esta será nuestra carpeta de **entrada** (input), está carpeta sera en la cual ingresaremos nuestros estilos.
4. Dentro de `scss`, creamos nuestro archivo `main.scss`, aquí es donde escribiremos nuestros estilos que posteriormente serán compilados a *css*
5. Abrimos nuestra extensión `Live Sass Compilar`, luego vamos a la configuración de Visual Studio y buscamos *Live Sass Compile › Settings: Formats*, damos click para abrir el `json`, y buscamos las siguientes opciones

```json
        {
            "format": "expanded",
            "extensionName": ".css",
            "savePath": "/css",
            "savePathReplacementPairs": null
        }
```

6. Con *CTRL + SHIFT+ P* vamos a los comandos de Visual Studio y ponemos Live Sass: Watch Sass. Esto nos creará dos archivos en la carpeta **css**: `main.css` y `main.css.map`.
7. Finalmente en nuestro archivo `index.html` enlazaremos nuestro archivo `css/main.css`, para los estilos de nuestra página

