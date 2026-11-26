# Ayudamex

**Equipo:** 7 Sistemas  
**Campus:** Toluca  
**Repositorio:** [https://github.com/pabloguioro-commits/ayudamex](https://github.com/pabloguioro-commits/ayudamex)

---

## 1. Resumen ejecutivo

**Ayudamex** es una aplicación móvil diseñada para reducir la brecha informativa que enfrentan los adultos mayores —incluyendo personas migrantes y en comunidades con baja conectividad— al gestionar trámites legales orientados a su bienestar. La plataforma centraliza información oficial, georreferencia las dependencias más cercanas y conecta con un directorio filtrado de abogados locales según la zona del usuario. Su innovación radica en integrar **Google Gemini** como un asistente conversacional multimodal (voz y texto) que traduce tecnicismos legales a un lenguaje sencillo, personaliza la interfaz y agiliza la localización y el agendamiento de citas en menos de dos segundos.

---

## 2. Boceto y concepto

### El problema
Las personas adultas mayores —especialmente aquellas en situación de vulnerabilidad, migrantes o residentes en zonas con baja conectividad y recursos limitados— sufren una marcada brecha informativa y digital. La complejidad de los términos jurídicos, la dispersión de los datos oficiales y la dificultad para identificar oficinas gubernamentales o asesoría legal cercana obstaculizan el ejercicio de sus derechos y el acceso a trámites fundamentales para su bienestar.

### Propuesta de solución
**Ayudamex** ofrece una plataforma móvil centralizada, accesible y tolerante a fallos de conexión que acompaña al usuario de principio a fin:
* **Información oficial verificada:** Centraliza requisitos y pasos claros para trámites legales.
* **Georreferenciación inteligente:** Confirma la zona o sección del usuario para mostrar dependencias públicas cercanas y un directorio de abogados locales con domicilio verificado.
* **Asistencia conversacional:** Mediante Google Gemini, el usuario interactúa por voz o texto para resolver dudas en un lenguaje claro y recibir recomendaciones adaptadas a su perfil.

### Alineación con los Objetivos de Desarrollo Sostenible (ODS)
* **ODS 10 (Reducción de las desigualdades):** Promueve la inclusión social y jurídica de adultos mayores, personas migrantes y comunidades con baja conectividad al democratizar el acceso a información legal comprensible y asesoría profesional cercana, eliminando barreras tecnológicas y lingüísticas.
* **ODS 11 (Ciudades y comunidades sostenibles):** Facilita el acceso equitativo a servicios públicos y de justicia dentro de la comunidad local mediante la georreferenciación precisa de dependencias y profesionales por zona, reduciendo traslados innecesarios y fortaleciendo el tejido comunitario.

---

## 3. Documentación funcional

A continuación se describen las capacidades y atributos principales del sistema:

* **Asistente conversacional multimodal (Voz y Texto):** Permite al usuario realizar consultas hablando o escribiendo de forma natural, recibiendo respuestas inmediatas en un lenguaje adaptado a su nivel de comprensión.
* **Traducción y simplificación de términos legales:** Procesa lenguaje jurídico complejo y lo transforma en explicaciones claras, cotidianas y fáciles de seguir.
* **Georreferenciación y filtrado por zona:** Identifica y confirma la ubicación o sección del usuario para desplegar únicamente las dependencias gubernamentales y abogados locales más cercanos, junto con sus domicilios.
* **Acceso directo a agendamiento de citas:** Integra un botón o acceso directo intuitivo que gestiona la ubicación actual para mostrar alternativas disponibles y facilitar la programación de citas.
* **Personalización dinámica de la experiencia:** Adapta las funciones y la presentación de la interfaz según el perfil y las necesidades específicas de cada usuario.
* **Usabilidad e interfaz adaptativa:** Diseño visual amigable, con navegación intuitiva pensada para personas con poca experiencia digital.
* **Alto rendimiento:** Arquitectura optimizada para garantizar tiempos de respuesta inferiores a los 2 segundos.
* **Tolerancia a fallos y disponibilidad:** Capacidad operativa para resistir pérdidas intermitentes de conexión, manteniendo la disponibilidad de la información esencial en entornos de baja conectividad.
* **Protección y seguridad de datos:** Implementación de prácticas estandarizadas de seguridad para resguardar la información personal y de ubicación del usuario.
* **Compatibilidad multidispositivo:** Estructura responsiva diseñada para operar de manera estable en distintos dispositivos móviles Android.

---

## 4. Documentación técnica

### Stack tecnológico
* **Frontend / Móvil:** Flutter (Android)
* **Backend / Lógica de servidor:** Python
* **Inteligencia Artificial:** Google Gemini API
* **Productividad y gestión de datos/citas:** Google Workspace (Docs, Sheets, Slides y Drive)
* **Entorno de desarrollo y control de versiones:** Visual Studio Code y GitHub

### Arquitectura general
El sistema opera bajo una arquitectura cliente-servidor optimizada para baja latencia (< 2 segundos) y resiliencia ante desconexiones:
1. **Capa de presentación (Flutter/Android):** Interfaz adaptativa con soporte de entrada/salida de voz y texto, almacenamiento en caché local para tolerancia a fallos de red y captura de geolocalización.
2. **Capa de servicios y procesamiento (Python):** Gestiona las peticiones del cliente, aplica las reglas de seguridad y privacidad, filtra las bases de datos de dependencias y abogados por zona geográfica y orquesta la comunicación con los servicios externos.
3. **Capa de inteligencia y ecosistema (Google Gemini & Google Workspace):** Procesa el lenguaje natural, adapta el contenido al perfil del usuario y sincroniza la disponibilidad para citas e información a través de los servicios e integraciones asociadas.

![Arquitectura del Sistema Ayudamex](image_1.png)

### Integración de Google Gemini en el flujo de la app
Google Gemini actúa como el motor central de interacción y personalización dentro de la aplicación:
1. **Recepción multimodal:** El usuario ingresa una consulta mediante voz o texto desde la pantalla principal.
2. **Comprensión y simplificación (NLP):** Gemini interpreta la intención de la consulta legal, consulta los datos oficiales y redacta una respuesta libre de tecnicismos, ajustando el tono y la complejidad según el perfil del usuario.
3. **Activación contextual de geolocalización:** Al detectar una necesidad de atención presencial o al presionar el acceso directo de citas, el sistema solicita y confirma la zona del usuario, cruzando esta información con el directorio local para desplegar dependencias y abogados cercanos con opciones disponibles para agendar.

---

## 5. Manual de usuario

Esta guía está pensada para ayudarte a usar **Ayudamex** por primera vez de forma sencilla.

### Paso 1: Instalación y acceso
1. Descarga e instala la aplicación **Ayudamex** directamente desde Google Play en tu teléfono Android.
2. Toca el ícono de **Ayudamex** en la pantalla de tu teléfono para abrirla.
3. Para empezar a usarla, es necesario realizar un breve registro utilizando tu correo electrónico o tu número de teléfono móvil. Sigue las instrucciones que aparecen en pantalla para confirmar tus datos.

### Paso 2: Configuración inicial y permisos
1. Al abrir la aplicación por primera vez, verás un mensaje pidiendo permiso para usar tu **ubicación** y tu **micrófono**.
2. Toca **"Permitir"** en ambas opciones. Esto sirve para que puedas hablar con la aplicación y para mostrarte oficinas y abogados cerca de tu casa.
3. Confirma en la pantalla si la colonia o zona que detectó el teléfono es correcta.

### Paso 3: Cómo hacer una consulta (por voz o escribiendo)
1. En la pantalla principal verás un botón grande con un micrófono y un espacio para escribir.
2. **Si prefieres hablar:** Mantén presionado el botón del micrófono, di tu duda con tus propias palabras (por ejemplo: *"¿Qué papeles necesito para tramitar mi pensión?"*) y suelta el botón.
3. **Si prefieres escribir:** Toca el recuadro de texto, escribe tu pregunta y presiona enviar.
4. En menos de dos segundos, **Ayudamex** te responderá en pantalla (y en voz alta, si lo deseas) con pasos claros y fáciles de entender.

### Paso 4: Buscar oficinas, abogados y agendar una cita
1. Si necesitas acudir en persona, toca el botón de **"Agendar cita / Atención cercana"** en la pantalla principal.
2. La aplicación te mostrará una lista con las oficinas de gobierno y los abogados locales más cercanos a tu zona, junto con su dirección exacta.
3. Selecciona la opción que mejor te quede y elige el horario disponible que prefieras para confirmar tu cita.

### ¿Qué pasa si se va el internet?
No te preocupes. Si tienes mala señal o te quedas sin datos momentáneamente, la aplicación guardará tu avance y te permitirá seguir consultando la información básica que ya habías cargado sin cerrarse ni perder tus datos.

---

## 6. Accesibilidad e impacto

### Diseño inclusivo y accesibilidad
**Ayudamex** fue concebida eliminando las barreras habituales de las aplicaciones tradicionales:
* **Interacción sin barreras de lectura o escritura:** La integración multimodal por voz permite que personas con debilidad visual, dificultades motrices o bajo nivel de alfabetización digital utilicen la herramienta con total autonomía.
* **Claridad cognitiva:** La traducción automática de jerga legal a lenguaje cotidiano evita la confusión y el abandono de trámites.
* **Adaptabilidad para zonas marginadas:** Su tolerancia a fallos de conexión y bajo consumo de recursos aseguran que funcione en dispositivos Android de gama básica y en comunidades con infraestructura de internet deficiente.

### Impacto esperado
* **Empoderamiento jurídico:** Reducir la dependencia de terceros o intermediarios informales para que los adultos mayores conozcan y ejerzan sus derechos con seguridad.
* **Ahorro de tiempo y recursos:** Evitar traslados largos o innecesarios mediante la georreferenciación exacta de dependencias y abogados por zona.
* **Atención oportuna y digna:** Acercar servicios legales confiables a poblaciones históricamente desatendidas, como adultos mayores migrantes y habitantes de comunidades rurales o periféricas.