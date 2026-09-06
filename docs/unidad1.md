# MÓDULO PROFESIONAL: PROYECTO INTERMODULAR (PI)

## SPRINT 1. Definición del reto, gestión de requisitos y herramientas de IA (3 semanas | 3 horas)

---

# SEMANA 1 — SESIÓN 1 (Viernes, 18 de septiembre de 2026 — 1 hora lectiva)
### Bloque: De la idea al reto técnico: Análisis de necesidades, identificación de actores, ODS y uso ético de la Inteligencia Artificial (IA)
* **Distribución horaria:** 20 minutos de marco metodológico y ético + 40 minutos de taller práctico de análisis y backlog.
* **Criterios de Evaluación vinculados:** RA1.c, RA1.d, RA1.e, RA5.a, RA5.c, Anexo I (Bloques 1 y 3 de la Guía Oficial).

---

## PARTE I. SESIÓN TEÓRICA (20 MINUTOS): EL ANÁLISIS DEL RETO Y LA INGENIERÍA DE REQUISITOS

### 1. Caso práctico narrativo: La mesa de proyectos de AzaharTech

Es viernes por la tarde en la sede de **AzaharTech** en Castellón de la Plana. Tras las intensas sesiones de la semana en Programación y Entornos de Desarrollo, la célula de trabajo se reúne para la sesión semanal de **Proyecto Intermodular**: el espacio reservado para la estrategia, la relación con el cliente y la gestión metodológica.

**Laia Claramunt**, supervisora de proyectos, conecta su portátil y muestra en el proyector dos documentos en paralelo: a la izquierda, el análisis del sistema de acceso por QR del **IES El Caminàs** (el caso guía modelado por el docente); a la derecha, el catálogo de la **bolsa de proyectos** donde cada equipo ha elegido su reto singular para el curso.

Laia toma la palabra dirigiéndose a **Alba Torres**, **Pau Ferrer** y al nuevo estudiante:

> *«Durante esta primera semana habéis aprendido a declarar variables en Java y a configurar vuestro entorno en IntelliJ con Git. Esas son las herramientas del artesano. Pero un ingeniero de software no empieza tirando líneas de código al azar; un ingeniero primero **escucha al cliente, analiza el problema y delimita el alcance de la solución**.*
>
> *Si el cliente nos pide un sistema para su negocio y nosotros le entregamos lo que creemos que necesita sin haber analizado a sus usuarios, el proyecto fracasará. Hoy aprenderemos a transformar una idea abstracta en un **reto técnico formal**, analizaremos los diferentes perfiles de usuario que interactuarán con el sistema, vincularemos el proyecto con los **Objetivos de Desarrollo Sostenible (ODS)** y utilizaremos la **Inteligencia Artificial de forma ética y transparente** como copiloto de análisis, registrando cada consulta en nuestro cuaderno de bitácora»*.

---

### 2. Fundamento metodológico: Del problema de negocio a la especificación técnica

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL CICLO DE ANÁLISIS DEL RETO (FASE INICIAL)                    │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Problema Raíz         │ 2. Mapa de Actores          │ 3. Impacto y Sostenibilidad   │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ ¿Qué ineficiencia, coste │ ¿Quiénes son los usuarios   │ ¿Cómo contribuye la solución  │
│ o retraso sufre el       │ primarios, secundarios y    │ a la innovación y a los ODS   │
│ cliente en su día a día? │ administradores del sistema?│ de la Agenda 2030?            │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

#### A. Definición del problema y justificación de la digitalización (RA1.c)
Todo proyecto de software viable responde a una necesidad real no resuelta o deficientemente gestionada:
* **En el caso guía (IES El Caminàs):** El fichaje manual en papel genera aglomeraciones en conserjería, pérdida de tiempo lectivo y retraso en las alertas a las familias. La digitalización aporta inmediatez, trazabilidad y ahorro de papel.
* **En vuestro proyecto propio de la bolsa de proyectos:** Debéis responder con precisión a tres preguntas:
    1. ¿Cuál es la situación actual del cliente (*As-Is*)?
    2. ¿Qué problemas operativos, económicos o de gestión genera esa situación?
    3. ¿Cómo resolverá vuestra aplicación ese problema (*To-Be*)?

