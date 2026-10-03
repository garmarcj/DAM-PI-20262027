# Sprint 2. Especificación de requisitos del sistema

---

## Semana 4. De la necesidad al requisito: catalogación de requisitos funcionales, no funcionales y apertura del Sprint Backlog 2

---

### Día 4 - 1 sesión

#### Teoría. De la necesidad al catálogo de requisitos del sistema

#### 1. Caso guía en AzaharTech

Es viernes por la tarde en la sede de **AzaharTech** en Castellón de la Plana. Tras haber cerrado con éxito el Sprint 1 y haber congelado la primera entrega en GitHub, el equipo arranca el **Sprint 2**.

En la sala de reuniones, **Laia Claramunt** proyecta un nuevo documento en la pantalla. A su lado, **Alba Torres** revisa las especificaciones del entorno Maven y **Pau Ferrer** tiene abierto el esquema del vestíbulo del **IES El Caminàs**.

Laia toma la palabra dirigiéndose al equipo de trabajo:

> *«En el Sprint 1 definimos el problema global, identificamos a los actores y demostramos que la lógica base era viable. Pero un cliente no puede firmar un contrato sobre intenciones generales; necesita saber con exactitud matemática **qué hará y qué no hará el software**.*
>
> *Si el equipo directivo del IES El Caminàs nos dice 'queremos que el sistema sea rápido y seguro', esa frase no le sirve a un programador. ¿Qué significa 'rápido'? ¿Menos de un segundo? ¿Menos de diez? ¿Qué significa 'seguro'? ¿Qué datos valida?*
>
> *Hoy aprenderemos a transformar las necesidades del cliente en un **Catálogo Formal de Requisitos del Sistema**. Aprenderemos a distinguir los **Requisitos Funcionales (RF)** de los **Requisitos No Funcionales (RNF)**, contrastaremos la documentación técnica oficial para no basarnos en suposiciones y abriremos el **Sprint Backlog 2** que guiará nuestro trabajo durante las próximas tres semanas»*.

---

#### 2. La ingeniería de requisitos en el desarrollo de software

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL PUENTE ENTRE EL CLIENTE Y EL CÓDIGO                          │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Necesidad del Cliente │ 2. Requisito Funcional (RF) │ 3. Requisito No Funcional     │
│    (Lenguaje natural)    │    (¿Qué hace el sistema?)  │    (¿Bajo qué restricciones?) │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ "Queremos que los chicos │ El sistema generará un      │ La respuesta de validación    │
│ fichen rápido al entrar" │ código de acceso único con  │ en pantalla debe realizarse   │
│                          │ el DNI y la marca de tiempo.│ en un tiempo inferior a 1,5 s.│
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

##### A. Requisitos Funcionales frente a Requisitos No Funcionales
Para que el equipo de desarrollo pueda construir el software sin ambigüedades, los requisitos se dividen en dos categorías complementarias:

* **Requisitos Funcionales (RF).** Describen los servicios, comportamientos y funciones operativas que debe ejecutar el software ante determinadas entradas. Responden a la pregunta: *¿Qué hace el sistema?*
    * *En el caso guía (IES El Caminàs):*
        * **RF-01.** El sistema debe capturar el identificador del alumno y los minutos lectivos programados.
        * **RF-02.** El sistema debe componer un código de verificación que una el prefijo del centro, el DNI y el número de terminal.
* **Requisitos No Funcionales (RNF).** Definen las restricciones técnicas, propiedades de calidad, rendimiento o normativas que limitan la solución. Responden a la pregunta: *¿Bajo qué condiciones o restricciones debe operar?*
    * *En el caso guía (IES El Caminàs):*
        * **RNF-01 (Tecnología).** La aplicación debe ejecutarse sobre la Máquina Virtual de Java utilizando OpenJDK 21 LTS.
        * **RNF-02 (Usabilidad/Presentación).** La salida de datos por consola debe estar estructurada de forma tabular con decimales acotados.
        * **RNF-03 (Mantenibilidad).** El código debe estructurarse mediante proyectos gestionados con Apache Maven y control de dependencias.

##### B. Reglas de redacción de requisitos profesionales
Un requisito técnico mal redactado propaga errores en cascada hacia las fases de diseño y pruebas. En AzaharTech aplicamos la regla **SMART**:
1. **Identificador unívoco.** Todo requisito comienza con un código (`RF-01`, `RF-02`, `RNF-01`).
2. **Sin ambigüedades.** Se evitan términos subjetivos como *«fácil»*, *«rápido»*, *«eficiente»* o *«moderno»*. Se utilizan verbos operativos (*«El sistema calculará...»*, *«El sistema almacenará...»*).
3. **Verificable.** Debe ser posible diseñar una prueba técnica objetiva que demuestre si el requisito se cumple o no.

##### C. Búsqueda y contraste de fuentes técnicas oficiales
Para especificar los requisitos de un proyecto no podemos recurrir a foros informales, blogs desactualizados o código no mantenido:
* **Fuentes primarias y oficiales.** Se consultan las especificaciones oficiales de Oracle para Java SE 21, la documentación de la Apache Software Foundation para Maven y las guías de estándares de la industria (IEEE 830 / ISO 25010).
* **Detección de información no contrastada.** Antes de dar por válido un requisito o librería externa, se verifica su licencia, su mantenimiento activo y su compatibilidad con la JVM.

