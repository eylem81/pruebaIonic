							//DOCUMENTACION APP IONIC//

	//SISTEMA//
Ionic:

   Ionic CLI                     : 6.10.1 
   Ionic Framework               : @ionic/angular 5.3.1
   @angular-devkit/build-angular : 0.901.12
   @angular-devkit/schematics    : 9.1.12
   @angular/cli                  : 9.1.12
   @ionic/angular-toolkit        : 2.3.0

Capacitor:

   Capacitor CLI   : 2.4.0
   @capacitor/core : 2.4.0


System:

   NodeJS : v12.16.2 
   npm    : 6.14.5
   OS     : Windows 10



	//FUNCIONAMIENTO//

-Por el terminal ubicarse en la carpeta del proyecto.
-Ejecutar el servidor para visualizar la vista de la app en el navegador: ionic serve.


//INTEGRACIÓN DE LOS ENDPOINTS DE BACKEND//

1.Importar HttpClientModule: se agrega en el archivo app.module.ts

2.Crear provider: ejecutamos ionic generator para crear nuestro nuevo proveedor de datos:
	ionic g provider user-service

3.En post-service.ts crearemos una variable url, donde se añadirá la url de la API y la función getPosts para hacer la petición.

4.Para mostrar los datos que devuelve el service, se importa en home.ts y se crea una variable llamada arrayPost, un método llamado getPost que llamará a la función de nuestro servicio y guardará los datos en nuestra variable. Se llama a getPost en la función ionic ionViewLoad que se ejecutará cuando la página se cargue.

5.Por último vamos a home.html donde se mostrará el contenido de los post retornados por la API.



	//ADICIONALES//


//PRUEBA DE LA APP//

-Para obtener las vistas en Android & iOS ejecutar por consola ionic lab.
-Se recomienda usar el Open fullscreen para recorrer las páginas de la app (tabs).


//BUILD PARA ANDROID & iOS//

	-ANDROID:
		-Se debe correr el comando cli: $ ionic cordova build android --prod--release
		-Esto generará un build basado en las configuraciones en el config.xml en la ruta:
		 platforms/android/app/build/outputs/apk del directorio de la app. La aplicación en ionic presentará valores por defecto en este archivo los 		 cuales pueden ser modificados para modificar el build.
		

	-iOS:
		-Requerimientos: Xcode, cuenta paga de desarrollador en Apple, un perfil válido (provisioning profile), desarrollo de aplicaciones y 		 		 certificado de distribución.
		-Agregar la plataforma iOS corriendo la línea de comandos: $ ionic cordova platform add ios
		-Una vez agregada la plataforma, correr el comando para el build: $ ionic cordova build ios --prod
		 Esto generará el código minimizado para la parte web de la aplicación y lo copiará sobre la base del código iOS. Desde allí abrir el     	  	 	 .xcworkspace archivo ubicado en ./platforms/ios para iniciar Xcode.