#### B. Identificación y mapa de actores (RA1.e)
Un **actor** es cualquier entidad externa (humana o máquina) que interactúa directamente con el software:
1. **Usuarios primarios u operacionales:** Aquellos que utilizan la herramienta para su función principal diaria (*ej. el alumno que valida su QR o el operario que registra una entrada de stock*).
2. **Usuarios administradores o de gestión:** Aquellos que configuran el sistema, dan de alta parámetros y extraen informes (*ej. el equipo directivo o el jefe de almacén*).
3. **Sistemas externos:** Dispositivos periféricos o servicios web con los que la aplicación intercambia datos (*ej. pantallas HDMI, bases de datos externas o lectores ópticos*).

#### C. Vinculación con los Objetivos de Desarrollo Sostenible (ODS - RA1.d)
Siguiendo las directrices del Decreto de Formación Profesional de la Comunitat Valenciana, todo proyecto intermodular debe incorporar la dimensión social y ambiental alineada con los **ODS**:
* **ODS 9 (Industria, Innovación e Infraestructura):** Modernización y digitalización de procesos productivos tradicionales.
* **ODS 12 (Producción y Consumo Responsables):** Eliminación del consumo de papel y optimización de recursos energéticos.
* **ODS 4 (Educación de Calidad) u ODS 8 (Trabajo Decente y Crecimiento Económico):** Mejora de la conciliación, control horario y transparencia laboral.

#### D. Uso ético y profesional de la Inteligencia Artificial (Anexo I, Bloque 1)
En AzaharTech no se prohíbe la Inteligencia Artificial generativa (como ChatGPT, Claude o Copilot); **se exige su uso profesional y crítico**.
* **Uso permitido:** Asistente para estructurar ideas, mejorar la redacción técnica de requisitos, proponer casos límite y contrastar vocabulario técnico.
* **Uso prohibido:** Copiar y pegar ciegamente respuestas generadas sin contrastar su veracidad o delegar en la máquina la toma de decisiones del proyecto.
* **El estándar del Prompt Log (Registro de IA):** Toda aportación de la IA debe documentarse en una tabla indicando la herramienta, la instrucción exacta (*prompt*) introducida y el criterio del estudiante para modificar o aceptar la respuesta.

---

## PARTE II. TALLER PRÁCTICO GUIADO (40 MINUTOS): ESPECIFICACIÓN DEL RETO Y SPRINT BACKLOG 1

### Caso de laboratorio
Laia Claramunt asigna las tareas de la sesión:
> *«Durante los próximos cuarenta minutos, cada uno de vosotros va a crear el espacio oficial de Proyecto Intermodular en su repositorio de GitHub. Redactaréis el **documento formal de análisis del reto de vuestro proyecto propio** incluyendo el registro ético de IA, y crearéis el archivo **`sprint1-backlog.md`** que coordinará vuestras tareas entre Programación, Entornos de Desarrollo y Proyecto Intermodular»*.

---

### Procedimiento técnico paso a paso

#### Paso 1. Estructuración del espacio de Proyecto Intermodular
1. Abre tu proyecto en **IntelliJ IDEA**.
2. Comprueba que dentro de tu carpeta individual (`azahartech/nombreEquipo/nombreEstudiante/`) dispones del directorio **`pi/`**.
3. Dentro de `pi/`, crea dos subcarpetas de trabajo:
    * **`pi/docs/`**: Para memorias técnicas, análisis y diagramas.
    * **`pi/backlog/`**: Para el seguimiento de sprints y tareas.

---

#### Paso 2. Redacción del Documento de Análisis del Reto (`pi/docs/analisis-reto.md`)
1. En `pi/docs/`, crea el archivo `analisis-reto.md`.
2. Redacta el documento aplicando la siguiente plantilla formal adaptada a **tu proyecto elegido de la bolsa de proyectos**:

