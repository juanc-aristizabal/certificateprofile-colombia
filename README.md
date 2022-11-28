# certificateprofile-colombia

## Modificar y Compilar X-Road
Antes de iniciar asegúrese de descargar descargar el código fuente de X-Road dentro de la carpeta 'xroad-code'.  La versión 6.22 es la disponible al momento de escribir este documentación y puede [descargarla en este enlace](https://github.com/nordic-institute/X-Road/releases/tag/6.22.0)

### Agregar Proveedor de Certificación  
La palataforma necesita conocer los campos que utilizan los certificados de su Autoridad Certificadora, para esto es necesario crear cuatro classes en Java:

* 1- SubjectClientIdDecoder:  Describe los campos incluidos en el Sujeto de los certificados, Ejemplo SVSubjectClientIdDecoder.java. Este Archivo debe incluirse en la carpeta
```
 xroad-code/src/common-util/src/main/java/ee/ria/xroad/common/util/
```
* 2- SignCertificateProfileInfo: Información del certificado de Firma, Ejemplo TENOLISignCertificateProfileInfo.java. Este Archivo debe incluirse en la carpeta
``` 
xroad-code/src/common-util/src/main/java/ee/ria/xroad/common/certificateprofile/impl/
```
* 3- AuthCertificateProfileInfo: Información del certificado de Autenticación de clientes, Ejemplo TENOLIAuthCertificateProfileInfo.java. Este Archivo debe incluirse en la carpeta 
```
xroad-code/src/common-util/src/main/java/ee/ria/xroad/common/certificateprofile/impl/
```
* 4- CertificateProfileInfoProvider: Información del proveedor de certificados, incluye la información del certificado de firma y Autenticación, Ejemplo TENOLICertificateProfileInfoProvider.java. Este Archivo debe incluirse en la carpeta 
```
xroad-code/src/common-util/src/main/java/ee/ria/xroad/common/certificateprofile/impl/
```

 
### Compilar la Plataforma
Para compilar el código fuente debe seguir las instrucciones del proyecto X-Road [disponible en este enlace](https://github.com/nordic-institute/X-Road/blob/6.22.0/src/BUILD.md)

Una vez terminada la compilación los paquetes de instalación estarán disponibles en las siguientes rutas: 
```
Paquetes .DEB en xroad-code/src/packets/ 
Paquetes  .RPM en xroad-code/src/packets/xroad/redhat/RMPS/
```
La instalación de los paquetes DEB está [documentada en este enlace](https://github.com/egobsv/Tenoli-LAT/tree/master/ubuntu-xenial).

