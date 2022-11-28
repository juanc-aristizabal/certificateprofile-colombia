# certificateprofile-Colombia

## Modificar y Compilar X-Road
Antes de iniciar asegúrese de descargar el código fuente de X-Road dentro de la carpeta 'X-Road' y guardar la presente carpeta "certificateprofile-colombia" en X-Road
```
 X-Road/certificateprofile-colombia/
```

## Insertar certificados
Por medio del bash realizamos el despliege de los archivos al codigo fuente
```
chmod 777 ./insert_class.sh
./insert_class.sh  
```

### Clases para Proveedor de Certificación
La plataforma necesita conocer los campos que utilizan los certificados de su Autoridad Certificadora, para esto es necesario crear cuatro classes en Java:

* 1- SubjectClientIdDecoder:  Describe los campos incluidos en el Sujeto de los certificados, Ejemplo COLSubjectClientIdDecoder.java. Este Archivo debe incluirse en la carpeta
```
 X-Road/src/common-util/src/main/java/ee/ria/xroad/common/util/
```
* 2- SignCertificateProfileInfo: Información del certificado de Firma, Ejemplo ColSignCertificateProfileInfo.java. Este Archivo debe incluirse en la carpeta
``` 
 X-Road/src/common-util/src/main/java/ee/ria/xroad/common/certificateprofile/impl/
```
* 3- AuthCertificateProfileInfo: Información del certificado de Autenticación de clientes, Ejemplo ColAuthCertificateProfileInfo.java. Este Archivo debe incluirse en la carpeta 
```
X-Road/src/common-util/src/main/java/ee/ria/xroad/common/certificateprofile/impl/
```
* 4- CertificateProfileInfoProvider: Información del proveedor de certificados, incluye la información del certificado de firma y Autenticación, Ejemplo ColCertificateProfileInfoProvider.java. Este Archivo debe incluirse en la carpeta 
```
X-Road/src/common-util/src/main/java/ee/ria/xroad/common/certificateprofile/impl/
```

 
### Compilar la Plataforma
Para compilar el código fuente debe seguir las instrucciones del proyecto X-Road [disponible en este enlace](https://github.com/nordic-institute/X-Road/blob/develop/src/BUILD.md)

Una vez terminada la compilación los paquetes de instalación estarán disponibles en las siguientes rutas: 
```
Paquetes en X-Road/src/packages/build
```