```markdown
# Documento de Análisis de Necesidades y Definición del Reto
**Consultora:** AzaharTech Software Consulting  
**Proyecto Seleccionado:** [Nombre del Proyecto de la Bolsa de Proyectos]  
**Cliente / Sector:** [Nombre de la Empresa o Sector Profesional]  
**Desarrollador/a:** [Tus Apellidos, Tu Nombre]  
**Fecha:** 18 de septiembre de 2026  
**Versión:** 1.0  

---

## 1. Contexto y Justificación del Problema
### 1.1 Situación actual y problemática detectada
[Describe el problema operativo de tu cliente. Qué procesos manuales lentos, pérdidas económicas o fallos de registro sufre actualmente su organización].

### 1.2 Propuesta de solución y digitalización
[Explica cómo la aplicación de software que vas a desarrollar resolverá el problema, automatizando la captura de datos y ofreciendo información en tiempo real].

### 1.3 Contribución a los Objetivos de Desarrollo Sostenible (ODS)
* **ODS Principal:** [ej. ODS 9: Industria, Innovación e Infraestructura].
* **Justificación:** [Explica en 2 líneas cómo tu software reduce el impacto ambiental, ahorra recursos materiales o moderniza el sector].

---

## 2. Mapa de Actores y Usuarios del Sistema
| Perfil de Usuario | Tipo de Actor | Función principal en la aplicación |
| :--- | :---: | :--- |
| **Operario / Cliente final** | Primario | Introduce los datos de la transacción o evento diario. |
| **Administrador / Gestor** | Secundario | Configura las constantes, supervisa y extrae informes. |
| **Terminal / Hardware** | Externo | Dispositivo que ejecuta o proyecta la salida del sistema. |

---

## 3. Registro Ético de Uso de Inteligencia Artificial (Prompt Log)
| Fecha | Herramienta | Objetivo de la consulta | Prompt introducido | Revisión crítica y ajuste aplicado |
| :---: | :---: | :--- | :--- | :--- |
| 18/09/2026 | ChatGPT / Claude | Estructurar requisitos funcionales | *"Actúa como analista y redacta 3 necesidades de software para..."* | Se adaptaron los requisitos al alcance secuencial del Sprint 1 y se eliminaron funciones innecesarias. |
```

---

#### Paso 3. Creación del Sprint Backlog 1 (`pi/backlog/sprint1-backlog.md`)
1. En la carpeta `pi/backlog/`, crea el archivo `sprint1-backlog.md`.
2. Define la lista de tareas del **Sprint 1 (14 sep – 2 oct)** desglosada por los tres módulos:

```markdown
# Sprint Backlog 1 — [Nombre de Tu Proyecto Propio]
**Periodo:** 14 de septiembre – 2 de octubre de 2026  
**Responsable:** [Tu Nombre]  

## 🎯 Objetivo General del Sprint 1
Construir el incremento base v0.1: definir el análisis técnico del reto, configurar el taller digital con Git/IntelliJ y programar el primer motor de cálculo secuencial en Java.

---

## 📋 Cuadro de Mando de Tareas

### Módulo: Proyecto Intermodular (PI)
- [x] T-PI-01: Redactar análisis de necesidades y mapa de actores (`pi/docs/analisis-reto.md`)
- [x] T-PI-02: Registrar el uso ético de IA (*Prompt Log*)
- [x] T-PI-03: Crear el Sprint Backlog 1 inicial
- [ ] T-PI-04: Elaborar diagrama de bloques funcional y viabilidad técnica (Semana 2)
- [ ] T-PI-05: Consolidar dossier técnico y guion de demo v0.1 (Semana 3)

### Módulo: Entornos de Desarrollo (ED)
- [x] T-ED-01: Instalar y verificar OpenJDK 21 e IntelliJ IDEA (`ed/docs/entorno.png`)
- [x] T-ED-02: Crear estructura corporativa oficial y repositorio en GitHub
- [ ] T-ED-03: Elaborar memoria técnica de marco Scrum (`ed/docs/marco-scrum.md`) (Semana 2)
- [ ] T-ED-04: Auditar limpieza de repositorio y publicar tag `v0.1.0-sprint1` (Semana 3)

### Módulo: Programación (PR)
- [x] T-PR-01: Declarar variables primitivas y lectura con Scanner (`pr/src/Reto1Variables.java`)
- [ ] T-PR-02: Implementar operadores aritméticos, módulo y casting (Semana 2)
- [ ] T-PR-03: Integrar constantes `final` y salida formateada con `printf` (Semana 3)
```

---

#### Paso 4. Confirmación y sincronización en GitHub
1. Abre la terminal integrada de IntelliJ IDEA (`Alt + F12`) o la pestaña **Commit** (`Ctrl + K`).
2. Verifica mediante `git status` que los dos archivos de PI están detectados.
3. Confirma los cambios aplicando el estándar de **Conventional Commits**:
   ```bash
   git add pi/
   git commit -m "docs(pi): definir analisis del reto del proyecto propio y sprint backlog 1"
   git push
   ```
4. Accede a tu repositorio en GitHub desde el navegador y comprueba que la carpeta `pi/docs/` y `pi/backlog/` se visualizan correctamente con su formato Markdown maquetado.

---

### Resumen de la Sesión 1 de Proyecto Intermodular
Al finalizar estos 60 minutos:
* Has transformado la propuesta de la bolsa de proyectos en un **reto de ingeniería formal**.
* Has identificado los **actores clave** y has vinculado el proyecto con los **ODS**.
* Has utilizado la **IA de forma ética, documentada y transparente**.
* Tu repositorio cuenta con el **Sprint Backlog 1** que coordina tu trabajo con Programación y Entornos de Desarrollo.