##### D. El uso ético de la Inteligencia Artificial como asistente para documentar requisitos
La IA generativa se utiliza como asistente para desglosar requisitos y anticipar casos límite que el analista haya podido pasar por alto:
* **Uso correcto.** Pedir a la IA que revise una lista inicial de requisitos en busca de ambigüedades o incoherencias.
* **El Prompt Log del Sprint 2.** Cada consulta debe quedar documentada en la memoria, detallando qué aportación de la IA se ha aceptado y qué partes se han corregido para adaptarse a la realidad técnica del proyecto.

---

#### Laboratorio práctico guiado. Catálogo de requisitos y Sprint Backlog 2

Laia Claramunt asigna las tareas de la sesión:
> *«Durante los próximos treinta minutos, cada uno de vosotros abrirá el archivo de requisitos de su proyecto propio de la bolsa de proyectos. Definiréis al menos **cuatro Requisitos Funcionales** y **dos Requisitos No Funcionales**, contrastaréis las fuentes oficiales y crearéis el archivo **`sprint2-backlog.md`** que coordinará las tres semanas que tenemos por delante»*.

---

##### Paso 1. Creación del archivo de catálogo de requisitos (`pi/docs/requisitos-sistema.md`)
1. Abre tu proyecto en **IntelliJ IDEA**.
2. Dentro de tu carpeta `azahartech/nombre-equipo/apellidos-nombre/pi/docs/`, crea el archivo `requisitos-sistema.md`.
3. Redacta el catálogo aplicando la siguiente plantilla formal adaptada a **tu proyecto elegido de la bolsa de proyectos**:

```markdown
# Catálogo de requisitos del sistema y fuentes técnicas
**Consultora:** AzaharTech Software Consulting  
**Proyecto Seleccionado:** [nombre de tu proyecto de la bolsa de proyectos]  
**Cliente / Sector:** [nombre de la empresa o sector profesional]  
**Desarrollador/a:** [tus apellidos, tu nombre]  
**Fecha:** 9 de octubre de 2026  
**Versión:** 1.0 (Sprint 2)  

---

## 1. Alcance y objetivos técnicos del Sprint 2
El objetivo de esta fase es estructurar la lógica del software mediante el uso de objetos estándar y clases predefinidas de Java, gestionando la construcción mediante Apache Maven y definiendo con exactitud el comportamiento esperado del sistema.

---

## 2. Catálogo de Requisitos Funcionales (RF)
| Código | Nombre del Requisito | Descripción técnica obligatoria | Prioridad |
| :---: | :--- | :--- | :---: |
| **RF-01** | Captura de parámetros base | El sistema solicitará interactivamente los identificadores y valores iniciales de la operación del cliente. | Alta |
| **RF-02** | Procesamiento de objetos | El sistema empleará clases predefinidas del lenguaje (Scanner, String, Math) para transformar los datos de entrada. | Alta |
| **RF-03** | Generación de identificador | El sistema compondrá un identificador o código alfanumérico combinando prefijos fijos y marcas de transacción. | Media |
| **RF-04** | Resumen estructurado | El sistema emitirá un informe de resultados formateado sin pérdida de precisión numérica. | Media |

---

## 3. Catálogo de Requisitos No Funcionales (RNF)
| Código | Categoría | Restricción técnica o estándar | Verificación |
| :---: | :--- | :--- | :--- |
| **RNF-01** | Entorno y Plataforma | El software debe compilar y ejecutarse bajo OpenJDK 21 LTS sin librerías externas no estándar. | Inspección de compilación |
| **RNF-02** | Gestión de Proyecto | La estructura de carpetas y dependencias debe regirse bajo el estándar de Apache Maven con su archivo `pom.xml`. | Archivo de configuración |
| **RNF-03** | Calidad de Código | Nombres de variables en camelCase, constantes en UPPER_SNAKE_CASE y código autoformateado. | Revisión de estilo |

---

## 4. Fuentes técnicas oficiales contrastadas
1. **Oracle Java SE 21 Specification:** Documentación de la API estándar para clases del paquete `java.lang` y `java.util`. URL: `https://docs.oracle.com/en/java/javase/21/`
2. **Apache Maven Project Standard Directory Layout:** Especificación oficial de la jerarquía de carpetas en proyectos de software. URL: `https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html`

---

## 5. Registro ético de uso de Inteligencia Artificial (Prompt Log)
| Fecha | Herramienta | Objetivo de la consulta | Prompt introducido | Revisión crítica y ajuste aplicado |
| :---: | :---: | :--- | :--- | :--- |
| 09/10/2026 | ChatGPT / Claude | Redactar requisitos no funcionales | *"Actúa como analista y redacta 2 requisitos no funcionales SMART para..."* | Se adaptaron las métricas de rendimiento y se eliminaron peticiones de bases de datos externas para respetar el Sprint 2. |
```

---

##### Paso 2. Creación del Sprint Backlog 2 (`pi/backlog/sprint2-backlog.md`)
1. En la carpeta `pi/backlog/`, crea el archivo `sprint2-backlog.md`.
2. Define la lista de tareas del **Sprint 2 (5 oct – 23 oct)** desglosada para los tres módulos:

```markdown
# Sprint Backlog 2 — [nombre de tu proyecto]
**Periodo:** 5 de octubre – 23 de octubre de 2026  
**Responsable:** [tu nombre]  

