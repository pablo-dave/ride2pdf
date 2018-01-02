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

Utilización
-----------
1. Ejecuta el siguiente comando en la consola de tu sistema operativo:
```bash
java -jar ride2pdf.jar [clave de acceso o la ruta del XML] [ruta donde se guardará el archivo PDF generado]
```

Colaboradores
-------------

| [![](https://avatars1.githubusercontent.com/u/11875482?v=4&s=80)](https://github.com/rolandopalermo) |
|-|
| [@rolandopalermo](https://github.com/rolandopalermo) |