---
---

# SEMANA 2 — SESIÓN 2 (Viernes, 25 de septiembre de 2026 — 1 hora lectiva)
### Bloque: Arquitectura funcional del sistema: Diagrama de bloques (IPO), estudio de viabilidad técnica y búsqueda de fuentes oficiales
* **Distribución horaria:** 20 minutos de teoría de arquitectura y viabilidad + 40 minutos de taller práctico de modelado.
* **Criterios de Evaluación vinculados:** RA1.e, RA2.e, RA2.f, RA2.g, RA3.b, RA5.c, Anexo I (Bloque 3 de la Guía Oficial).

---

## PARTE I. SESIÓN TEÓRICA (20 MINUTOS): ARQUITECTURA DE BLOQUES Y VIABILIDAD

### 1. Caso práctico narrativo: El plano de la solución en AzaharTech

Es viernes 25 de septiembre. La célula de desarrollo de **AzaharTech** inicia su segunda sesión de Proyecto Intermodular. En la pantalla táctil de la sala, **Laia Claramunt** proyecta un esquema técnico del caso guía: el sistema del **IES El Caminàs**.

El esquema no contiene código, sino tres grandes bloques conectados por líneas de flujo:
1. Bloque de Captura (cámara del móvil del alumno y lector óptico).
2. Bloque de Procesamiento Central (algoritmo en Java que valida la matrícula y calcula tiempos).
3. Bloque de Salida y Notificación (pantalla HDMI del vestíbulo y volcado en log).

Laia se gira hacia el equipo:

> *«En la semana anterior analizamos el problema y los actores. Pero un cliente no puede financiar una idea en el aire: necesita ver el **plano arquitectónico de la solución y tener la certeza de que es técnicamente viable**.*
>
> *Para el IES El Caminàs tuvimos que estudiar previamente si la red WiFi del centro soportaba la concurrencia de escaneos a las ocho de la mañana, qué librerías oficiales de Java utilizaríamos y qué hardware requería el vestíbulo.*
>
> *Hoy cada uno de vosotros va a diseñar el **Diagrama de Bloques Funcional** de su proyecto propio, evaluará su **viabilidad técnica** contrastando fuentes oficiales de información y actualizará el **Sprint Backlog** para afrontar la recta final del sprint»*.

---

### 2. Fundamento metodológico: Arquitectura funcional y contraste de fuentes

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL DIAGRAMA DE BLOQUES FUNCIONAL (IPO)                          │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ BLOQUE DE ENTRADA        │ BLOQUE DE PROCESAMIENTO     │ BLOQUE DE SALIDA              │
│ (Captura de datos)       │ (Lógica de Negocio)         │ (Resultados y Persistencia)   │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ Dispositivos de entrada, │ Módulos Java, cálculos      │ Pantallas de visualización,   │
│ teclado, Scanner,        │ aritméticos, conversiones,  │ consolas de texto, tickets    │
│ sensores o archivos.     │ aplicación de reglas.       │ formateados o logs locales.   │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

#### A. El Diagrama de Bloques Funcional (RA1.e)
Es la representación visual de más alto nivel de un sistema de software. Permite entender de un vistazo cómo fluyen los datos sin necesidad de descender al detalle del código fuente:
* **Entradas:** Qué datos brutos recibe el sistema del exterior (*ej. DNI, lecturas térmicas, unidades demandadas*).
* **Procesamiento:** Qué módulos de software transforman esos datos (*ej. motor de cálculo, cálculo de porcentajes, validadores de tokens*).
* **Salidas:** Qué información útil entrega el sistema al usuario (*ej. pantallas informativas, informes formateados, comprobantes de acceso*).

#### B. Estudio de Viabilidad Técnica (RA2.e, RA2.g)
Evaluar la viabilidad de un proyecto significa certificar que la solución es realizable con los medios tecnológicos disponibles:
1. **Viabilidad de Software:** Compatibilidad de versiones. En nuestro caso: Java OpenJDK 21 LTS como entorno de ejecución universal e IntelliJ IDEA Community como entorno de construcción.
2. **Viabilidad de Hardware:** Requisitos mínimos de memoria RAM (mínimo 4 GB para la JVM), procesador y periféricos necesarios en el cliente.
3. **Gestión de Restricciones Operativas:** Identificar qué tecnologías se aplican en cada sprint (*ej. en el Sprint 1 la persistencia se realiza estrictamente en memoria y consola; las bases de datos relacionales y el modelado avanzado se incorporarán en la Formación en Empresa*).

