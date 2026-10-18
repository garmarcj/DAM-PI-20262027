# Sprint 3. Cronograma y planificación temporal del proyecto

---

## Semana 7. Secuenciación de tareas, cronograma y Sprint Backlog 3

---

### Día 7 - 1 sesión

#### Teoría. Secuenciación de fases, estimación temporal y dependencias

#### 1. Caso guía en AzaharTech

Es viernes 30 de octubre de 2026 por la tarde en la sede de **AzaharTech** en Castellón de la Plana. Tras una semana de intenso trabajo dominando las bifurcaciones y los bucles en Programación, junto con el manejo del depurador en Entornos de Desarrollo, el equipo se reúne en la sala de planificación para iniciar formalmente el **Sprint 3**.

En el panel interactivo, **Laia Claramunt** tiene desplegado un calendario que abarca desde la situación presente hasta el final del curso, junto con una estructura desglosada del sistema de control de acceso por QR del **IES El Caminàs**. A su lado, **Alba Torres** revisa la lista de tareas pendientes del motor de lectura y **Pau Ferrer** anota las duraciones estimadas de cada módulo.

Laia toma la palabra dirigiéndose al equipo:

> *«En los dos primeros sprints habéis sentado los cimientos: analizasteis las necesidades del cliente, redactasteis el catálogo de requisitos funcionales y no funcionales, y dibujasteis la arquitectura visual de la aplicación. Pero en la ingeniería del software real, una excelente arquitectura sin una planificación temporal rigurosa está condenada al fracaso.*
>
> *Si el equipo directivo del IES El Caminàs nos pregunta cuándo entrará en funcionamiento el lector del vestíbulo o qué ocurrirá si el módulo de validación se retrasa tres semanas, no podemos responder con suposiciones. Necesitamos una **Estructura de Descomposición del Trabajo (EDT)**, una matriz de duraciones y precedencias, y un **Diagrama de Gantt** que visibilice el camino crítico del proyecto.*
>
> *Hoy aprenderemos a secuenciar las fases del desarrollo, estimaremos el esfuerzo en horas lectivas reales, construiremos el cronograma temporal combinando herramientas visuales y código declarativo, y abriremos el **Sprint Backlog 3**, que asegurará que el ritmo de trabajo sea constante, predecible y profesional»*.

---

#### 2. Fundamentos de secuenciación y planificación temporal

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL CICLO DE PLANIFICACIÓN TEMPORAL                              │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Descomposición (EDT)  │ 2. Estimación y Dependencias│ 3. Cronograma (Gantt)         │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ ¿Qué paquetes de trabajo │ ¿Cuánto tiempo exige cada   │ ¿En qué fechas exactas se     │
│ componen el producto de  │ tarea y qué actividades     │ ejecutan las fases y cuáles   │
│ forma tangible?          │ deben finalizar antes?      │ marcan el camino crítico?     │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

##### A. Estructura de Descomposición del Trabajo (EDT / WBS)

La Estructura de Descomposición del Trabajo (EDT, o *Work Breakdown Structure* en inglés) es una técnica fundamental de gestión que consiste en fragmentar un proyecto complejo en componentes más pequeños, manejables e independientes:

* **Orientación a entregables.** Cada elemento terminal de la EDT debe asociarse a un resultado verificable (un documento técnico formal, una clase Java compilada, un conjunto de casos de prueba o una etiqueta de versión en Git).
* **Nivel de granularidad adecuado.** Una tarea excesivamente genérica (*«programar la aplicación»*) genera incertidumbre; una tarea minúscula (*«declarar variable booleana»*) asfixia la gestión. El tamaño óptimo de un paquete de trabajo se sitúa entre las 2 y las 12 horas.
* **Criterio del 100 %:** La suma del trabajo de los niveles inferiores debe equivaler con total exactitud al alcance comprometido con el cliente, sin omitir tareas ni añadir requisitos fuera de contrato (*scope creep*).

##### B. Estimación de tiempos y gestión de dependencias entre tareas

Ninguna tarea de desarrollo ocurre en el vacío. Para articular un cronograma creíble es imprescindible definir las relaciones lógicas entre actividades:

* **Dependencia Fin a Inicio (FS - *Finish to Start*).** Es la más habitual en software. Una actividad no puede comenzar hasta que su predecesora haya concluido satisfactoriamente (*ejemplo: no se puede iniciar la depuración de algoritmos en Entornos de Desarrollo sin tener implementada la lógica condicional en Programación*).
* **Hitos del proyecto (*Milestones*).** Puntos de control temporales de duración cero que marcan el cierre formal de una fase (*por ejemplo: H1 - Catálogo de requisitos cerrado, H2 - Entrega v0.3 del prototipo*).
* **Camino crítico.** La secuencia encadenada de tareas que determina la duración total mínima del proyecto. Cualquier retraso en una tarea situada en el camino crítico pospone de forma inmediata la fecha de entrega acordada con el cliente.

