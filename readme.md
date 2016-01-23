pasos

1) Instalación de entorno de trabajo:
    -Instalación de android-studio, para obtener el sdk de android (plataforma linux ubuntu) siguiendo el siguiente vinculo: http://developer.android.com/sdk/index.html
    -Se instalo el api de phonegap para linux, por medio del gestor de paquetes de nodejs npm, con el comando
        `npm install -g phonegap`
    -Se instala apache ant 
        `apt-get install ant`     
2) Creación del proyecto:
    - se crea la estructura del proyecto phonegap mediante el comando de consola ahora disponible 
        `phonegap create testMovil`
    - se añade las plataformas con las que se trabajará 
        `phonegap platform add android`
        `phonegap platform add ios`
3) agregamos los plugins necesarios para que la app funciones
    - se agrega el plugin de geolocalización de phonegap, mediante el comando 
        `phonegap plugin add org.apache.cordova.geolocation`
        
4) codificación, el código fuente lo pueden obervar en la carpeta www/index.html donde se muestra el mapa con lo solicitado en el test

5) construimos y ejecutamos la aplicación
    `phonegap build android`
    `phonegap run android`
    
        
        