#### C. Búsqueda y contraste de fuentes técnicas oficiales (Anexo I, Bloque 3)
Un desarrollador profesional no diseña basándose en tutoriales anónimos o respuestas de foros obsoletos. La guía oficial exige:
* **Selección de fuentes primarias:** Documentación oficial de Oracle Java SE 21, estándares IEEE para documentación y especificaciones de la Comunitat Valenciana.
* **Detección de información no contrastada:** Descartar soluciones que empleen librerías no oficiales o versiones obsoletas de Java (como Java 8 o Java 11) que no respeten las buenas prácticas actuales.

---

## PARTE II. TALLER PRÁCTICO GUIADO (40 MINUTOS): MODELADO DE BLOQUES Y VIABILIDAD TÉCNICA

### Procedimiento técnico paso a paso

#### Paso 1. Redacción del Documento de Viabilidad y Arquitectura (`pi/docs/viabilidad-tecnica.md`)
1. Abre tu proyecto en IntelliJ IDEA y navega hasta la carpeta `pi/docs/`.
2. Crea el archivo `viabilidad-tecnica.md`.
3. Redacta el contenido aplicando la plantilla técnica estructurada para **tu proyecto propio**:

```markdown
# Estudio de Viabilidad Técnica y Arquitectura del Sistema
**Consultora:** AzaharTech Software Consulting  
**Proyecto:** [Nombre de Tu Proyecto Propio]  
**Desarrollador/a:** [Tus Apellidos, Tu Nombre]  
**Fecha:** 25 de septiembre de 2026  
**Versión:** 1.0 (Sprint 1)  

---

## 1. Diagrama de Bloques Funcional del Sistema
El sistema se descompone en tres subsistemas funcionales coordinados:

```text
+-----------------------------------------------------------------------+
|                       BLOQUE 1: ENTRADA DE DATOS                      |
|  - Captura interactiva por teclado mediante clase Scanner             |
|  - Parámetros de identificación de cliente y volumen de demanda       |
+-----------------------------------┬-----------------------------------+
                                    |
                                    v
+-----------------------------------------------------------------------+
|                    BLOQUE 2: PROCESAMIENTO Y CÁLCULO                  |
|  - Módulo Java en OpenJDK 21                                          |
|  - Descomposición de unidades mediante división entera y módulo (%)   |
|  - Fórmulas de recargos económicos y casting explícito a decimal      |
+-----------------------------------┬-----------------------------------+
                                    |
                                    v
+-----------------------------------------------------------------------+
|                   BLOQUE 3: SALIDA DE INFORMACIÓN                     |
|  - Consola de usuario formateada mediante System.out.printf()         |
|  - Resumen tabular con columnas de ancho fijo y decimales acotados    |
+-----------------------------------------------------------------------+
```

---

## 2. Estudio de Viabilidad Técnica
* **Entorno de Ejecución:** Java SE 21 (LTS) garantizando portabilidad multiplataforma mediante la JVM.
* **Requisitos Mínimos de Hardware:**
    * Procesador con arquitectura x86_64 o ARM64.
    * Memoria RAM mínima: 2 GB (óptima: 4 GB para entorno de pruebas).
    * Espacio en disco: 500 MB libres para instalación del JDK y logs.
* **Análisis de Restricciones del Sprint 1:** Se prescinde de bases de datos externas en esta fase inicial; el procesamiento se realiza en memoria volátil de forma secuencial y transparente.

---

## 3. Fuentes Técnicas Oficiales Contrastadas
1. **Documentación Oficial de Java SE 21 (Oracle):** Consulta de especificaciones de tipos primitivos y clase Scanner. URL: `https://docs.oracle.com/en/java/javase/21/`
2. **Guía de Estilo Java de Google:** Estándares de nomenclatura *camelCase* y buenas prácticas de ingeniería de software.
```

---

#### Paso 2. Actualización y seguimiento del Sprint Backlog 1 (`pi/backlog/sprint1-backlog.md`)
1. Abre el archivo `sprint1-backlog.md`.
2. Actualiza el estado de las tareas de los tres módulos al cierre de la segunda semana:

```markdown
# Sprint Backlog 1 — [Nombre de Tu Proyecto Propio]
**Estado al cierre de la Semana 2 (25 de septiembre de 2026)**

## 📋 Cuadro de Mando de Tareas

