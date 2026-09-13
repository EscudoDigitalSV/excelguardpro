# <img src="https://i34.servimg.com/u/f34/20/32/08/60/egpro10.png" width="32" height="32"> ExcelGuard Pro 1.0.0

> ## 🔐 Protección, Desbloqueo y Cifrado Avanzado de Hojas y Libros de Excel para Windows 10 & 11
>
> ExcelGuard Pro 1.0.0 es la suite profesional de seguridad y gestión de archivos Microsoft Excel (`.xlsx`, `.xlsm`) para Windows. Integra funciones avanzadas de remoción instantánea de restricciones (`sheetProtection` y `workbookProtection`), cifrado con algoritmo militar de contraseñas de apertura (AES-256 Agile Encryption), protección con hashing SHA-512 + Salt, y un exclusivo sistema de restauración automática de contraseñas mediante respaldos cifrados ocultos.
>
> Diseñado para operar 100% de forma local sin depender de la nube, garantiza la privacidad total de tus datos financieros y reportes corporativos, ofreciendo integración directa con el menú contextual del Explorador de Windows y licenciamiento seguro RSA-4096.

---

<div align="center">
  <h2>📸 Captura de Pantalla</h2>
  <img src="https://i.servimg.com/u/f34/20/32/08/60/egpro11.png" alt="ExcelGuard Pro Interface" width="450">
</div>

---

# ✨ Funciones incluidas en esta versión Pro

ExcelGuard Pro 1.0.0 es la versión completa del proyecto e incorpora una suite avanzada de seguridad, cifrado militar y gestión de protecciones para Windows.

### 🔓 Desbloqueo Directo y Respaldo Automático Oculto (`sheetProtection` & `workbookProtection`)

Permite remover instantáneamente la protección contra escritura e inspección de hojas individuales y la estructura completa de libros de Microsoft Excel en milisegundos.

Al realizar la desprotección, el sistema genera automáticamente un archivo de respaldo oculto (`.protbak.json`) marcado con atributos de sistema (`Hidden` | `System`) en Windows. Este archivo almacena la estructura exacta de protección original sin exponer las claves.

Cada archivo procesado genera una copia desprotegida etiquetada como `_unlocked` para garantizar la integridad del archivo original y evitar sobreescrituras accidentales.

### 🔒 Protección con Estándar SHA-512 + Salt (Excel 2013+)

Permite proteger hojas de trabajo y la estructura de libros aplicando el algoritmo de hashing seguro **SHA-512** con **salt aleatorio de 16 bytes** y **100,000 iteraciones** (`spinCount`), cumpliendo rigurosamente con el estándar de seguridad de Microsoft Excel 2013 y versiones superiores.

### ♻️ Restauración Automática de la Protección Original

Gracias al sistema de respaldos ocultos `.protbak.json`, permite restaurar la protección original de un archivo previamente desbloqueado con un solo clic, restableciendo la misma contraseña que tenía inicialmente sin necesidad de recordarla ni ingresarla manualmente.

### 🔐 Cifrado Real de Apertura del Libro (AES-256 Agile Encryption)

Incorpora un módulo avanzado (`OpenPasswordDialog`) para cifrar la apertura completa del archivo mediante el estándar **Agile Encryption (AES-256)** a través de `msoffcrypto`. Este nivel de cifrado impide que el documento sea siquiera abierto o visualizado sin la contraseña correcta.

Incluye además un **medidor dinámico de fortaleza de contraseña** en tiempo real que evalúa la complejidad de la clave ingresada.

### 🖱️ Integración al Menú Contextual del Explorador de Windows

Permite registrar o remover con un clic la entrada **"Abrir con ExcelGuard Pro"** en el menú contextual del Explorador de Windows (clic derecho sobre archivos `.xlsx` y `.xlsm`).

El registro se realiza a nivel de usuario (`HKEY_CURRENT_USER`), lo que significa que **no requiere permisos de Administrador (UAC)** y admite la precarga automática de archivos al ejecutarse.

### 🔄 Almacenamiento 100% Local, Licenciamiento RSA-4096 y Privacidad

Incluye un motor autónomo desarrollado en Python/PyQt6 que no requiere conexión a Internet, servidores remotos ni librerías externas de Office.

Tus archivos financieros, reportes corporativos y datos confidenciales nunca salen de tu computadora, ofreciendo total cumplimiento con normas de seguridad de la información.

El sistema de licencias utiliza autenticación criptográfica **RSA-4096 + PKCS#1 v1.5 con SHA-256** vinculada al ID único de tu equipo (`get_machine_id()`), incluyendo un periodo de prueba (*Trial*) de 15 días respaldado por doble anclaje anti-manipulación.

