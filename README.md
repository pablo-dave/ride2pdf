<p align="center">
  <a href="https://limonte.github.io/ride2pdf/">
    <img src="/site/img/ride2pdf_logo.png" alt="Ride2PDF">
  </a>
</p>

<br>

<p align="center">
  <a href="https://paypal.me/rolandopalermo/25"><img alt="PayPal Donate" src="http://ionicabizau.github.io/badges/paypal.svg"></a>
</p>

<p align="center">
  La herramienta más flexible para la generación autómatica de representaciones impresas de comprobantes electrónicos que se ajusta a los lineamientos del Sistema de Rentas Internas del Ecuador.
</p>

Instalación
-----------
1. Descargar el archivo <a href="https://github.com/rolandopalermo/ride2pdf/blob/master/ride2pdf.rar">ride2pdf.rar</a> y descomprimir en una carpeta.
2. Solicitar el token asociado al R.U.C. de la Razón Social que se utilizará para generar los documentos impresos al correo electrónico rolando.roc@gmail.com.
3. Abrir el archivo **estilos.properties** y en la propiedad **lincencia.key** agregar el token. Si se cuenta con más de uno, separárlos por una coma. Por ejemplo:
```bash
lincencia.key=7137022B685B467FE21D3417DBC7B227,H743E4D22C4279236474F16D14152BAE,11788D2F86561A04CD496FF2DD115ADA
```
4. Reemplazar el archivo logo.jpg por el logo de la empresa. La imagene debe conservar el mismo nombre, ser en formato JPG y de un tamaño recomendado de 320x210.

Utilización
-----------
1. Para generar una RIDE desde un archivo XML, especificar la ruta del archivo XML y la ruta del archivo PDF que se generará. Puede ser un XML firmado o un XML autorizado, la librería lo detectará automáticamente.
```bash
java -jar ride2pdf.jar arg0 arg1
```
| Argumento | Description                                             |
| --------- | ------------------------------------------------------- |
| `'arg0'`  | Puede tomar el valor de la ruta completa del archivo XML o la clave de acceso del comprobante electrónico previamente autorizado.|
| `'arg1'`  | Ruta completa del archivo PDF que se generará.|

Ejemplos
--------
Generación de una RIDE en Sistemas Operativos Windows
```bash
java -jar ride2pdf.jar c:\\xml\\factura.xml c:\\pdf\\factura.pdf
```
Un ejemplo para distribuciones Linux
```bash
java -jar ride2pdf.jar /home/documents/factura.xml /home/rides/factura.pdf
```
También es posibile indicarle directamente la clave de acceso del comprobante electrónico autorizado; sin embargo para esta opción es necesario tener acceso a Internet.
```bash
java -jar ride2pdf.jar 1312201721091223824600110020730000000551234567811 /home/rides/factura.pdf
```

Tipos de Documentos Soportados
------------------------------
La librería soporta los siguientes tipos de documentos:

| Tipo de Documento | Soporte |
| --------|---------|
| `Facturas`  |  ✅ |
| `Notas de Crédito`  |  ✅ |
| `Notas de Débito`  |  ✅ |
| `Comprobantes de Retención`  |  ✅ |
| `Guías de Remisión`  |  ✅ |

JDK's soportados
----------------
La librería soporta las siguientes versiones de JDK:

| 1.6.x | 1.7.x | 1.8.x |
|-------|------|--------|
|  ✅   |   ✅  |   ✅   |

Autores
-------

| [![](https://avatars1.githubusercontent.com/u/11875482?v=4&s=80)](https://github.com/rolandopalermo) |
|-|
| [@rolandopalermo](https://github.com/rolandopalermo) |