### Módulo: Proyecto Intermodular (PI)
- [x] T-PI-01: Redactar análisis de necesidades y mapa de actores (`pi/docs/analisis-reto.md`)
- [x] T-PI-02: Registrar el uso ético de IA (*Prompt Log*)
- [x] T-PI-03: Crear el Sprint Backlog 1 inicial
- [x] T-PI-04: Elaborar diagrama de bloques funcional y viabilidad técnica (`pi/docs/viabilidad-tecnica.md`)
- [ ] T-PI-05: Consolidar dossier técnico y guion de demo v0.1 (Semana 3)

### Módulo: Entornos de Desarrollo (ED)
- [x] T-ED-01: Instalar y verificar OpenJDK 21 e IntelliJ IDEA (`ed/docs/entorno.png`)
- [x] T-ED-02: Crear estructura corporativa oficial y repositorio en GitHub
- [x] T-ED-03: Elaborar memoria técnica de marco Scrum (`ed/docs/marco-scrum.md`)
- [ ] T-ED-04: Auditar limpieza de repositorio y publicar tag `v0.1.0-sprint1` (Semana 3)

### Módulo: Programación (PR)
- [x] T-PR-01: Declarar variables primitivas y lectura con Scanner (`pr/src/Reto1Variables.java`)
- [x] T-PR-02: Implementar operadores aritméticos, módulo y casting (`pr/src/Reto1Calculo.java`)
- [ ] T-PR-03: Integrar constantes `final` y salida formateada con `printf` (Semana 3)
```

---

#### Paso 3. Confirmación y sincronización en GitHub
1. Abre el panel **Commit** en IntelliJ IDEA (`Ctrl + K`).
2. Comprueba que aparecen seleccionados `pi/docs/viabilidad-tecnica.md` y `pi/backlog/sprint1-backlog.md`.
3. Escribe el mensaje siguiendo el estándar de **Conventional Commits**:
   ```text
   docs(pi): elaborar estudio de viabilidad tecnica y actualizar sprint backlog 1
   ```
4. Haz clic en **Commit and Push** y verifica en GitHub que ambos archivos quedan registrados.

---

### Resumen de la Sesión 2 de Proyecto Intermodular
Al término de estos 60 minutos:
* Tu proyecto propio cuenta con una **arquitectura en bloques funcional bien definida**.
* Has certificado la **viabilidad técnica y los requisitos de hardware y software**.
* Has referenciado **fuentes técnicas oficiales** según exige el Anexo I de la normativa.
* El **Sprint Backlog 1** refleja un avance ordenado y sincronizado con Programación y Entornos de Desarrollo.

---
---

# SEMANA 3 — SESIÓN 3 (Viernes, 2 de octubre de 2026 — 1 hora lectiva)
### Bloque: Consolidación del Dossier Técnico, cierre del Sprint Backlog 1 y preparación de la Sprint Review (Demo técnica v0.1)
* **Distribución horaria:** 20 minutos de teoría de comunicación y defensa oral + 40 minutos de consolidación y ensayo.
* **Criterios de Evaluación vinculados:** RA1.a-e, RA5.a, RA5.b, RA5.c, RA5.d, Anexo I (Bloques 2 y 4 de la Guía Oficial).

---

## PARTE I. SESIÓN TEÓRICA (20 MINUTOS): ASPECTOS FORMALES Y TÉCNICAS DE COMUNICACIÓN ORAL

### 1. Caso práctico narrativo: El ensayo de la Sprint Review en AzaharTech

Es viernes 2 de octubre. Hoy concluyen las tres semanas del **Sprint 1**. La sala de demostraciones de **AzaharTech** está preparada para la revisión oficial del primer incremento de software.

**Laia Claramunt** reúne a la célula de desarrollo:

> *«Equipo, en Programación tenéis listo el programa secuencial con cálculos de precisión y formateo `printf`. En Entornos de Desarrollo habéis sellado el repositorio con la etiqueta de versión `v0.1.0-sprint1`. El software está terminado.*
>
> *Pero en la vida profesional, un excelente código no se defiende solo. El cliente del IES El Caminàs y el tribunal evaluador no van a leerse doscientas líneas de código; van a juzgar nuestra capacidad para **documentar el producto con normas de estilo impecables y comunicar su valor en una demostración en vivo de tres minutos**.*
>
> *Hoy consolidaremos el **Dossier Técnico formal del Sprint 1**, cerraremos el **Sprint Backlog al 100 %** y entrenaremos la estructura de la **Sprint Review (Demo v0.1)**. Un ingeniero de software debe saber hablar con tanta precisión como programa»*.

---

### 2. Fundamento metodológico: Calidad documental y comunicación técnica

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        ESTRUCTURA DE LA DEMO TÉCNICA (THE 3-MINUTE DEMO)               │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ MINUTO 1: CONTEXTO       │ MINUTO 2: DEMO EN VIVO      │ MINUTO 3: ARQUITECTURA        │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ • ¿Quién es el cliente?  │ • Ejecución real en consola │ • Estructura en bloques.      │
│ • ¿Qué problema crítico  │   del código Java.          │ • Herramientas empleadas.     │
│   resuelve el software?  │ • Comprobación de cálculos. │ • Próximo hito (Sprint 2).    │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

#### A. Aspectos formales y estructura del Dossier Técnico (Anexo I, Bloque 2)
La documentación que se entrega a un cliente o a un comité evaluador debe reflejar la máxima pulcritud:
1. **Estructura lógica completa:** Portada corporativa, índice de contenidos, cuerpo técnico organizado por apartados numerados y bibliografía de fuentes.
2. **Normas de estilo:** Lenguaje técnico impersonal (*«se implementa»*, *«el sistema calcula»*), ausencia total de faltas ortográficas y jerarquía visual limpia.
3. **Trazabilidad de herramientas TIC e IA:** Registro transparente de cómo se ha empleado la tecnología para documentar el proyecto.

#### B. Técnicas de comunicación oral y defensa ante el cliente (Anexo I, Bloque 4)
Para defender con éxito el primer incremento de software ante el profesorado o el cliente:
* **Estructura en 3 minutos (*The 3-Minute Demo*):**
    * *Minuto 1 (Problema y Propuesta):* Presentar al cliente, justificar la necesidad y explicar el alcance del Sprint 1.
    * *Minuto 2 (Software funcionando):* Compartir pantalla, ejecutar la clase `Reto1Completo.java` en IntelliJ, introducir datos de prueba y mostrar el informe de salida generado con `printf`.
    * *Minuto 3 (Ingeniería y Conclusión):* Mostrar el repositorio en GitHub, verificar el tag `v0.1.0-sprint1` y resumir los objetivos alcanzados.
* **Comunicación no verbal y seguridad:** Hablar con voz firme y clara, mantener contacto visual con la audiencia, evitar leer diapositivas de forma monótona y demostrar dominio de los términos técnicos en inglés (*commit*, *stage*, *casting*, *build*).

---

## PARTE II. TALLER PRÁCTICO GUIADO (40 MINUTOS): CONSOLIDACIÓN DOCUMENTAL Y ENSAYO DE LA DEMO

### Procedimiento técnico paso a paso

#### Paso 1. Consolidación del Dossier Técnico del Sprint 1 (`pi/docs/dossier-tecnico-sprint1.md`)
1. En la carpeta `pi/docs/`, crea el archivo consolidado `dossier-tecnico-sprint1.md`.
2. Ensambla los apartados trabajados durante las tres semanas en un único documento maestro para **tu proyecto propio**:

```markdown
# Dossier Técnico de Proyecto Intermodular — Sprint 1 (Incremento v0.1)
**Consultora:** AzaharTech Software Consulting  
**Proyecto:** [Nombre de Tu Proyecto Propio]  
**Cliente:** [Nombre del Cliente de la Bolsa de Proyectos]  
**Desarrollador/a:** [Tus Apellidos, Tu Nombre]  
**Célula / Equipo:** [Nombre de tu equipo asignado]  
**Fecha de Entrega:** 2 de octubre de 2026  
**Versión Tag:** v0.1.0-sprint1  