## Objetivo general del Sprint 2
Construir el incremento v0.2: formalizar el catálogo de requisitos del sistema, estructurar el proyecto con Apache Maven en Entornos de Desarrollo y aplicar clases y objetos predefinidos en Programación.

---

## Tareas

### Módulo: Proyecto Intermodular (PI)
- [ ] T-PI-06: Redactar el catálogo de requisitos funcionales y no funcionales (`pi/docs/requisitos-sistema.md`)
- [ ] T-PI-07: Contrastar fuentes técnicas oficiales y registrar el *Prompt Log*
- [ ] T-PI-08: Modelar el diagrama de bloques funcional en Draw.io (Semana 5)
- [ ] T-PI-09: Actualizar el avance y planificar el seguimiento del sprint (Semana 6)

### Módulo: Entornos de Desarrollo (ED)
- [ ] T-ED-05: Comprender el ciclo de compilación a Bytecode y la virtualización en la JVM
- [ ] T-ED-06: Crear y configurar la estructura de proyecto con Apache Maven (`pom.xml`)
- [ ] T-ED-07: Configurar y verificar el archivo `.gitignore` para exclusiones de compilación de Maven (`target/`)

### Módulo: Programación (PR)
- [ ] T-PR-04: Instanciar y utilizar objetos de clases predefinidas (`Scanner`, `String`, `Math`, `Random`)
- [ ] T-PR-05: Programar llamadas a métodos estáticos y métodos de instancia pasando parámetros
- [ ] T-PR-06: Integrar los cálculos y generación de cadenas en el código guía del proyecto propio
```

---

##### Paso 3. (Únicamente si los estudiantes ya lo han visto en ED) Confirmación y sincronización en GitHub
1. Realiza el commit convencional y push:
   ```bash
   git add pi/
   git commit -m "docs(pi): definir catalogo de requisitos del sistema y abrir sprint backlog 2"
   git push
   ```
2. Accede a tu repositorio en GitHub desde el navegador y comprueba que los archivos `requisitos-sistema.md` y `sprint2-backlog.md` se visualizan correctamente con su formato Markdown maquetado.

---

## Semana 5. Arquitectura del software: modelado visual en Draw.io, tratamiento de imágenes técnicas y previsión de recursos

---

### Día 5 - 1 sesión

#### Teoría. Del requisito a la arquitectura visual: diagramas de bloques funcionales y estimación de recursos

#### 1. Caso guía en AzaharTech

Es viernes 16 de octubre por la tarde en la sede de **AzaharTech** en Castellón de la Plana. El equipo de trabajo se reúne para la segunda sesión del Sprint 2.

En la pantalla digital de la sala, **Laia Claramunt** proyecta el catálogo de requisitos que el equipo aprobó la semana anterior. A su lado, **Alba Torres** tiene abierta en su portátil la herramienta **Draw.io**, donde ha transformado los requisitos del **IES El Caminàs** en un esquema visual nítido y estructurado:

```text
+-----------------------+      +--------------------------+      +-----------------------+
|  CAPTURA Y TERMINAL   | ===> |   LÓGICA CENTRAL JAVA    | ===> |  VISUALIZACIÓN Y LOG  |
|  - Lector móvil       |      |   - Paquete java.lang    |      |  - Pantalla vestíbulo |
|  - Escáner de teclado |      |   - Clases Math y String |      |  - Consola formateada |
+-----------------------+      +--------------------------+      +-----------------------+
```

Laia toma la palabra dirigiéndose a **Pau Ferrer** y al estudiante:

> *«En la semana anterior redactamos los Requisitos Funcionales y No Funcionales. Pero cuando un cliente o un comité técnico revisa una memoria, enfrentarse a páginas de texto denso sin apoyo gráfico dificulta entender cómo encajan las piezas del sistema.*
>
> *Un ingeniero de software debe saber traducir las especificaciones escritas a **modelos visuales de arquitectura**. Para el IES El Caminàs, este diagrama de bloques permite que el jefe de estudios entienda exactamente por dónde viajan los datos y qué módulos intervienen.*
>
> *Hoy aprenderemos a utilizar una herramienta estándar de diagramación técnica (**Draw.io / diagrams.net**), aplicaremos el **tratamiento e inserción formal de imágenes técnicas** en nuestra documentación Markdown y cuantificaremos la **previsión de recursos materiales y humanos** que exige nuestro proyecto»*.

---

#### 2. Modelado de arquitectura y tratamiento de imágenes técnicas en ingeniería

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        DEL REQUISITO AL MODELO VISUAL (IPO)                            │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Subsistema de Entrada │ 2. Subsistema de Proceso    │ 3. Subsistema de Salida       │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ Qué componentes reciben  │ Qué clases, métodos y       │ Qué dispositivos o archivos   │
│ los datos del exterior   │ algoritmos transforman      │ reciben la información        │
│ (dispositivos, teclado). │ los datos en memoria.       │ procesada final.              │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

##### A. El Diagrama de Bloques Funcional en la ingeniería del software
El Diagrama de Bloques Funcional es una técnica de modelado de alto nivel que representa la arquitectura de un sistema dividiéndolo en bloques funcionales interconectados:
* **Cajas negras funcionales.** Cada bloque representa un subsistema con una responsabilidad única y bien delimitada (captura, procesamiento matemático, formateo).
* **Flechas de flujo.** Indican la dirección en la que viajan los datos y qué tipo de información se transmite entre subsistemas.
* **Independencia de implementación.** El diagrama muestra *cómo colaboran las partes*, permitiendo que cualquier desarrollador entienda el flujo antes de inspeccionar el código Java o la estructura de Maven.

##### B. Herramientas TIC para diagramación técnica: Draw.io (diagrams.net)
Ya no dibujaremos esquemas de ingeniería a mano alzada ni con herramientas de retoque fotográfico genéricas:
* **Draw.io (diagrams.net).** Es una herramienta estándar, libre y multiplataforma especializada en diagramación técnica.
* Permite alinear elementos con rejilla milimétrica, utilizar conectores ortogonales inteligentes y exportar esquemas en formatos vectoriales o de alta resolución listos para documentación técnica.

##### C. Tratamiento formal de imágenes técnicas en Markdown
Una memoria técnica profesional no puede incrustar capturas borrosas o con fondos descuadrados. Al incorporar diagramas a la documentación se deben respetar tres normas de calidad:
1. **Exportación optimizada.** Las imágenes deben exportarse en formato **PNG** (con fondo transparente o blanco nítido) o **SVG** (vectorial escalable), recortando los márgenes sobrantes (*crop*).
2. **Rutas relativas estrictas.** En Markdown, las imágenes deben guardarse en una subcarpeta dedicada (`pi/docs/img/`) y enlazarse mediante rutas relativas (`![Descripción](img/diagrama.png)`), garantizando que se visualicen correctamente tanto en local como en GitHub.
3. **Pie de figura numerado.** Toda imagen técnica debe ir acompañada de un pie explicativo numerado (*«Figura 1. Diagrama de bloques funcional de la arquitectura del sistema»*).

##### D. Previsión y justificación de recursos
Un proyecto de software viable exige cuantificar con rigor los recursos necesarios para su ejecución:
* **Recursos humanos.** Estimación de horas de trabajo por desarrollador y asignación de responsabilidades.
* **Recursos hardware.** Equipamiento físico requerido tanto para el desarrollo (puestos de trabajo con 8 GB de RAM) como para el despliegue en el cliente (pantallas, servidores, terminales de red).
* **Recursos software.** Licencias y herramientas necesarias (OpenJDK 21 LTS, IntelliJ IDEA Community, Git, GitHub y librerías del ecosistema Maven).

---

#### Laboratorio práctico guiado. Modelado visual en Draw.io y actualización del Sprint Backlog 2

Laia Claramunt asigna las tareas de la sesión:
> *«Durante los próximos minutos, cada uno de vosotros abrirá Draw.io en su navegador y diseñará el **Diagrama de Bloques Funcional de su proyecto de la bolsa de proyectos**. Exportaréis la imagen a vuestra carpeta de documentación, redactaréis la memoria técnica de arquitectura y recursos (**`arquitectura-recursos.md`**) y actualizaréis el avance semanal en vuestro **Sprint Backlog 2**»*.

---

##### Paso 1. Diseño y exportación del Diagrama de Bloques en Draw.io
1. Abre tu navegador web y accede a [app.diagrams.net](https://app.diagrams.net/).
2. Selecciona **Crear nuevo diagrama** (Diagrama en blanco).
3. Modela la arquitectura funcional de tu proyecto propio siguiendo el patrón de tres subsistemas:
    * **Bloque 1 (Entrada de Datos).** Dibuja los componentes que capturan la información de tu cliente (por ejempo, teclado de terminal, escáner, sensores o parámetros).
    * **Bloque 2 (Procesamiento Lógico Java).** Dibuja el núcleo de la aplicación indicando las clases estándar que intervienen (`Scanner`, `String`, `Math`).
    * **Bloque 3 (Salida de Resultados).** Dibuja los soportes donde se muestra o registra la información procesada (consola formateada, pantalla del usuario, comprobante de operación).
4. Conecta los bloques mediante flechas de flujo señalando qué dato viaja entre ellos.
5. Ajusta el diseño: aplica colores sobrios corporativos, textos nítidos y comprueba que la ortografía sea correcta.
6. Exporta el diagrama:
    * Menú superior: **Archivo -> Exportar como -> PNG...**
    * En las opciones, marca la casilla **Recortar** (*Crop*) para eliminar espacios en blanco sobrantes alrededor del diagrama.
    * Guarda el archivo con el nombre: `diagrama-bloques.png`.

---

##### Paso 2. Integración de la imagen y redacción técnica (`pi/docs/arquitectura-recursos.md`)
1. En tu proyecto de IntelliJ, crea la carpeta `img/` dentro de `pi/docs/` si no existe: `azahartech/nombre-equipo/apellidos-nombre/pi/docs/img/`.
2. Mueve el archivo `diagrama-bloques.png` dentro de `pi/docs/img/`.
3. Dentro de `pi/docs/`, crea el archivo `arquitectura-recursos.md`.
4. Redacta el documento aplicando la siguiente plantilla formal adaptada a **tu proyecto propio**:

```markdown
# Arquitectura funcional del sistema y previsión de recursos
**Consultora:** AzaharTech Software Consulting  
**Proyecto Seleccionado:** [nombre de tu proyecto de la bolsa de proyectos]  
**Desarrollador/a:** [tus apellidos, tu nombre]  
**Fecha:** 16 de octubre de 2026  
**Versión:** 1.0 (Sprint 2)  

