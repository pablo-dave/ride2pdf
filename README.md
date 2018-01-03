<h1 align="center">
  <br>
  <a href="#"><img src="https://raw.githubusercontent.com/rolandopalermo/ride2pdf/master/site/img/ride2pdf_logo.png" alt="Markdownify" width="300"></a>
  <br>
  RIDE2PDF
  <br>
</h1>

<h4 align="center">Generación autómatica de representaciones impresas de comprobantes electrónicos para Ecuador 🇪🇨.</h4>

<p align="center">
  <a href="https://paypal.me/rolandopalermo/25"><img alt="PayPal Donate" src="http://ionicabizau.github.io/badges/paypal.svg"></a>
</p>

<p align="center">
  <a href="#descarga">Descarga</a> •
  <a href="#instalaci%C3%B3n">Instalación</a> •
  <a href="#c%C3%B3mo-utilizar">Cómo utilizar</a> •
  <a href="#autores">Autores</a>
</p>

<p align="center">
  <a href="#">
    <img src="/site/img/ride2pdf_inaction.gif"><br>
    RIDE2PDF en acción ↗
  </a>
</p>


## Tabla de contenidos

- [Descarga](#descarga)
- [Instalación](#instalaci%C3%B3n)
- [Configuración](#configuraci%C3%B3n)
- [Cómo utilizar](#c%C3%B3mo-utilizar)
    - [Ejemplos](#ejemplos)
- [Soporte](#soporte)
    - [Tipos de documentos soportados](#tipos-de-documentos-soportados)
    - [JDK's soportados](#jdks-soportados)
- [Autores](#autores)

## Descarga
Puede <a href="https://github.com/rolandopalermo/ride2pdf/blob/master/ride2pdf.rar">descargar</a> la última versión estable de RIDE2PDF para Windows, macOS y Linux.

## Instalación

1. Descomprimir el archivo descargado en una carpeta nueva.
2. Solicitar el token asociado al R.U.C. de la Razón Social que se utilizará para generar los documentos impresos al correo electrónico rolando.roc@gmail.com.
3. Abrir el archivo **estilos.properties** y en la propiedad **lincencia.key** agregar el token. Si se cuenta con más de uno, separárlos por una coma. Por ejemplo:
```bash
lincencia.key=7137022B685B467FE21D3417DBC7B227,H743E4D22C4279236474F16D14152BAE,11788D2F86561A04CD496FF2DD115ADA
```
4. Reemplazar el archivo logo.jpg por el logo de la empresa. La imagen debe conservar el mismo nombre, ser en formato JPG y de un tamaño recomendado de 320x210.

## Configuración

Para personalizar la librería podemos editar el archivo **estilos.properties** configurando los valores que se requieran de acuerdo a la siguiente tabla:

| Propiedad | Valor         | Descripción |
| --------- | ------------- | ----------- |
| `'t1.borde'` | r,g,b      | Define el color de los bordes de las tablas. Se expresa en formato RGB tomando valores desde 0,0,0 hasta 255,255,255 |
| `'t1.fuente'` | r,g,b      | Define el color del texto utilizado. Se expresa en formato RGB tomando valores desde 0,0,0 hasta 255,255,255 |
| `'t1.contraste'` | r,g,b      | Define el color del texto utilizado en las tablas cuyo fondo estará relleno con el color `'t1.borde'`. Se expresa en formato RGB tomando valores desde 0,0,0 hasta 255,255,255 |
| `'img.logo'` | logo.jpg      | Ruta del archivo utilizado como logo  |
| `'fuente.nombre'` | tt0132m_.ttf      | Ruta del archivo para la fuente utilizado por la librería  |
| `'lincencia.key'` |       | Licencias asociadas a R.U.C.s autorizados para generar RIDEs  |

## Cómo utilizar

1. Para generar una RIDE, se deberá ejecutar el siguiente comando desde una consola o CMD.
```bash
java -jar ride2pdf.jar arg0 arg1
```
La descripción de los argumentos es la siguiente:
| Argumento | Description                                             |
| --------- | ------------------------------------------------------- |
| `'arg0'`  | Puede tomar el valor de la ruta completa del archivo XML o la clave de acceso del comprobante electrónico previamente autorizado.|
| `'arg1'`  | Ruta completa del archivo PDF que se generará.|

### Ejemplos

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

## Soporte

### Tipos de Documentos Soportados

La librería soporta los siguientes tipos de documentos:

| Tipo de Documento | Soporte |
| --------|---------|
| `Facturas`  |  ✅ |
| `Notas de Crédito`  |  ✅ |
| `Notas de Débito`  |  ✅ |
| `Comprobantes de Retención`  |  ✅ |
| `Guías de Remisión`  |  ✅ |

### JDK's soportados

La librería soporta las siguientes versiones de JDK:

| 1.6.x | 1.7.x | 1.8.x |
|-------|------|--------|
|  ✅   |   ✅  |   ✅   |

## Autores
-------

| [![](https://avatars1.githubusercontent.com/u/11875482?v=4&s=80)](https://github.com/rolandopalermo) |
|-|
| [@rolandopalermo](https://github.com/rolandopalermo) |