Esta función es ideal para:

* 🏢 Contadores, auditores y departamentos de finanzas corporativas
* ⚖️ Abogados, administradores y consultores de empresas
* 🎓 Estudiantes y docentes que trabajan con plantillas de cálculo
* 🎒 Usuarios que gestionan presupuestos familiares o archivos personales restringidos

---

# 💎 Comparativa de Licencias y Descarga

<table>
<tr>
<th>Funciones</th>
<th>Gratis</th>
<th>Licencia Vitalicia</th>
</tr>

<tr>
<td>Desbloqueo de hojas protegidas (sheetProtection)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Desbloqueo de libros protegidos (workbookProtection)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Procesamiento 100% local (sin nube ni telemetría)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Interfaz moderna con Drag & Drop y tema oscuro</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Generación de copia segura (_unlocked)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td>Procesamiento asíncrono multihilo (QThread)</td>
<td align="center">✅</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Protección con clave real (SHA-512 + Salt Excel 2013+)</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Restaurar protección original sin contraseña (.protbak)</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Cifrado real de apertura de archivo (AES-256 Agile Encryption)</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Medidor dinámico de fortaleza de contraseñas</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Menú Contextual del Explorador de Windows (Clic Derecho)</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Apertura y precarga automática desde el sistema</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Licencia comercial segura RSA-4096 / Hardware Binding</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Soporte técnico prioritario y actualizaciones</b></td>
<td align="center">❌</td>
<td align="center">✅</td>
</tr>

<tr>
<td><b>Duración</b></td>
<td align="center"><b>GRATIS</b></td>
<td align="center"><b>PARA SIEMPRE</b></td>
</tr>

<tr>
<td><b>Acción</b></td>

<td align="center">
<a href="https://github.com/EscudoDigitalSV/excelguardpro/releases/download/v1.0.0/ExcelGuardPro.exe">
<img src="https://img.shields.io/badge/PROBAR_GRATIS-blue?style=for-the-badge&logo=windows11&logoColor=white">
</a>
</td>

<td align="center">
<a href="https://escudodigitalsv.com/excelguardpro">
<img src="https://img.shields.io/badge/🛒_COMPRAR_PRO-escudodigitalsv.com-blue?style=for-the-badge">
</a>
</td>

</tr>

</table>

---

<p align="center">
  <a href="https://github.com/EscudoDigitalSV/easyfolderlock/releases">
    <img src="https://img.shields.io/github/downloads/escudodigitalsv/easyfolderlock/total?style=for-the-badge&color=28a745&logo=github" alt="Descargas">
  </a>
</p>

---

# 🚀 ¿Por qué elegir ExcelGuard Pro?

| 💡 Beneficios Clave                           | ⚙️ Especificaciones                |
| :-------------------------------------------- | :--------------------------------- |
| 🔓 Desbloqueo y bloqueo instantáneo en tu PC. | 🖥️ Compatible con Windows 10 y 11 |
| 🛡️ Cifrado militar AES-256 para clave de apertura. | ⚡ Hashing SHA-512 + Salt + 100k Spin |
| ♻️ Restauración automática de clave original.| 🌐 Funciona completamente offline  |
| 🖱️ Menú contextual en clic derecho de Windows. | 🔑 Licenciamiento seguro RSA-4096  |
| ⚡ Interfaz responsiva con ajuste dinámico UI.| 🚀 Ejecutable portable sin inst.   |
| 📂 Generación automática de copias seguras.   | 🔏 Formato .xlsx y .xlsm soportado |

---

# ⭐ Características Principales

### 🔐 Desbloqueo, Bloqueo y Restauración Multimodal

* **Desbloquear:** Eliminación automática de protecciones de hojas (`sheetProtection`) y estructura del libro (`workbookProtection`).
* **Bloquear:** Aplicación de contraseña con hashing SHA-512 + Salt (estándar Excel 2013+).
* **Restaurar:** Recuperación de la clave de protección original mediante respaldo oculto `.protbak.json`.
* Preservación intacta del contenido de celdas, gráficos, fórmulas, formatos y código VBA/macros.

### 🛡️ Cifrado Avanzado de Apertura y Privacidad

* Cifrado y descifrado completo de apertura del libro utilizando AES-256 (Agile Encryption).
* Medidor visual de fortaleza de contraseñas (Débil, Media, Fuerte).
* Ejecución totalmente fuera de línea (offline) sin recolección de telemetría.
* Operaciones de limpieza en memoria mediante lectura y escritura Zip/XML de alto desempeño.

### ⚙️ Interfaz Gráfica, Integración y Rendimiento

