# Portal Judicial del Distrito de San Pedro de Macorís (DJSPM)

**Asignatura:** ISW-311 Tecnologías de Internet I — Unidad I  
**Institución:** Universidad Central del Este (UCE)  
**Estudiante:** Julián Vázquez  
**Matrícula:** 2023-0715  
**Proyecto Integrador:** Sistema de Información Web, Trazabilidad Procesal y Notificaciones Electrónicas Judiciales  

---

## 1. Descripción del Proyecto

Este repositorio contiene la implementación en **HTML5 semántico estricto** de un portal web de tres páginas diseñado para el **Distrito Judicial de San Pedro de Macorís**. Su propósito institucional es proporcionar información procesal confiable, un catálogo completo de trámites y aranceles judiciales, así como una mesa digital de radicación y recepción de solicitudes ciudadanas.

El sitio ha sido construido aplicando rigurosamente los estándares del consorcio W3C y cumpliendo con la totalidad de los requisitos pedagógicos y técnicos de la asignatura:
- Tres páginas HTML interconectadas mediante navegación común (`index.html`, `servicios.html`, `contacto.html`).
- Aplicación de las **nueve familias de etiquetas HTML5**.
- Cero texto genérico o de relleno ("lorem ipsum"), empleando datos verídicos y contextualmente precisos del sistema de justicia dominicano.
- Validación con 0 errores en `validator.w3.org`.
- Publicado y accesible a través de **GitHub Pages**.

---

## 2. Mapa de Etiquetas: Las Nueve Familias en Acción

A continuación se presenta la matriz analítica de justificación técnica y semántica de las etiquetas implementadas en el sitio:

| Familia | Página y Sección | Etiquetas Usadas | ¿Por qué esa etiqueta? (Justificación Técnica y Semántica) |
|---|---|---|---|
| **1. Cimientos y estructura** | Las tres páginas (`index.html`, `servicios.html`, `contacto.html`) | `<!DOCTYPE html>`, `<html lang="es">`, `<head>`, `<meta charset="UTF-8">`, `<meta name="viewport">`, `<title>`, `<meta name="description">`, `<body>` | Establecen la base estándar de HTML5. El atributo `lang="es"` define el idioma castellano para motores de búsqueda y lectores de pantalla; `meta charset="UTF-8"` previene problemas de codificación de acentos y caracteres especiales dominicanos; `meta viewport` garantiza la correcta escala en pantallas móviles; y los `title` y `meta description` únicos en cada archivo optimizan la indexación contextual e identificación de cada página. |
| **2. Semántica estructural** | Las tres páginas (en cabecera, cuerpo y pie), `index.html` (Presentación y Novedades), `servicios.html` (Multimedia) | `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>` | Reemplazan la maquetación obsoleta con contenedores genéricos (`div`), dotando a la estructura de un significado inteligible para navegadores y motores de indexación. `<header>` y `<footer>` enmarcan la identidad y autoría institucional; `<nav>` unifica la barra de navegación; un único `<main>` alberga el contenido principal de cada página; las `<section>` agrupan temáticas coherentes con sus encabezados; `<article>` aísla el comunicado oficial como pieza informativa autónoma; y `<aside>` expone advertencias suplementarias para los juristas. |
| **3. Jerarquía y formato de texto** | `index.html` (Presentación y Novedades), `servicios.html`, `contacto.html` | `<h1>`, `<h2>`, `<h3>`, `<strong>`, `<em>`, `<mark>`, `<del>`, `<ins>`, `<abbr>`, `<small>`, `<sub>`, `<sup>`, `<code>`, `<kbd>`, `<pre>` | Aseguran una lectura jerárquica sin saltos de nivel (`h1` $\rightarrow$ `h2` $\rightarrow$ `h3`). `<strong>` y `<em>` destacan la relevancia legal y enfatizan mandatos; `<mark>` resalta la validez probatoria de las resoluciones; `<del>` e `<ins>` documentan el reemplazo histórico del expediente en papel por el digital; `<abbr>` documenta siglas como el CARD; `<sub>` y `<sup>` representan las salas ordinarias (1<sup>ra</sup> y 2<sup>da</sup>); `<small>` estipula descargos legales; y `<code>`, `<kbd>` y `<pre>` describen comandos de terminal y atajos de teclado para la consulta de firmas digitales. |
| **4. Citas y referencias** | `index.html` (Sección Presentación Institucional) | `<blockquote>`, `<cite>`, `<q>` | Permiten atribuir la autoría de declaraciones y principios jurídicos con total transparencia. `<blockquote>` enmarca la cita textual extensa del Presidente de la Corte de Apelación; `<cite>` acredita el cargo y procedencia del emisor; y `<q>` envuelve la máxima clásica procesal entre comillas tipográficas nativas sin recurrir a signos ortográficos manuales en el texto. |
| **5. Listas estructuradas** | `servicios.html` (Sección Catálogo y Radicación), `contacto.html` (Directorio de canales) | `<ul>` con `<li>` y sublista anidada, `<ol start="1">`, `<dl>`, `<dt>`, `<dd>` | Estructuran conjuntos de datos según su lógica inherente. `<ul>` con lista anidada dentro de un `<li>` permite desglosar las materias judiciales y sus tipos de litigio sin orden forzado; `<ol start="1">` numera la secuencia cronológica de cinco pasos obligatorios e inalterables para radicar una demanda; y la lista descriptiva `<dl>` con sus pares `<dt>` y `<dd>` construye el glosario terminológico institucional sobre expedientes y firmas. |
| **6. Enlaces e hipervínculos** | `contacto.html` (Sección Canales Oficiales), navegación global en las tres páginas | `<a href>` con: enlace externo (`target="_blank"` y `rel="noopener"`), protocolo `mailto:`, protocolo `tel:`, ancla interna `#id`, atributo `download` | Proveen la conectividad del portal con el exterior y con acciones del sistema operativo. El enlace externo dirige al Poder Judicial abriendo una pestaña segura protegida contra abusos por `rel="noopener"`; `mailto:` y `tel:` inician clientes de correo o llamadas a la central del palacio; el ancla interna `#formulario-solicitud` permite el desplazamiento directo sin scroll; y `download` fuerza la descarga del formulario de trámites en formato PDF. |
| **7. Multimedia y geolocalización** | `servicios.html` (Sección Contenido Multimedia y Geolocalización) | `<figure>`, `<img>` (con `alt` detallado), `<figcaption>`, `<audio>` con `<controls>` y `<source>`, `<iframe>` con `title` | Incorporan recursos interactivos accesibles. `<figure>` y `<figcaption>` unifican la ilustración alegórica de la justicia con su explicación académica; el atributo `alt` describe exhaustivamente los elementos visuales de la fotografía en lugar de usar palabras vacías; `<audio>` entrega la locución explicativa con controles nativos del navegador; e `<iframe>` embebe la cartografía abierta de la sede física incorporando un atributo `title` descriptivo para cumplir estándares de accesibilidad universal. |
| **8. Tablas de datos** | `servicios.html` (Sección Tabla Arancelaria y Plazos) | `<table>`, `<caption>`, `<thead>`, `<tbody>`, `<tfoot>`, `<tr>`, `<th>` (con `scope="col"` y `scope="row"`), `<td>`, atributos `colspan` y `rowspan` | Modela la matriz arancelaria y los tiempos de emisión procesal sin incurrir en maquetación de diseño. `<caption>` nombra formalmente el cuadro; `thead`, `tbody` y `tfoot` dividen la estructura tabular; los atributos `scope` asocian cada encabezado a su columna o fila para tecnologías asistivas; `rowspan="2"` fusiona la celda de la Cámara Civil que comprende dos trámites; y `colspan="5"` abarca la totalidad del ancho para la nota reglamentaria final. |
| **9. Formularios e interacción** | `contacto.html` (Mesa de Radicación y Solicitudes), `index.html` (Avisos) | `<form>`, `<fieldset>`, `<legend>`, `<label for>`, `<input>` (tipos: `text`, `email`, `tel`, `date`, `number`, `time`, `file`, `radio`, `checkbox`), `<select>`, `<optgroup>`, `<option>`, `<textarea>`, `<button type="submit">`, validaciones nativas (`required`, `min`, `max`, `pattern`, `minlength`), `<details>`, `<summary>`, `<time datetime>`, `<address>` | Garantiza la captura fidedigna de información procesal. Dos `<fieldset>` con `<legend>` segmentan datos personales de los procesales; `<label>` con `for` emparejado garantiza accesibilidad total; los tipos de `input` disparan interfaces y validaciones nativas; `<select>` con `<optgroup>` clasifica tribunales por competencia; `<details>` con `<summary>` despliega información a demanda; `<time datetime>` aporta fechas computables; y `<address>` normaliza la geolocalización de la sede física. |

---

## 3. Instrucciones de Despliegue en GitHub Pages

Para publicar este proyecto en **GitHub Pages**:
1. Cree un repositorio en GitHub (por ejemplo, `sitio-web-html5-djspm`).
2. Suba o empuje los archivos de este directorio a la rama principal (`main`).
3. Vaya a **Settings** $\rightarrow$ **Pages** en su repositorio.
4. En **Branch**, seleccione `main` y la carpeta `/ (root)`.
5. Presione **Save**. En un par de minutos, GitHub Pages publicará su sitio en una URL similar a:
   `https://<su-usuario>.github.io/sitio-web-html5-djspm/`

---

## 4. Datos del Estudiante (Presentes en el Footer de las 3 Páginas)
* **Nombre:** Julián Vázquez
* **Matrícula:** 2023-0715
* **Asignatura:** ISW-311 Tecnologías de Internet I
* **Universidad Central del Este (UCE)**

