# Política de privacidad — Widget de NiHaru para Android

*Una app de Niharu* · Última actualización: 3 de octubre de 2026

🇬🇧 [Read this policy in English](privacy-policy.md)

## 1. Qué cubre esta política

Esta política se aplica **solo al widget de NiHaru para Android** (paquete `app.niharu.widget`), una app companion sin ícono en el launcher que muestra una palabra o un kanji de japonés en tu pantalla de inicio.

El widget **no usa tu cuenta de NiHaru** ni ningún inicio de sesión. Si usás el sitio web [niharuapp.com](https://niharuapp.com), esa experiencia se rige por su propia política de privacidad en el sitio.

## 2. Quién es responsable

- **Responsable del tratamiento:** Santiago Agustín Playa, desarrollador y titular de NiHaru.
- **Domicilio legal:** Ciudad Autónoma de Buenos Aires, Argentina. El domicilio completo está disponible ante requerimiento de la autoridad de control.
- **Contacto:** hola@niharuapp.com

## 3. Qué datos se recopilan

| Dato | Para qué sirve | Dónde queda |
|------|----------------|-------------|
| **Hash del dispositivo**: huella SHA-256 del identificador `ANDROID_ID`, calculada en tu teléfono. El `ANDROID_ID` en claro nunca sale del dispositivo | Evitar abuso y poder bloquear instalaciones que dañen el servicio | Servidor y dispositivo |
| **Hash de tu dirección IP** (HMAC-SHA256 con una clave secreta del servidor). La IP en claro no se guarda | Aplicar límites de uso y bloqueos por abuso | Servidor |
| **Clave de instalación (`widgetKey`)**: un identificador aleatorio (UUID) que emite el servidor la primera vez que usás el widget | Identificar tu instalación de forma anónima en cada pedido de contenido | Servidor y dispositivo |
| **Última actividad**: la fecha y hora de tu último pedido de contenido (un único valor que se sobrescribe, sin historial) | Detectar instalaciones inactivas o abusivas | Servidor |
| **Filtros que elegís** (nivel JLPT, tipo de palabra, frecuencia, categoría) | Devolverte contenido acorde. Viajan en cada pedido pero **no se guardan** en el servidor | Solo en tu dispositivo |
| **Configuración visual y último contenido mostrado** (modo, campos visibles, color, opacidad, intervalo de refresco) | Que el widget se vea y funcione como lo configuraste | Solo en tu dispositivo |

Además, al procesar cada pedido, el servidor ve temporalmente tu dirección IP, como cualquier servidor web. La usa para aplicar límites de uso en memoria y no la registra en sus logs de la aplicación.

## 4. Qué datos NO se recopilan

- Ubicación, contactos, cuentas del dispositivo, identificador de publicidad, versión de la app ni del sistema operativo.
- Nombre, email, contraseña o cualquier dato de una cuenta de NiHaru.
- Analítica o telemetría: no hay SDK de analítica ni de reporte de fallos en el widget, y no se registran tus toques, la cantidad de refrescos ni los errores.
- Historial de estudio: el servidor no guarda qué palabras o kanji te mostró.

El widget solo declara los permisos de Android `INTERNET` y `ACCESS_NETWORK_STATE`.

## 5. Para qué usamos los datos

Únicamente para (a) entregarte el contenido del widget y (b) proteger el servicio contra abuso (límites de uso y bloqueos). **No vendemos ni cedemos tus datos, no hacemos publicidad ni creamos perfiles.**

## 6. Dónde se almacenan y quién los procesa

Los datos del servidor se guardan en una base de datos PostgreSQL alojada en **Railway**. Las copias de seguridad de la base se almacenan cifradas en **Cloudflare R2** y se conservan 14 días. Estos proveedores actúan como encargados de infraestructura y pueden procesar los datos fuera de Argentina.

El widget se comunica con el servidor únicamente por HTTPS (`api.niharuapp.com`).

## 7. Cuánto tiempo se conservan

Los datos de tu instalación se conservan mientras el widget siga en uso. Desinstalar el widget detiene todo nuevo pedido al servidor. Los datos que viven solo en tu dispositivo se borran al desinstalar la app.

## 8. Copias de seguridad de Android

La app permite el respaldo automático de Android. Eso significa que la clave de instalación y el hash del dispositivo pueden incluirse en el respaldo de tu cuenta de Google, que se rige por las políticas de Google y no por esta.

## 9. Tus derechos

Como persona titular de los datos, según la Ley 25.326 de Protección de los Datos Personales de la República Argentina, tenés derecho a **acceder, rectificar y suprimir** tus datos. Como el widget es anónimo, para poder ubicar tu instalación necesitamos que nos indiques la clave de instalación; si no la tenés disponible, escribinos igual y vemos cómo ayudarte.

Podés ejercer estos derechos escribiendo a **hola@niharuapp.com**.

La **Agencia de Acceso a la Información Pública**, en su carácter de Órgano de Control de la Ley 25.326, tiene la atribución de atender las denuncias y reclamos que interpongan quienes resulten afectados en sus derechos por incumplimiento de las normas vigentes en materia de protección de datos personales.

## 10. Menores de edad

El widget no está dirigido a menores de 13 años y no pide ni recopila edad ni datos personales de identificación.

## 11. Cambios en esta política

Si cambiamos esta política, publicaremos la nueva versión en este mismo lugar y actualizaremos la fecha de arriba. El historial completo de cambios está disponible en el historial de este repositorio.

## 12. Contacto

¿Dudas sobre esta política? Escribinos a **hola@niharuapp.com**.