---

## 1. Diagrama de Bloques Funcional de la Arquitectura
El siguiente esquema técnico modela visualmente el flujo de información y la descomposición en subsistemas de la solución:

![Diagrama de Bloques Funcional](img/diagrama-bloques.png)
*Figura 1. Modelo de arquitectura funcional Entrada-Procesamiento-Salida (IPO).*

---

## 2. Descripción de los Subsistemas
* **Subsistema de Entrada (Captura).** [Describe qué componentes capturan los datos de tu cliente y mediante qué mecanismos].
* **Subsistema de Procesamiento (Lógica Java).** [Explica cómo las clases Java y las operaciones matemáticas transforman los datos en memoria].
* **Subsistema de Salida (Presentación).** [Describe el formato y soporte final donde se presentan los resultados al usuario].

---

## 3. Previsión de Recursos Materiales y Humanos
| Categoría de Recurso | Descripción del Elemento | Justificación Técnica en el Proyecto |
| :--- | :--- | :--- |
| **Recursos Humanos** | Desarrollador/a junior (34 h lectivas) | Análisis, documentación en PI, codificación en PR y control en ED. |
| **Hardware de Desarrollo** | PC con procesador x86_64 y 8 GB RAM | Entorno de compilación local y ejecución fluida de IntelliJ IDEA. |
| **Hardware de Despliegue** | Terminal de cliente / Pantalla operativa | Soporte físico para la visualización del software en producción. |
| **Software de Base** | OpenJDK 21 LTS | Entorno de ejecución estándar multiplataforma mediante la JVM. |
| **Herramientas de Gestión** | Apache Maven 3.9+ / Git & GitHub | Automatización de construcción y control de versiones distribuido. |
```

---

##### Paso 3. Actualización del estado del Sprint Backlog 2 (`pi/backlog/sprint2-backlog.md`)
Abre tu archivo `sprint2-backlog.md` y actualiza el estado de las tareas de los tres módulos al cierre de la segunda semana del sprint:

```markdown
# Sprint Backlog 2 — [nombre de tu proyecto]
**Estado al cierre de la Semana 5 (16 de octubre de 2026)**