---

## 1. Contexto, Necesidad y Objetivos
[Resumen del problema del cliente y justificación de la digitalización de la solución].
* **Alineación con ODS:** [Indica el ODS seleccionado y su impacto en sostenibilidad].

---

## 2. Mapa de Actores del Sistema
[Tabla completa de perfiles de usuario: operarios, administradores y sistemas externos].

---

## 3. Arquitectura y Diagrama de Bloques Funcional
[Esquema funcional de 3 bloques: Entrada de datos por Scanner -> Procesamiento aritmético y módulo -> Salida estructurada con printf].

---

## 4. Viabilidad Técnica y Recursos
* **Tecnología base:** Java SE 21 LTS e IntelliJ IDEA Community Edition.
* **Control de versiones:** Git & GitHub bajo estructura oficial corporativa.
* **Requisitos mínimos:** 2 GB RAM, procesador x86_64/ARM64.

---

## 5. Registro Ético de Uso de Inteligencia Artificial (Prompt Log)
[Tabla con las consultas realizadas a herramientas de IA, prompts exactos y revisiones críticas aplicadas por el estudiante].

---

## 6. Referencias Técnicas Oficiales
1. Oracle Java Documentation: `https://docs.oracle.com/en/java/javase/21/`
2. Guía Oficial de Programación del Módulo Proyecto Intermodular (GVA).
```

---

#### Paso 2. Cierre definitivo del Sprint Backlog 1 al 100 % (`pi/backlog/sprint1-backlog.md`)
1. Abre el archivo `sprint1-backlog.md`.
2. Marca **absolutamente todas las tareas del Sprint 1 con el check `[x]`**:

```markdown
# Sprint Backlog 1 — [Nombre de Tu Proyecto Propio]
**Estado Final: 100% COMPLETADO Y SELLADO (2 de octubre de 2026)**