##### C. Modelado del cronograma: herramientas de código y software visual

La representación de un cronograma debe ser accesible, mantenible y versionable junto con el resto del proyecto. En nuestro flujo de trabajo disponemos de dos alternativas complementarias:

1. **Modelado declarativo mediante código (Mermaid en Markdown).** Permite describir diagramas de Gantt mediante bloques de texto estructurado dentro de los propios documentos Markdown. Esta opción facilita el control de versiones en Git, la revisión de cambios mediante `git diff` y su visualización automática tanto en GitHub como en el visor interno del IDE.
2. **Modelado visual con software especializado de escritorio (GanttProject - https://www.ganttproject.biz/download/).** Para quienes prefieran diseñar y ajustar la planificación mediante una interfaz gráfica dedicada, **GanttProject** es una aplicación libre y multiplataforma orientada al cálculo de rutas críticas, dependencias y asignación de recursos. En entornos GNU/Linux puede ejecutarse descargando directamente su versión portable y lanzando el binario desde el directorio del usuario sin requerir instalaciones del sistema operativo, exportando el resultado en un archivo PNG.

##### D. Fuentes técnicas oficiales y uso ético de la Inteligencia Artificial

* **Estándares internacionales de gestión.** La estructuración de las fases se apoya en las directrices de la norma ISO/IEC/IEEE 12207 (Procesos del ciclo de vida del software) y la Guía Scrum oficial.
* **Uso ético y crítico de la IA.** La Inteligencia Artificial resulta muy útil para obtener propuestas de desgloses de tareas iniciales y contrastar posibles dependencias técnicas que el analista novel suele pasar por alto. Sin embargo, los tiempos deben contrastarse siempre con el calendario lectivo oficial y las horas reales asignadas a cada módulo. Cada sugerencia de la IA debe documentarse de forma transparente en el *Prompt Log*.

---

#### Laboratorio. Planificación temporal, cronograma y Sprint Backlog 3

Laia Claramunt asigna los objetivos operativos para la sesión:

> *«Durante los próximos minutos, cada estudiante abrirá su repositorio y creará el documento formal de cronograma y secuenciación de su proyecto singular de la bolsa de proyectos. Modelaréis las fases del proyecto hasta el cierre del curso, definiréis la matriz de dependencias, incorporaréis el Diagrama de Gantt y crearéis el archivo **`sprint3-backlog.md`** que coordinará las tres semanas que tenemos por delante»*.

---

##### Paso 1. Creación del documento de cronograma (`pi/docs/cronograma.md`)

1. Abre tu proyecto en **IntelliJ IDEA**.
2. En la carpeta `azahartech/nombre-equipo/apellidos-nombre/pi/docs/`, crea el archivo `cronograma.md`.
3. Redacta el contenido aplicando la plantilla técnica adaptada a **tu proyecto de la bolsa de proyectos**:

```markdown
# Planificación temporal, secuenciación de fases y cronograma
**Consultora:** AzaharTech Software Consulting  
**Proyecto Seleccionado:** [nombre de tu proyecto de la bolsa de proyectos]  
**Cliente / Sector:** [entidad receptora o sector profesional]  
**Desarrollador/a:** [tus apellidos, tu nombre]  
**Fecha:** 30 de octubre de 2026  
**Versión:** 1.0 (Sprint 3)  

---

## 1. Estructura de Descomposición del Trabajo (EDT)
El ciclo de vida del proyecto se divide en cuatro grandes fases secuenciales orientadas a entregables verificables:

* **Fase 1: Análisis y Viabilidad (Sprints 1 y 2 - Semanas 1 a 6).** Definición del problema, requisitos funcionales/no funcionales y arquitectura base.
* **Fase 2: Construcción del Núcleo y Control de Calidad (Sprints 3 y 4 - Semanas 7 a 12).** Implementación de la lógica algorítmica, validación de entradas, control de excepciones y auditoría de pruebas en consola.
* **Fase 3: Almacenamiento, Concurrencia e Interfaz Gráfica (Sprints 5 a 8 - Semanas 13 a 24).** Estructuras dinámicas de datos, persistencia en archivos estructurados y desarrollo de interfaces con Swing.
* **Fase 4: Consolidación Final y Pase a Producción (Semanas 25 a 30).** Pruebas de integración, empaquetado con Maven y defensa técnica pública.

---

## 2. Matriz de tareas, estimaciones y dependencias

| ID Tarea | Descripción del Paquete de Trabajo | Módulo | Duración Estimada | Dependencia (Predecesora) | Hito Asociado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **T-01** | Catálogo de requisitos y arquitectura IPO | PI | 6 h | Ninguna | H1: Base aprobada |
| **T-02** | Configuración de entorno Maven y Git | ED | 9 h | Ninguna | H1: Base aprobada |
| **T-03** | Lógica con clases estándar Java | PR | 48 h | Ninguna | Incremento v0.2 |
| **T-04** | Cronograma de fases y matriz de riesgos | PI | 3 h | T-01 | H2: Planificación |
| **T-05** | Implementación de bucles y control condicional | PR | 24 h | T-03 | Incremento v0.3 |
| **T-06** | Pruebas de código y depuración con breakpoints | ED | 9 h | T-05 | Incremento v0.3 |
| **T-07** | POO modular y encapsulamiento | PR | 24 h | T-05 | Prototipo v0.4 |
| **T-08** | Versionado de ramas y empaquetado | ED | 9 h | T-06 | Prototipo v0.4 |
| **T-09** | Dossier técnico y defensa final Sprint 4 | PI | 3 h | T-04, T-07 | H3: Fin Trimestre 1 |

---

## 3. Cronograma del proyecto (Diagrama de Gantt)

Elige una de las dos modalidades de representación técnica e incorpórala a este apartado:

### Opción A: Diagrama declarativo en código Mermaid

gantt
    title Cronograma de Desarrollo — AzaharTech Consulting
    dateFormat  YYYY-MM-DD
    axisFormat  %d/%m

    section Fase 1: Fundamentos y Requisitos
    Análisis y requisitos (Sprints 1 y 2)    :done, f1, 2026-09-14, 2026-10-23
    Hito 1 - Incremento v0.2 alcanzado       :milestone, m1, 2026-10-23, 0d

    section Fase 2: Lógica y Depuración
    Planificación temporal y riesgos (PI)    :active, t_pi3, 2026-10-26, 2026-11-13
    Estructuras de control y bucles (PR)     :active, t_pr3, 2026-10-26, 2026-11-13
    Depuración paso a paso e incidencias (ED):active, t_ed3, 2026-10-26, 2026-11-13
    Hito 2 - Incremento v0.3 consolidado     :milestone, m2, 2026-11-13, 0d

    section Fase 3: Arquitectura de Clases
    Diseño de clases y miembros (PR)        :t_pr4, 2026-11-16, 2026-12-04
    Ramas en Git y documentación (ED)        :t_ed4, 2026-11-16, 2026-12-04
    Dossier técnico y cierre T1 (PI)         :t_pi4, 2026-11-16, 2026-12-04
    Hito 3 - Prototipo individual completo   :milestone, m3, 2026-12-04, 0d

### Opción B: Diagrama exportado desde herramienta de escritorio

Si has modelado tu planificación en una herramienta de escritorio como **GanttProject**, guarda la imagen recortada en `pi/docs/img/cronograma-gantt.png` y referénciala aquí:

![Cronograma de Fases del Proyecto](img/cronograma.png)  
*Figura 1. Cronograma temporal detallado y dependencias del sistema.*

---

## 4. Fuentes técnicas y estándares de gestión
* **ISO/IEC/IEEE 12207:2017:** Systems and software engineering — Software life cycle processes.
* **Scrum Guide (Ken Schwaber & Jeff Sutherland):** Principios de inspección, adaptación y definición del trabajo en sprints.
* **Documentación oficial de Oracle Java SE 21:** Estructuras sintácticas de bucles y gestión de excepciones en el lenguaje Java.

---

## 5. Registro ético de uso de Inteligencia Artificial (Prompt Log)

| Fecha | Herramienta | Objetivo de la consulta | Prompt introducido | Revisión crítica y ajuste aplicado |
| :---: | :---: | :--- | :--- | :--- |
| 30/10/2026 | ChatGPT / Claude | Estructurar dependencias del proyecto | *"Actúa como jefe de proyectos y sugiere una secuencia de dependencias lógicas para una aplicación Java que requiere validación de datos en consola..."* | Se ajustaron las duraciones al calendario de 3 semanas por sprint y se eliminaron tareas de base de datos no aplicables a esta fase. |
```

---

##### Paso 2. Creación del Sprint Backlog 3 (`pi/backlog/sprint3-backlog.md`)

1. En la carpeta `azahartech/nombre-equipo/apellidos-nombre/pi/backlog/`, crea el archivo `sprint3-backlog.md`.
2. Registra los compromisos de trabajo del **Sprint 3 (26 oct – 13 nov)** coordinando los tres módulos:

```markdown
# Sprint Backlog 3 — [nombre de tu proyecto]
**Periodo:** 26 de octubre – 13 de noviembre de 2026  
**Responsable:** [tu nombre]  

## Objetivo general del Sprint 3
Construir el incremento v0.3: definir la secuenciación temporal y matriz de riesgos en Proyecto Intermodular, dominar el uso de puntos de ruptura y seguimiento de variables en Entornos de Desarrollo, e implementar estructuras de control condicionales y repetitivas robustas en Programación.

---

## Tareas

### Módulo: Proyecto Intermodular (PI)
- [ ] T-PI-10: Elaborar la EDT, matriz de dependencias y Diagrama de Gantt (`pi/docs/cronograma.md` o `pi/docs/img/cronograma.png`)
- [ ] T-PI-11: Registrar el uso ético de IA (*Prompt Log*) en la planificación temporal
- [ ] T-PI-12: Redactar la matriz de riesgos técnicos y planes de contingencia (Semana 8)
- [ ] T-PI-13: Consolidar el Capítulo 3 de la memoria y ensayar la demo técnica v0.3 (Semana 9)

### Módulo: Entornos de Desarrollo (ED)
- [ ] T-ED-08: Diseñar casos de prueba de caja negra aplicando particiones de equivalencia y valores límite
- [ ] T-ED-09: Configurar puntos de ruptura (*breakpoints*) condicionales en IntelliJ IDEA para inspección de memoria
- [ ] T-ED-10: Documentar el procedimiento formal de recogida y registro de incidencias técnicas (Semana 8)

### Módulo: Programación (PR)
- [ ] T-PR-07: Implementar lógica condicional mediante bloques `if / else if / else` y selector `switch`
- [ ] T-PR-08: Construir bucles iterativos controlados (`while`, `for`) para la captura repetitiva de datos
- [ ] T-PR-09: Incorporar gestión de excepciones básica con bloques `try-catch` frente a entradas erróneas del usuario
```

---

##### Paso 3. Confirmación y sincronización en GitHub

1. En IntelliJ IDEA, abre el panel de control de versiones **Commit** mediante el atajo de teclado (`Ctrl + K`).
2. Verifica que se encuentran seleccionados los archivos creados durante la sesión:
    * *(Opcion A)*`pi/docs/cronograma.md` si has utilizado la opción de modelado declarativo.
    * `pi/backlog/sprint3-backlog.md`
    * *(Opcion B)* `pi/docs/img/cronograma.png` si has utilizado la opción modelado visual.
3. Escribe el mensaje de confirmación siguiendo el formato estandarizado de **Conventional Commits**:

```text
docs(pi): definir secuenciacion de tareas, cronograma y abrir sprint backlog 3
```

4. Pulsa sobre el botón **Commit and Push**.
5. Accede a tu repositorio remoto en GitHub desde el navegador y verifica que los archivos aparecen estructurados correctamente y que el diagrama se visualiza con absoluta nitidez.

---

## Semana 9. Consolidación de la memoria técnica y demo del incremento v0.3

---

### Día 9 - 1 sesión

#### Teoría. Cierre del incremento de producto, consolidación documental y defensa técnica

#### 1. Caso guía en AzaharTech

Es viernes 13 de noviembre de 2026 por la tarde en la sede de **AzaharTech** en Castellón de la Plana. Tras tres semanas de trabajo continuado, el equipo alcanza el cierre del **Sprint 3**.

En el proyector de la sala de reuniones, **Alba Torres** ejecuta la versión actualizada del lector QR para el **IES El Caminàs**. Introduce deliberadamente datos incorrectos, códigos en blanco y entradas no numéricas en la consola: el sistema responde con mensajes claros de advertencia, solicita de nuevo los datos mediante un bucle controlado y jamás interrumpe su ejecución. En otra pestaña, **Pau Ferrer** muestra el historial de incidencias resueltas en Entornos de Desarrollo tras localizar la causa raíz en memoria con el depurador de IntelliJ IDEA.

**Laia Claramunt** asiente satisfecha y toma el control de la sesión:

> *«Habéis logrado transformar un código frágil en una solución robusta. En Programación vuestro algoritmo valida y controla cualquier entrada imprevista; en Entornos de Desarrollo habéis verificado con breakpoints que el flujo en memoria es el adecuado y habéis registrado formalmente las incidencias técnicas; y en Proyecto Intermodular tenéis el proyecto secuenciado en el cronograma y los riesgos bajo control con planes de contingencia reales.*
>
> *Sin embargo, el incremento técnico no está terminado hasta que se consolida documentalmente en la memoria global y se defiende con profesionalidad ante el cliente. Igual que hicimos al cierre del Sprint 1 y del Sprint 2, no podemos dejar documentos técnicos fragmentados y aislados.*
>
> *Hoy unificaremos el trabajo de las semanas 7 y 8 dentro de nuestro documento maestro **`memoria.md`** incorporando el **Capítulo 3**, cerraremos al 100 % el **Sprint Backlog 3**, estructuraremos el guion de la demostración oral de 3 minutos y marcaremos en nuestro repositorio la versión formal mediante la etiqueta **`v0.3`** utilizando la interfaz visual de IntelliJ IDEA con su correspondiente sincronización de tags»*.

---

#### 2. Fundamentos de consolidación y comunicación técnica

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL CIERRE DEL INCREMENTO DE SPRINT                              │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Consolidación Memoria │ 2. Cierre de Backlog        │ 3. Sprint Review (3 minutos)  │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ Integrar cronograma,     │ Verificar que todas las     │ Demostrar el valor en vivo:   │
│ matriz de riesgos e      │ tareas cumplen la DoD y     │ lógica robusta, depuración y  │
│ incidencias en memoria.md│ registrar el 100 % de éxito.│ cumplimiento del cronograma.  │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

##### A. Integración documental acumulativa en la memoria técnica

La memoria técnica del proyecto es un documento vivo que crece con cada sprint de forma incremental. Al finalizar el Sprint 3, se incorpora el **Capítulo 3 (Planificación temporal, gestión de riesgos y control de incidencias)** a continuación de los capítulos ya consolidados:

* **Capítulo 1 (Sprint 1).** Análisis de necesidades, problemática operativa del cliente, vinculación con ODS y viabilidad técnica inicial.
* **Capítulo 2 (Sprint 2).** Catálogo formal de requisitos funcionales y no funcionales, modelado visual de arquitectura y previsión de recursos.
* **Capítulo 3 (Sprint 3).** Secuenciación de fases (EDT/WBS), cronograma y dependencias (Gantt), matriz de evaluación de riesgos con planes de contingencia y procedimiento formal de registro y resolución de incidencias.

Integrar estos contenidos en `memoria.md` garantiza que cualquier revisor, cliente o tribunal disponga de un documento técnico único, coherente y trazable.

##### B. Criterio de Hecho (*Definition of Done* - DoD) y cierre de sprint

Antes de dar por concluido el sprint, cada tarea debe cumplir unos requisitos innegociables:
* Código Java compilable sin advertencias ni dependencias rotas.
* Algoritmos de control ejecutables con excepciones capturadas de forma preventiva.
* Memoria técnica consolidada en `memoria.md` sin enlaces rotos ni inconsistencias de formato.
* Pruebas manuales superadas y registradas en el cuaderno de incidencias.

##### C. Estructura de la demostración técnica en 3 minutos (*Pitch*)

Una defensa técnica ante un cliente o un tribunal evaluador debe ser precisa, estructurada y basada en hechos verificables:

* **Minuto 1. Contexto, hito alcanzado y cumplimiento temporal.** Presentar el proyecto, indicar en qué punto del cronograma se encuentra el equipo y destacar el principal riesgo mitigado durante el sprint.
* **Minuto 2. Demostración técnica en vivo (en consola).** Ejecutar la aplicación, forzar intencionadamente una entrada errónea para evidenciar que el control de excepciones y los bucles mantienen el programa estable sin caídas de ejecución.
* **Minuto 3. Sinergia técnica, lecciones aprendidas y próximos pasos.** Explicar cómo el depurador de IntelliJ IDEA permitió resolver incidencias en memoria y anticipar la transición hacia el Sprint 4 (diseño de clases propias y orientación a objetos).

##### D. Soporte visual para la exposición: código declarativo y herramientas de escritorio

Para proyectar el soporte visual de la defensa se cuenta con dos vías de trabajo:

1. **Presentaciones declarativas basadas en código (Marp en Markdown).** Permite generar diapositivas directamente a partir de archivos Markdown delimitados por separadores `---`. Esta opción permite que la presentación se mantenga dentro del propio repositorio de Git y se visualice en cualquier visor web o extensión del editor de código.
2. **Presentaciones mediante software visual de escritorio (LibreOffice Impress).** Aplicación de software libre para la creación de diapositivas con soporte multimedia y esquemas gráficos. En entornos GNU/Linux puede ejecutarse mediante su versión portable en formato AppImage descargada en la carpeta del usuario (`~/bin/` o `~/Descargas/`), otorgando permisos de ejecución y lanzándola directamente sin requerir privilegios de superusuario, exportando la presentación en formato PDF en la carpeta de documentación.

##### E. Etiquetado visual de versiones en IntelliJ IDEA (*Semantic Tagging*)

Al finalizar cada sprint, el repositorio debe reflejar el estado exacto del código y la documentación mediante una etiqueta anotada de Git:

* La etiqueta formal `v0.3` no requiere comandos de terminal; puede generarse de forma gráfica directamente desde el entorno de desarrollo mediante los diálogos de control de versiones de IntelliJ IDEA.
* Al enviar los cambios al repositorio remoto, se activa la opción de sincronización de etiquetas (*Push Tags*) para que la versión quede publicada inmediatamente en GitHub.

---

#### Laboratorio. Consolidación de la memoria técnica, cierre de backlog y demo v0.3

Laia Claramunt marca los pasos para la sesión práctica:

> *«Es el momento de cerrar el Sprint 3. Cada estudiante abrirá su archivo **`memoria.md`**, añadirá al final el **Capítulo 3** aunando lo trabajado en `cronograma.md` y `riesgos-incidencias.md`, verificará y marcará al 100 % las tareas de su **Sprint Backlog 3**, redactará el **guion de la defensa técnica** de 3 minutos y sellará visualmente su entrega con la etiqueta **`v0.3`** en IntelliJ IDEA»*.

---

##### Paso 1. Consolidación de la memoria técnica (`pi/docs/memoria.md`)

1. Abre tu proyecto en **IntelliJ IDEA**.
2. Abre el archivo maestro `azahartech/nombre-equipo/apellidos-nombre/pi/docs/memoria.md`.
3. Al final del documento (tras el Capítulo 2), añade el **Capítulo 3**, integrando el contenido de `cronograma.md` y `riesgos-incidencias.md` adaptado a **tu proyecto de la bolsa de proyectos**:

```markdown

---

# Capítulo 3: Planificación temporal, gestión de riesgos y control de incidencias

## 3.1. Estructura de Descomposición del Trabajo (EDT)
El desarrollo del proyecto se desglosa en cuatro fases orientadas a entregables tangibles e independientes:

* **Fase 1: Análisis y Viabilidad (Semanas 1 a 6 - Sprints 1 y 2).** Definición operativa del problema, catálogo de requisitos y modelado de arquitectura IPO.
* **Fase 2: Construcción del Núcleo y Control de Calidad (Semanas 7 a 12 - Sprints 3 y 4).** Implementación de la lógica algorítmica, validación de datos, control de excepciones y auditoría con depurador.
* **Fase 3: Almacenamiento, Concurrencia e Interfaz Gráfica (Semanas 13 a 24 - Sprints 5 a 8).** Colecciones dinámicas, serialización y desarrollo de interfaces con Swing.
* **Fase 4: Consolidación y Pase a Producción (Semanas 25 a 30).** Pruebas de integración, empaquetado Maven y defensa pública.

---

## 3.2. Cronograma de proyecto y camino crítico

### Matriz de tareas y dependencias
| ID Tarea | Descripción del Paquete de Trabajo | Módulo | Duración | Dependencia | Hito Asociado |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **T-01** | Catálogo de requisitos y arquitectura IPO | PI | 6 h | Ninguna | H1: Base aprobada |
| **T-02** | Configuración de entorno Maven y Git | ED | 9 h | Ninguna | H1: Base aprobada |
| **T-03** | Lógica con clases estándar Java | PR | 48 h | Ninguna | Incremento v0.2 |
| **T-04** | Cronograma de fases y matriz de riesgos | PI | 3 h | T-01 | H2: Planificación |
| **T-05** | Implementación de bucles y control condicional | PR | 24 h | T-03 | Incremento v0.3 |
| **T-06** | Pruebas de código y depuración con breakpoints | ED | 9 h | T-05 | Incremento v0.3 |
| **T-07** | POO modular y encapsulamiento | PR | 24 h | T-05 | Prototipo v0.4 |
| **T-08** | Versionado de ramas y empaquetado | ED | 9 h | T-06 | Prototipo v0.4 |
| **T-09** | Dossier técnico y defensa final Sprint 4 | PI | 3 h | T-04, T-07 | H3: Fin Trimestre 1 |

### Diagrama de Gantt
*(Incluye aquí el bloque de código Mermaid con el cronograma o la referencia a la imagen `img/cronograma.png` generada con GanttProject).*

---

## 3.3. Evaluación de riesgos y planes de contingencia

### Matriz de riesgos cuantificada
| ID | Categoría | Descripción del Riesgo | Prob. (1-5) | Imp. (1-5) | Severidad | Nivel |
| :---: | :---: | :--- | :---: | :---: | :---: | :---: |
| **RSK-01** | Técnico | Bloqueo o finalización abrupta por entrada no numérica en consola | 4 | 4 | **16** | Crítico |
| **RSK-02** | Técnico | Bucle infinito en la lógica de validación o espera | 3 | 4 | **12** | Medio |
| **RSK-03** | Organizativo | Desviación temporal en la entrega del incremento v0.3 | 3 | 3 | **9** | Medio |
| **RSK-04** | Alcance | Modificaciones de requisitos sin control previo de cambios | 2 | 4 | **8** | Medio |
| **RSK-05** | Técnico | Corrupción de datos por valores fuera de rango admisible | 3 | 5 | **15** | Crítico |

*(Incluye aquí el cuadrante declarativo en Mermaid o la referencia a la imagen `img/matriz-riesgos.png` exportada desde Draw.io Desktop).*

### Medidas de prevención y planes de contingencia operativos
* **Plan para RSK-01 (Entradas anómalas):** Captura preventiva mediante bloques `try-catch` y reintento guiado dentro de un bucle `while`. Si la entrada es inválida, se muestra aviso pedagógico y se restaura el flujo sin caída de la JVM.
* **Plan para RSK-02 (Bucles infinitos):** Incorporación de contadores de seguridad (*guard clauses*) con límite de intentos y depuración paso a paso en IntelliJ IDEA inspeccionando variables centinela.
* **Plan para RSK-03 (Desviación en cronograma):** Priorización estricta de requisitos esenciales frente a mejoras cosméticas para salvaguardar la fecha comprometida.

---

## 3.4. Control de calidad y protocolo de incidencias técnicas

### Procedimiento formal de seguimiento
Toda anomalía detectada en fase de pruebas o depuración sigue el ciclo: *Identificada* $\rightarrow$ *Registrada* $\rightarrow$ *En depuración* $\rightarrow$ *Resuelta* $\rightarrow$ *Cerrada*.

### Registro histórico de incidencias del sprint
* **Incidencia INC-01:** Entrada vacía o salto de línea prematuro en la lectura por consola provoca `NoSuchElementException`.
  * **Causa técnica:** Llamada directa a lectura sin comprobación de fin de línea.
  * **Solución aplicada:** Validación de búfer mediante `hasNextLine()` y verificación de cadena no vacía antes de procesar el dato.
  * **Verificación:** Batería de 10 pruebas sucesivas superadas con entradas límite y caracteres no imprimibles.

---

## 3.5. Registro acumulativo de Inteligencia Artificial (Prompt Log)

| Fecha | Herramienta | Objetivo | Prompt resumido | Ajuste crítico aplicado |
| :---: | :---: | :--- | :--- | :--- |
| 13/11/2026 | ChatGPT / Claude | Contrastar estructura de mitigación de riesgos | *"Revisa este plan de contingencia para excepciones en consola Java..."* | Se adaptó la respuesta a las clases estándar disponibles en Java SE 21 sin recurrir a dependencias externas. |
```

---

##### Paso 2. Redacción del guion de la demostración oral (`pi/docs/guion-demo-v03.md`)

1. En la carpeta `azahartech/nombre-equipo/apellidos-nombre/pi/docs/`, crea el archivo `guion-demo-v03.md`.
2. Completa la estructura de exposición cronometrada en **3 minutos**:

```markdown
# Guion de la Sprint Review — Incremento v0.3
**Proyecto:** [nombre de tu proyecto]  
**Ponente:** [tu nombre]  
**Duración límite:** 180 segundos (3 minutos)  
**Fecha de defensa:** 13 de noviembre de 2026  

---

## Minuto 1: Contexto, cronograma y riesgos (00:00 - 01:00)
* **Apertura:** Saludo profesional y presentación del proyecto en el marco de AzaharTech.
* **Hito de planificación:** Mostrar brevemente el cronograma y confirmar que el proyecto cumple con las fechas estimadas para el Sprint 3.
* **Gestión de riesgos:** Explicar cómo se detectó el riesgo de caídas por datos erróneos y la estrategia de mitigación adoptada.

## Minuto 2: Demostración técnica en vivo (01:00 - 02:00)
* **Ejecución en consola:** Lanzar la aplicación desde IntelliJ IDEA.
* **Caso de uso nominal:** Introducir datos válidos y mostrar la respuesta correcta del algoritmo.
* **Caso de prueba límite:** Introducir texto aleatorio o pulsar *Enter* repetidamente.
* **Evidencia de robustez:** Demostrar que el programa no cae, captura la excepción, avisa al usuario y permite reintentar la operación limpiamente.

## Minuto 3: Sinergia técnica y próximos pasos (02:00 - 03:00)
* **Depuración e incidencias:** Explicar cómo el uso de puntos de ruptura en Entornos de Desarrollo permitió resolver la incidencia `INC-01`.
* **Próximo incremento (Sprint 4):** Avanzar el salto hacia la orientación a objetos propia (creación de clases, atributos privados y constructores).
* **Cierre:** Agradecer la atención y quedar a disposición para responder preguntas técnicas.
```

---

##### Paso 3. Cierre al 100 % del Sprint Backlog 3 (`pi/backlog/sprint3-backlog.md`)

1. Abre el archivo `pi/backlog/sprint3-backlog.md`.
2. Verifica que todas las tareas están finalizadas y marca la última tarea de consolidación con `[x]`:

```markdown
# Sprint Backlog 3 — [nombre de tu proyecto]
**Periodo:** 26 de octubre – 13 de noviembre de 2026  
**Responsable:** [tu nombre]  
**Estado general:** Completado al 100 %  

## Objetivo general del Sprint 3
Construir el incremento v0.3: definir la secuenciación temporal y matriz de riesgos en Proyecto Intermodular, dominar el uso de puntos de ruptura y seguimiento de variables en Entornos de Desarrollo, e implementar estructuras de control condicionales y repetitivas robustas en Programación.

---

## Tareas

### Módulo: Proyecto Intermodular (PI)
- [x] T-PI-10: Elaborar la EDT, matriz de dependencias y Diagrama de Gantt (`pi/docs/cronograma.md` o `pi/docs/img/cronograma.png`)
- [x] T-PI-11: Registrar el uso ético de IA (*Prompt Log*) en la planificación temporal
- [x] T-PI-12: Redactar la matriz de riesgos técnicos y planes de contingencia (`pi/docs/riesgos-incidencias.md` o `pi/docs/img/matriz-riesgos.png`)
- [x] T-PI-13: Consolidar el Capítulo 3 de la memoria y ensayar la demo técnica v0.3 (`pi/docs/memoria.md` y `pi/docs/guion-demo-v03.md`)

### Módulo: Entornos de Desarrollo (ED)
- [x] T-ED-08: Diseñar casos de prueba de caja negra aplicando particiones de equivalencia y valores límite
- [x] T-ED-09: Configurar puntos de ruptura (*breakpoints*) condicionales en IntelliJ IDEA para inspección de memoria
- [x] T-ED-10: Documentar el procedimiento formal de recogida y registro de incidencias técnicas en coordinación con PI

### Módulo: Programación (PR)
- [x] T-PR-07: Implementar lógica condicional mediante bloques `if / else if / else` y selector `switch`
- [x] T-PR-08: Construir bucles iterativos controlados (`while`, `for`) para la captura repetitiva de datos
- [x] T-PR-09: Incorporar gestión de excepciones básica con bloques `try-catch` frente a entradas erróneas del usuario
```

---

##### Paso 4. Confirmación, etiquetado visual y sincronización en GitHub

1. En IntelliJ IDEA, abre la ventana de confirmación (`Ctrl + K`).
2. Asegúrate de incluir los archivos modificados y creados:
    * `pi/docs/memoria.md`
    * `pi/docs/guion-demo-v03.md`
    * `pi/backlog/sprint3-backlog.md`
3. Escribe el mensaje de confirmación estandarizado:

```text
docs(pi): consolidar capitulo 3 en memoria, guion de demo oral y cerrar sprint backlog 3 al 100%
```

4. Pulsa en **Commit** (o en la flecha contigua seleccionando únicamente *Commit* para registrar el estado local antes de crear la etiqueta).
5. Crea la etiqueta visualmente desde IntelliJ IDEA:
    * En el menú superior, accede a **Git** $\rightarrow$ **New Tag...** (o abre la pestaña inferior **Git / Log**, haz clic derecho sobre el commit recién creado y selecciona **New Tag...**).
    * En el campo **Tag name**, escribe exactamente: `v0.3`.
    * En el campo **Message**, introduce la descripción del incremento:  
      `Incremento v0.3: Planificacion temporal, matriz de riesgos, estructuras de control y depuracion formal`
    * Haz clic sobre el botón **Create Tag**.
6. Sincroniza el commit y la etiqueta con el repositorio remoto:
    * Abre la ventana de envío de cambios mediante el atajo `Ctrl + Shift + K` (o desde el menú **Git** $\rightarrow$ **Push...**).
    * En la esquina inferior izquierda del diálogo de confirmación, marca la casilla de verificación **Push Tags** (asegurándote de que indica *All* o la etiqueta `v0.3`).
    * Haz clic en el botón **Push**.
7. Accede a tu repositorio en GitHub desde el navegador, entra en la sección **Tags / Releases** para comprobar que la versión `v0.3` aparece publicada y verifica que `memoria.md` muestra los Capítulos 1, 2 y 3 consolidados con todas sus tablas y diagramas visibles.