## Tareas

### Módulo: Proyecto Intermodular (PI)
- [x] T-PI-06: Redactar el catálogo de requisitos funcionales y no funcionales (`pi/docs/requisitos-sistema.md`)
- [x] T-PI-07: Contrastar fuentes técnicas oficiales y registrar el *Prompt Log*
- [x] T-PI-08: Modelar el diagrama de bloques funcional en Draw.io (`pi/docs/arquitectura-recursos.md`)
- [ ] T-PI-09: Consolidar el Capítulo 2 de la memoria y preparar la demo del sprint (Semana 6)

### Módulo: Entornos de Desarrollo (ED)
- [x] T-ED-05: Comprender el ciclo de compilación a Bytecode y la virtualización en la JVM
- [x] T-ED-06: Crear y configurar la estructura de proyecto con Apache Maven (`pom.xml`)
- [ ] T-ED-07: Configurar y verificar el archivo `.gitignore` para exclusiones de compilación de Maven (`target/`)

### Módulo: Programación (PR)
- [x] T-PR-04: Instanciar y utilizar objetos de clases predefinidas (`Scanner`, `String`, `Math`, `Random`)
- [x] T-PR-05: Programar llamadas a métodos estáticos y métodos de instancia pasando parámetros
- [ ] T-PR-06: Integrar los cálculos y generación de cadenas en el código guía del proyecto propio
```

---

##### Paso 4. (Únicamente si los estudiantes ya lo han visto en ED) Confirmación y sincronización en GitHub
1. Confirma los cambios realizados con un mensaje convencional:
   ```bash
   git add pi/
   git commit -m "docs(pi): modelar diagrama de bloques funcional en drawio y estimar recursos"
   git push
   ```
2. Accede a tu repositorio remoto en GitHub desde el navegador y verifica:
    * Que el archivo `arquitectura-recursos.md` se visualiza correctamente formateado.
    * Que la imagen `diagrama-bloques.png` se renderiza de forma nítida dentro del documento sin enlaces rotos.

---

## Semana 6. Consolidación del Capítulo 2 de la memoria, cierre del Sprint Backlog 2 y defensa técnica del incremento v0.2

---

### Día 6 - 1 sesión

#### Teoría. Calidad documental en la ingeniería de requisitos, verificación de entregables y comunicación técnica

#### 1. Caso guía en AzaharTech

Es viernes 23 de octubre por la tarde en la sede de **AzaharTech** en Castellón de la Plana. Las tres semanas del segundo ciclo de desarrollo concluyen hoy.

En la sala de reuniones principal, **Laia Claramunt** proyecta el documento técnico consolidado del caso guía del **IES El Caminàs**. En pantalla se observa cómo el catálogo de requisitos redactado en la primera semana y el diagrama de bloques diseñado en Draw.io en la segunda semana se han ensamblado de forma armoniosa dentro de una memoria técnica unificada con numeración jerárquica y estilo corporativo impecable.

A su lado, **Alba Torres** tiene abierta la estructura de Apache Maven en IntelliJ y **Pau Ferrer** cronometra una presentación de prueba de tres minutos.

Laia toma la palabra dirigiéndose a los desarrolladores del equipo de trabajo:

> *«En las dos semanas anteriores definimos el catálogo de requisitos funcionales y modelamos la arquitectura funcional en Draw.io. En Programación habéis dominado el uso de objetos estándar como `Scanner`, `Math` y `String`, y en Entornos de Desarrollo habéis configurado la jerarquía estándar de Maven.*
>
> *Pero un proyecto de ingeniería no se entrega con notas sueltas dispersas por el disco duro. En AzaharTech, al finalizar cada ciclo de desarrollo, integramos todos los avances en un capítulo consolidado de la **Memoria del Proyecto**, auditamos que el **Sprint Backlog esté cerrado al 100 % de cumplimiento** y preparamos la **defensa oral de la solución técnica ante el cliente**.*
>
> *Hoy cerraremos formalmente el **Capítulo 2 de la memoria técnica de vuestro proyecto de la bolsa de proyectos**, comprobaremos que todos los requisitos y recursos están justificados sin ambigüedades y ensayaremos el guion de comunicación técnica para la Sprint Review del incremento v0.2»*.

---

#### 2. Calidad documental, verificación formal y comunicación técnica

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL CIERRE DOCUMENTAL DEL SPRINT 2                               │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Consolidación         │ 2. Cierre del Backlog       │ 3. Defensa oral de requisitos │
│    (Capítulo 2 memoria)  │    (Definition of Done)     │    (The 3-Minute Review)      │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ Se ensamblan requisitos, │ Se audita que todas las     │ Guion estructurado: requisitos│
│ bloques Draw.io, recursos│ tareas de PR, ED y PI están │ clave -> Modelo visual IPO -> │
│ y fuentes en un documento│ verificadas y marcadas:     │ Viabilidad y tecnologías base.│
│ formal normalizado.      │ - [x] 100% completado       │                               │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

##### A. La consolidación documental como garantía de ingeniería
Tener requisitos en un archivo, diagramas en una carpeta de imágenes y notas de recursos en borradores genera dispersión y desconfianza en el cliente.
* **El principio del documento maestro.** Al cierre de cada sprint, todos los elementos técnicos se integran en un documento consolidado bajo normas de estilo estrictas:
    1. Numeración jerárquica homogénea (1, 1.1, 1.2, 2, 2.1...).
    2. Tablas estandarizadas con identificadores unívocos (`RF-01`, `RNF-01`).
    3. Figuras técnicas incrustadas con pie numerado explicativo.
    4. Referencias bibliográficas a fuentes técnicas oficiales (estilo IEEE/APA).

##### B. Criterios de verificación y cierre del Sprint Backlog 2 (RA4.a)
Antes de dar por cerrado el sprint, el estudiante debe contrastar que los entregables cumplen la **Definición de Hecho (*Definition of Done - DoD*)**:
* Los requisitos no contienen adjetivos subjetivos ni funciones no verificables.
* El diagrama de bloques funcional está correctamente enlazado en Markdown mediante rutas relativas y se renderiza con nitidez en GitHub.
* La tabla de recursos distingue con claridad el equipamiento del cliente de las herramientas de desarrollo.
* El archivo `sprint2-backlog.md` refleja la realidad del repositorio: no pueden quedar casillas vacías (`- [ ]`) si el incremento se da por entregado.

##### C. Técnicas de oratoria técnica y defensa del incremento v0.2
Defender un catálogo de requisitos y un modelo de arquitectura ante un cliente o un comité evaluador requiere una técnica de comunicación específica:
* **No leer el documento.** La audiencia ya puede leer la pantalla. El ponente debe explicar el *porqué* de las decisiones de diseño.
* **Estructura de impacto en 3 minutos (*The 3-Minute Demo v0.2*):**
    * *Minuto 1 (Requisitos nucleares).* Explicar los dos requisitos funcionales más críticos del proyecto y la principal restricción no funcional (ej. compatibilidad con OpenJDK 21 LTS y Maven).
    * *Minuto 2 (Arquitectura en bloques).* Proyectar el diagrama de Draw.io y seguir el recorrido del dato desde el bloque de captura hasta la salida formateada.
    * *Minuto 3 (Viabilidad y apertura).* Resumir los recursos asignados, certificar la viabilidad y anticipar el objetivo del Sprint 3 (planificación temporal mediante Diagrama de Gantt y matriz de riesgos).
* **Control de la comunicación no verbal y autoconfianza:** Mantener contacto visual con la sala, voz firme y pausada, postura erguida y dominio del vocabulario técnico sin vacilaciones.

---

#### Laboratorio práctico guiado. Consolidación del Capítulo 2 de la memoria, cierre del Sprint Backlog 2 y preparación de la exposición

Laia Claramunt asigna las tareas de la sesión:
> *«Durante los próximos treinta minutos, cada uno de vosotros ensamblará el **Capítulo 2 consolidado de la Memoria del Proyecto (`capitulo2-requisitos-arquitectura.md`)** de su proyecto elegido. Comprobaréis que el diagrama de Draw.io se muestra impecable, cerraréis el **Sprint Backlog 2 al 100 % de cumplimiento** y redactaréis el guion de vuestra presentación oral de tres minutos»*.

---

##### Paso 1. Redacción del capítulo 2 (`pi/docs/capitulo2-requisitos-arquitectura.md`)
1. Abre tu proyecto en **IntelliJ IDEA**.
2. Dentro de tu carpeta `azahartech/nombre-equipo/apellidos-nombre/pi/docs/`, crea el archivo `capitulo2-requisitos-arquitectura.md`.
3. Ensambla y unifica los contenidos trabajados en las semanas 4 y 5 aplicando la plantilla oficial de AzaharTech para **tu proyecto de la bolsa de proyectos**:

```markdown
# Memoria técnica del proyecto — Capítulo 2. Requisitos y arquitectura funcional
**Consultora:** AzaharTech Software Consulting  
**Proyecto Seleccionado:** [nombre de tu proyecto de la bolsa de proyectos]  
**Cliente / Sector:** [nombre de la empresa o sector profesional]  
**Desarrollador/a:** [tus apellidos, tu nombre]  
**Fecha de Cierre:** 23 de octubre de 2026  
**Versión:** 1.0 (Incremento v0.2)  