* Diseño profesional en Dark Mode optimizado para evitar fatiga visual.
* Control segmentado interactivo para cambiar al instante entre los modos *Desbloquear*, *Bloquear* y *Restaurar*.
* Zona reactiva de arrastre (`DropZone`) con retroalimentación cromática y cambio de opacidad.
* Integración al Registro de Windows para habilitar el clic derecho en el Explorador.
* Arquitectura basada en hilos secundarios (`QThread`) con ajuste dinámico de altura (`_reflow_height`) para una UI 100% fluida.

---

# 🛡️ Casos de Uso

✅ Recuperar el acceso de edición a hojas de Excel con contraseña olvidada o perdida

✅ Proteger masivamente archivos contables con contraseñas robustas SHA-512 sin necesidad de Microsoft Office

✅ Cifrar la apertura completa de libros de cálculo confidenciales mediante AES-256 antes de enviarlos por correo

✅ Modificar plantillas protegidas temporalmente y restaurar su protección exacta al finalizar

✅ Trabajar de manera directa desde el Explorador de Windows mediante el clic derecho sobre archivos `.xlsx` o `.xlsm`

✅ Operar en entornos corporativos o financieros de alta seguridad totalmente sin conexión a Internet

---

# ⚠️ Nota de Seguridad

> [!CAUTION]
> ExcelGuard Pro interactúa directamente con la estructura de archivos ZIP/XML de documentos Microsoft Excel y realiza operaciones de cifrado/descifrado mediante bajo nivel de archivos temporales.
>
> Debido a este comportamiento técnico y al empaquetado autónomo del ejecutable, algunos antivirus o soluciones de seguridad pueden mostrar alertas preventivas o falsos positivos.

> [!NOTE]
> ExcelGuard Pro es un software comercial e independiente desarrollado por EscudoDigitalSV.
>
> Esta versión oficial se distribuye protegida mediante firmas digitales asimétricas RSA-4096 vinculadas al ID de máquina de cada usuario.
>
> Windows SmartScreen puede mostrar advertencias preventivas la primera vez que se ejecuta el ejecutable mientras finaliza la validación de reputación de dominio.
>
> Estas advertencias forman parte de las medidas de seguridad estándar de Windows y no indican la presencia de software malicioso.

---

# 📥 Instalación y Advertencia de Windows SmartScreen

> [!IMPORTANT]
> Al descargar ExcelGuard Pro, Windows puede mostrar la advertencia **"Windows protegió tu PC"**.
>
> Este comportamiento es normal cuando una aplicación descargada desde Internet aún no dispone de una firma de código reconocida por Microsoft.

### Pasos para continuar

1. Haz clic en **Más información**.
2. Haz clic en **Ejecutar de todas formas**.
3. Activa tu licencia `.lic` o inicia la prueba gratuita de 15 días.

<div align="center">

<img src="https://github.com/escudodigitalsv/applockerpro/blob/aea72c6f141e471c3751d2afb4370da7f3b25cf3/img/SmartScreen.gif" alt="Cómo ejecutar ExcelGuard Pro" width="250">

</div>

> [!TIP]
> Este procedimiento generalmente solo es necesario la primera vez que se ejecuta el ejecutable.

---

# 📦 Requisitos del Sistema

| Requisito         | Mínimo          |
| :---------------- | :-------------- |
| Sistema Operativo | Windows 10 / 11 |
| Arquitectura      | x64             |
| RAM               | 2 GB            |
| Espacio en Disco  | 40 MB           |
| Almacenamiento    | Disco local / Memoria USB |
| Internet          | No requerido    |

---

# 🐛 Reportar un Problema y Soporte Técnico

Si encuentras un error, deseas asistencia con tu licencia Pro o requieres soporte técnico, puedes enviarnos un correo a **soporte@escudodigitalsv.com** indicando:
* Versión de ExcelGuard Pro (v1.0.0)
* Código de Activación / Machine ID
* Pasos para reproducir el problema
* Captura de pantalla o mensaje de error, si es necesario

También puedes visitar nuestro sitio oficial en [https://escudodigitalsv.com](https://escudodigitalsv.com) o nuestro foro en [https://foro.escudodigitalsv.com/](https://foro.escudodigitalsv.com/).

> [!IMPORTANT]
> Nunca envíes archivos de Excel que contengan información confidencial o financiera personal.

---

<div align="center">

## ❤️ ExcelGuard Pro v1.0.0 © 2026

Versión oficial profesional (Pro Edition).

Protección avanzada, desprotección inteligente, restauración de contraseñas y cifrado AES-256 para Microsoft Excel.

</div>