## 📋 Verificación Final de Tareas del Incremento v0.1

### Módulo: Proyecto Intermodular (PI)
- [x] T-PI-01: Redactar análisis de necesidades y mapa de actores (`pi/docs/analisis-reto.md`)
- [x] T-PI-02: Registrar el uso ético de IA (*Prompt Log*)
- [x] T-PI-03: Crear el Sprint Backlog 1 inicial
- [x] T-PI-04: Elaborar diagrama de bloques funcional y viabilidad técnica (`pi/docs/viabilidad-tecnica.md`)
- [x] T-PI-05: Consolidar dossier técnico y guion de demo v0.1 (`pi/docs/dossier-tecnico-sprint1.md`)

### Módulo: Entornos de Desarrollo (ED)
- [x] T-ED-01: Instalar y verificar OpenJDK 21 e IntelliJ IDEA (`ed/docs/entorno.png`)
- [x] T-ED-02: Crear estructura corporativa oficial y repositorio en GitHub
- [x] T-ED-03: Elaborar memoria técnica de marco Scrum (`ed/docs/marco-scrum.md`)
- [x] T-ED-04: Auditar limpieza de repositorio y publicar tag `v0.1.0-sprint1`

### Módulo: Programación (PR)
- [x] T-PR-01: Declarar variables primitivas y lectura con Scanner (`pr/src/Reto1Variables.java`)
- [x] T-PR-02: Implementar operadores aritméticos, módulo y casting (`pr/src/Reto1Calculo.java`)
- [x] T-PR-03: Integrar constantes `final` y salida formateada con `printf` (`pr/src/Reto1Completo.java`)
```

---

#### Paso 3. Preparación del Guion de la Demo Técnica (3 minutos)
Redacta al final de tu dossier técnico una ficha con el minutaje exacto de tu intervención ante el tribunal:

```markdown
### Guion de Exposición: Sprint Review v0.1 (3 Minutos)
* **00:00 - 00:45 (Presentación y Reto):** Saludo formal, nombre del proyecto, cliente de la bolsa de proyectos y problema crítico que resolvemos.
* **00:45 - 02:15 (Demostración Práctica en Vivo):** Ejecución de `Reto1Completo.java` en IntelliJ IDEA, introducción de datos reales por consola y explicación de los resultados calculados con `printf`.
* **02:15 - 03:00 (Ingeniería y Repositorio):** Muestra de GitHub, confirmación del tag `v0.1.0-sprint1` y mención al objetivo del Sprint 2 (uso de objetos estándar y estructura Maven).
```

---

#### Paso 4. Commit final y sincronización en GitHub
1. Abre la terminal de IntelliJ (`Alt + F12`) o el panel **Commit** (`Ctrl + K`).
2. Comprueba mediante `git status` que los archivos de `pi/` están listos.
3. Confirma los cambios aplicando el estándar convencional:
   ```bash
   git add pi/
   git commit -m "docs(pi): consolidar dossier tecnico final del sprint 1 y cerrar backlog al 100 por ciento"
   git push
   ```
4. Accede a tu repositorio en GitHub y comprueba que la carpeta `pi/` luce con todos sus documentos accesibles.

---

### Resumen del Sprint 1 de Proyecto Intermodular completado
Al concluir estas 3 sesiones de los viernes (3 horas lectivas en total):
1. Has transformado la propuesta de tu proyecto propio en una **especificación de ingeniería formal**, analizando actores y alineándola con los **ODS**.
2. Has definido la **arquitectura funcional en bloques** y has contrastado **fuentes técnicas oficiales**.
3. Has utilizado la **Inteligencia Artificial con rigor ético y transparencia** mediante el *Prompt Log*.
4. Cuentas con un **Dossier Técnico consolidado**, el **Sprint Backlog 1 al 100 %** y un guion ensayado para defender tu software, dejando el módulo plenamente preparado para la evaluación formativa mediante la lista de cotejo de Proyecto Intermodular.