---

## 1. Objetivos del sistema y delimitación del alcance
El propósito de este incremento es formalizar el catálogo exhaustivo de requisitos técnicos del sistema, modelar visualmente la interacción de sus subsistemas funcionales y cuantificar los recursos materiales y humanos indispensables para garantizar la viabilidad del software.

---

## 2. Catálogo oficial de requisitos del sistema
### 2.1 Requisitos Funcionales (RF)
| Código | Nombre del Requisito | Descripción técnica obligatoria | Prioridad |
| :---: | :--- | :--- | :---: |
| **RF-01** | Captura interactiva | El sistema solicitará los identificadores de operación y parámetros iniciales de entrada. | Alta |
| **RF-02** | Procesamiento estándar | El sistema empleará clases predefinidas de Java (Scanner, Math, String) para la transformación de datos. | Alta |
| **RF-03** | Identificación unívoca | El sistema generará códigos alfanuméricos combinando prefijos corporativos y marcas de tiempo. | Media |
| **RF-04** | Resumen formateado | El sistema emitirá comprobantes estructurados por consola acotando la precisión decimal. | Media |

### 2.2 Requisitos No Funcionales (RNF)
| Código | Categoría | Restricción técnica o estándar aplicable | Criterio de Verificación |
| :---: | :--- | :--- | :--- |
| **RNF-01** | Plataforma base | Ejecución sobre la Máquina Virtual de Java utilizando OpenJDK 21 LTS sin dependencias propietarias. | Verificación de versión JVM |
| **RNF-02** | Gestión de proyecto | Estructura del proyecto y gestión del ciclo de construcción automatizada mediante Apache Maven (`pom.xml`). | Inspección del descriptor POM |
| **RNF-03** | Calidad documental | Documentación viva en formato Markdown con rutas relativas e imágenes optimizadas en PNG/SVG. | Auditoría del repositorio |

---

## 3. Modelo de Arquitectura Funcional (IPO)
La solución técnica se divide en tres subsistemas funcionales desacoplados cuyo flujo de información se representa en el siguiente esquema:

![Diagrama de Bloques Funcional](img/diagrama-bloques.png)  
*Figura 1. Diagrama de bloques funcional de la arquitectura del sistema (Entrada-Procesamiento-Salida).*

* **Subsistema de Entrada.** Responsable de la captura y validación inicial de los datos introducidos por el usuario o periférico.
* **Subsistema de Procesamiento.** Implementado en Java, aplica las reglas matemáticas y de negocio transformando los datos en memoria.
* **Subsistema de Salida.** Canaliza la presentación de los resultados hacia la pantalla o consola mediante formatos tabulares.

---

## 4. Previsión y justificación de recursos
| Tipo de Recurso | Detalle del Recurso | Justificación de Ingeniería |
| :--- | :--- | :--- |
| **Recursos Humanos** | Desarrollador/a de software | Dedicación estimada de 34 horas presenciales en aula más trabajo autónomo. |
| **Entorno Hardware** | Puesto de trabajo PC / Portátil | Equipo con 8 GB de RAM y procesador multi-núcleo para ejecución del IDE. |
| **Entorno Software** | OpenJDK 21 + IntelliJ Community | Pila tecnológica libre y estándar de la industria para desarrollo multiplataforma. |
| **Control de Proyecto**| Apache Maven + Git/GitHub | Trazabilidad del código, gestión de versiones y automatización de la construcción. |

---

## 5. Referencias técnicas oficiales
1. **Oracle Java SE Documentation (JDK 21 API):** Especificación de clases estándar de la biblioteca Java. URL: `https://docs.oracle.com/en/java/javase/21/`
2. **Apache Maven Documentation:** Guía de arquitectura de directorios estándar y ciclo de vida de construcción. URL: `https://maven.apache.org/`

---

## 6. Registro ético de uso de inteligencia artificial (prompt log del Sprint 2)
| Fecha | Herramienta | Objetivo de la consulta | Prompt introducido | Criterio de ajuste personal |
| :---: | :---: | :--- | :--- | :--- |
| 23/10/2026 | ChatGPT / Claude | Revisar consistencia de requisitos | *"Revisa si estos 4 requisitos funcionales presentan solapamientos o ambigüedades..."* | Se unificaron términos técnicos y se confirmó que ningún requisito exige bases de datos externas en el Sprint 2. |
```

---

##### Paso 2. Cierre y verificación del Sprint Backlog 2 (`pi/backlog/sprint2-backlog.md`)
1. Abre tu archivo `sprint2-backlog.md`.
2. Actualiza **absolutamente todas las tareas del sprint marcándolas como completadas (`- [x]`)**:

```markdown
# Sprint Backlog 2 — [nombre de tu proyecto]

## Tareas

### Módulo: Proyecto Intermodular (PI)
- [x] T-PI-06: Redactar el catálogo de requisitos funcionales y no funcionales (`pi/docs/requisitos-sistema.md`)
- [x] T-PI-07: Contrastar fuentes técnicas oficiales y registrar el *Prompt Log*
- [x] T-PI-08: Modelar el diagrama de bloques funcional en Draw.io (`pi/docs/img/diagrama-bloques.png`)
- [x] T-PI-09: Consolidar el Capítulo 2 de la memoria y preparar el guion de defensa técnica v0.2

### Módulo: Entornos de Desarrollo (ED)
- [x] T-ED-05: Comprender el ciclo de compilación a Bytecode y la virtualización en la JVM
- [x] T-ED-06: Crear y configurar la estructura de proyecto con Apache Maven (`pom.xml`)
- [x] T-ED-07: Configurar y verificar el archivo `.gitignore` para exclusiones de compilación de Maven (`target/`)

### Módulo: Programación (PR)
- [x] T-PR-04: Instanciar y utilizar objetos de clases predefinidas (`Scanner`, `String`, `Math`, `Random`)
- [x] T-PR-05: Programar llamadas a métodos estáticos y métodos de instancia pasando parámetros
- [x] T-PR-06: Integrar los cálculos y generación de cadenas en el código maestro del proyecto propio
```

---

##### Paso 3. Preparación de la ficha de guion de exposición (3 Minutos)
Añade al final de tu documento consolidado o en tu libreta técnica el guion para la *Sprint Review*:

```markdown
### Guion de Exposición Técnica: Sprint Review v0.2 (3 Minutos)
* **00:00 - 01:00 (Catálogo de Requisitos).** Saludo formal, nombre del proyecto, cliente y explicación concisa de los dos requisitos funcionales principales (RF-01 y RF-02) y la restricción tecnológica (RNF-01: OpenJDK 21).
* **01:00 - 02:00 (Arquitectura Visual).** Proyección del diagrama de bloques de Draw.io, explicando el recorrido del dato desde el subsistema de entrada hasta la salida estructurada.
* **02:00 - 03:00 (Viabilidad y Apertura al Sprint 3).** Certificación de la viabilidad técnica y recursos materiales, confirmación del cierre de tareas en GitHub y anticipación del objetivo del Sprint 3 (planificación temporal mediante Diagrama de Gantt y gestión de riesgos).
```

---

##### Paso 4. (Únicamente si los estudiantes ya lo han visto en ED) Confirmación y sincronización en GitHub
1. Realiza el commit convencional y push:
   ```bash
   git add pi/
   git commit -m "docs(pi): consolidar capitulo 2 de la memoria y cerrar sprint backlog 2 al 100 por ciento"
   git push
   ```
2. Accede a tu repositorio en GitHub desde el navegador y comprueba que `capitulo2-requisitos-arquitectura.md` se visualiza con su formato Markdown, la imagen de Draw.io y todas las casillas del backlog marcadas con el check `[x]`.

---

### Resumen del Sprint 2 de Proyecto Intermodular completado
Al concluir estas 3 sesiones de los viernes (3 horas lectivas en total):
1. Has formalizado el **catálogo oficial de requisitos del sistema**, clasificando con precisión los Requisitos Funcionales (RF) y No Funcionales (RNF) bajo criterios verificables y sin ambigüedades.
2. Has modelado visualmente la arquitectura técnica mediante **Draw.io**, exportando e incrustando el **Diagrama de Bloques Funcional (IPO)** con tratamiento profesional de imágenes técnicas en Markdown.
3. Has justificado con rigor la **previsión de recursos materiales y humanos**, contrastando fuentes oficiales de la industria (Oracle y Apache Maven) y manteniendo el registro ético de IA mediante el **Prompt Log del Sprint 2**.
4. Cuentas con el **Capítulo 2 de la Memoria Técnica consolidado**, el **Sprint Backlog 2 al 100 %** y un guion ensayado para la **defensa técnica del incremento v0.2**, dejando el proyecto plenamente preparado para abordar en el Sprint 3 la planificación temporal mediante diagramas de Gantt y la gestión de riesgos.