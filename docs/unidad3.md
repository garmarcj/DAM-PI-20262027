# Sprint 3. Cronograma del proyecto

---

## Semana 7. De la especificación a la temporización: descomposición de tareas, secuenciación temporal y apertura del Sprint Backlog 3

---

### Día 7 - 1 sesión

#### Teoría. Planificación temporal, secuenciación y cronograma del proyecto

#### 1. Caso guía en AzaharTech

Es viernes 30 de octubre de 2026 por la tarde en la sede de **AzaharTech Software Consulting** en Castellón de la Plana. Con los dos primeros sprints cerrados y consolidados en GitHub, el equipo de desarrollo inicia el **Sprint 3 (26 oct – 13 nov)**.

En la pantalla principal de la sala, **Laia Claramunt** proyecta una línea de tiempo dividida en semanas e hitos clave. A su lado, **Alba Torres** examina en su portátil los primeros casos de prueba con puntos de ruptura en IntelliJ IDEA, mientras **Pau Ferrer** anota en la pizarra las dependencias técnicas del lector del **IES El Caminàs**.

Laia toma la palabra dirigiéndose al equipo:

> *«Durante los Sprints 1 y 2 transformamos una necesidad del IES El Caminàs en un catálogo estricto de requisitos funcionales y un modelo de bloques en Draw.io. Sabemos con exactitud **qué** debemos construir. Pero un proyecto de software profesional no se gestiona con buenas intenciones: necesita responder a la pregunta que más preocupa al cliente y a dirección: **¿cuándo estará listo y qué tareas dependen de otras?**
>
> Si prometemos al equipo directivo del centro que el control de acceso estará operando sin haber secuenciado las fases de validación, algoritmos de repetición y captura de excepciones, cualquier imprevisto técnico paralizará la entrega.
>
> En este Sprint 3, mientras en Programación implementáis estructuras condicionales, bucles y control de errores con `try-catch`, y en Entornos de Desarrollo aprendéis a depurar paso a paso con puntos de ruptura, en Proyecto Intermodular aprenderemos a descomponer el proyecto en una **Estructura de Desglose del Trabajo (EDT/WBS)**, planificaremos su **Cronograma temporal formal**, identificaremos el **camino crítico** y abriremos el **Sprint Backlog 3** que coordinará nuestras próximas tres semanas de desarrollo»*.

---

#### 2. Planificación, temporización y estimación en ingeniería del software

```text
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        EL CICLO DE PLANIFICACIÓN TEMPORAL (SPRINT 3)                   │
├──────────────────────────┬─────────────────────────────┬───────────────────────────────┤
│ 1. Descomposición (EDT)  │ 2. Estimación y Dependencia │ 3. Cronograma y Seguimiento   │
├──────────────────────────┼─────────────────────────────┼───────────────────────────────┤
│ ¿Qué paquetes de trabajo │ ¿Cuánto tiempo exige cada   │ ¿En qué orden se ejecutan?    │
│ y tareas componen el     │ tarea y qué actividades     │ ¿Cuáles son los hitos clave   │
│ alcance del proyecto?    │ bloquean el inicio de otras?│ (milestones) de entrega?      │
└──────────────────────────┴─────────────────────────────┴───────────────────────────────┘
```

##### A. Descomposición del alcance: Estructura de Desglose del Trabajo (EDT / WBS)
Un requisito funcional complejo no puede abordarse de golpe. En ingeniería del software se utiliza el principio de *«divide y vencerás»* mediante la **EDT (Estructura de Desglose del Trabajo)**:
* **Fases o paquetes de trabajo:** Agrupaciones lógicas de entregables (Análisis, Arquitectura, Codificación del núcleo lógico, Pruebas unitarias, Despliegue).
* **Tareas elementales:** Actividades atómicas que pueden ser asignadas a un único responsable, con un resultado medible y un plazo delimitado (generalmente entre 2 y 8 horas lectivas).
* **Criterio de completitud (Regla del 100 %):** La suma de las tareas desglosadas debe cubrir el 100 % del alcance definido en el catálogo de requisitos, sin omitir ni añadir funcionalidades fuera de contrato.

##### B. Estimación de esfuerzos, dependencias y camino crítico
Una vez listadas las tareas, se deben dimensionar de forma realista:
1. **Estimación de esfuerzo:** Cuantificación del tiempo necesario teniendo en cuenta la complejidad técnica y la curva de aprendizaje (por ejemplo, implementar bucles anidados con validación interactiva).
2. **Dependencias entre tareas (Precedencias):** Determinadas tareas no pueden iniciarse hasta que sus predecesoras hayan concluido con éxito:
    * *Fin a Inicio (FS - Finish to Start):* No se pueden programar las pruebas de depuración sin tener compilada la clase de control.
3. **Identificación de Hitos (Milestones):** Puntos de control temporal con duración cero que marcan la consecución de un logro significativo (por ejemplo: *M1: Aprobación de requisitos*, *M2: Congelación del motor de cálculo v0.3*, *M3: Entrega del prototipo*).

##### C. Representación visual del cronograma: Diagrama de Gantt
El **Diagrama de Gantt** es el estándar de la industria para visualizar la planificación temporal:
* **Eje horizontal:** Representa el avance temporal (sprints, semanas lectivas o jornadas de trabajo).
* **Eje vertical:** Relación secuencial de fases y tareas.
* **Barras de actividad:** Indican la duración y solapamiento entre tareas concurrentes.
* Permite detectar de inmediato si un retraso en una tarea de Programación compromete el cierre del sprint o la entrega de documentación en Proyecto Intermodular.

##### D. Uso ético y profesional de la Inteligencia Artificial en la estimación temporal
En AzaharTech, las herramientas de IA generativa se emplean como soporte analítico para contrastar desgloses de tareas:
* **Uso permitido:** Solicitar a la IA una propuesta de desglose de tareas técnicas para un módulo de software determinado con el fin de no olvidar dependencias ocultas (como la gestión de excepciones numéricas o la configuración de carpetas).
* **Revisión crítica obligatoria:** Ajustar siempre los tiempos sugeridos por la IA a la realidad del calendario lectivo oficial y al ritmo de trabajo del curso. Toda consulta debe ser registrada con su prompt exacto y su valoración técnica en el **Prompt Log**.

---

#### Laboratorio práctico guiado. Cronograma del proyecto y Sprint Backlog 3

Laia Claramunt asigna los objetivos operativos para la sesión de hoy:

> *«Durante los próximos treinta minutos, cada desarrollador va a estructurar la planificación temporal de su proyecto propio de la bolsa de proyectos. Desglosaréis las tareas en fases lógicas, definiréis sus dependencias temporales, fijaréis los hitos en el documento **`cronograma-proyecto.md`** y abriréis el archivo **`sprint3-backlog.md`** para sincronizar los avances entre Programación, Entornos de Desarrollo y Proyecto Intermodular»*.

---

##### Paso 1. Creación del documento de temporización y cronograma (`pi/docs/cronograma-proyecto.md`)

1. Abre tu entorno de trabajo en **IntelliJ IDEA**.
2. Navega hasta la carpeta `pi/docs/` de tu proyecto individual (`azahartech/nombre-equipo/apellidos-nombre/pi/docs/`).
3. Crea un nuevo archivo denominado `cronograma-proyecto.md`.
4. Cumplimenta el documento adaptando la siguiente plantilla corporativa a **tu proyecto elegido de la bolsa de proyectos**:

```markdown
# Planificación temporal y cronograma del proyecto
**Consultora:** AzaharTech Software Consulting  
**Proyecto Seleccionado:** [Nombre de tu proyecto de la bolsa de proyectos]  
**Cliente / Sector:** [Nombre de la empresa o sector profesional]  
**Desarrollador/a:** [Tus apellidos, tu nombre]  
**Fecha:** 30 de octubre de 2026  
**Versión:** 1.0 (Sprint 3)  

---

## 1. Alcance y objetivos de la planificación temporal
El presente documento establece la secuenciación, estimación de esfuerzo y temporización de las tareas necesarias para el desarrollo del proyecto durante el primer trimestre del curso 2026-2027. La planificación se organiza en torno a los sprints metodológicos, alineando la ingeniería de requisitos (PI), el control de calidad y depuración (ED) y el desarrollo de la lógica de control (PR).

---

## 2. Estructura de Desglose del Trabajo (EDT / WBS)
A continuación se detalla la descomposición del proyecto en fases y tareas elementales, indicando su identificador, duración estimada y predecesoras:

| ID Tarea | Fase / Paquete de Trabajo | Descripción Técnica de la Tarea | Horas Est. | Dependencia |
| :---: | :--- | :--- | :---: | :---: |
| **T-01** | Análisis y Requisitos | Definición del problema, mapa de actores y ODS | 3 h | Ninguna |
| **T-02** | Análisis y Requisitos | Catálogo formal de Requisitos Funcionales y No Funcionales | 3 h | T-01 |
| **T-03** | Arquitectura del Sistema | Diagrama de bloques funcional (IPO) y viabilidad técnica | 3 h | T-02 |
| **T-04** | Codificación Base | Implementación de variables, tipos primitivos y Scanner | 8 h | T-03 |
| **T-05** | Codificación Base | Operaciones con objetos estándar (`String`, `Math`) | 8 h | T-04 |
| **T-06** | Lógica de Control | Implementación de menú interactivo y bucles (`while`, `for`) | 10 h | T-05 |
| **T-07** | Lógica de Control | Estructuras de selección y bifurcación (`if-else`, `switch`) | 8 h | T-06 |
| **T-08** | Lógica de Control | Control y tratamiento de excepciones con bloques `try-catch` | 6 h | T-07 |
| **T-09** | Calidad y Pruebas | Depuración con IntelliJ: breakpoints e inspección de memoria | 5 h | T-07 |
| **T-10** | Calidad y Pruebas | Diseño y ejecución de casos de prueba de valores límite | 4 h | T-08, T-09 |
| **T-11** | Planificación y Gestión | Elaboración del cronograma, matriz de riesgos y seguimiento | 6 h | T-02 |
| **T-12** | Consolidación Trimestral | Ensamblaje del dossier técnico y demo v0.3 | 4 h | T-10, T-11 |

---

## 3. Cronograma del proyecto y diagrama de Gantt
Secuenciación de las fases a lo largo de las semanas lectivas del primer trimestre:

```text
Semanas Lectivas:
[S1-S3: 14 Sep - 02 Oct]   [S4-S6: 05 Oct - 23 Oct]   [S7-S9: 26 Oct - 13 Nov]   [S10-S12: 16 Nov - 04 Dic]

Fase 1: Análisis y Requisitos
████████████ (S1-S3)
             
Fase 2: Arquitectura y Modelado
             ████████████ (S4-S6)
                          
Fase 3: Lógica y Control (Sprint 3)
                          ████████████ (S7-S9) [EN CURSO]
                                       
Fase 4: POO y Clases Propias
                                       ████████████ (S10-S12)
```

### Hitos clave (Milestones)
* **Hito 1 (02/10/2026):** *M1 - Incremento v0.1*: Repositorio verificado, análisis formal y primer cálculo secuencial en Java.
* **Hito 2 (23/10/2026):** *M2 - Incremento v0.2*: Catálogo de requisitos validado, proyecto en Maven y uso de clases predefinidas.
* **Hito 3 (13/11/2026):** *M3 - Incremento v0.3*: Algoritmos de control interactivo, captura robusta de errores y depuración formal.
* **Hito 4 (04/12/2026):** *M4 - Congelación v0.4*: Implementación completa de clases propias y cierre previo a evaluación.

---

## 4. Registro ético de uso de Inteligencia Artificial (Prompt Log)
| Fecha | Herramienta | Objetivo de la consulta | Prompt introducido | Revisión crítica y ajuste aplicado |
| :---: | :---: | :--- | :--- | :--- |
| 30/10/2026 | ChatGPT / Claude | Identificar tareas y dependencias para estructuras de control en Java | *"Actúa como jefe de proyectos y genera una lista de 5 tareas atómicas con dependencias para programar un menú con bucles y excepciones..."* | Se adaptaron las tareas para reflejar exactamente las horas lectivas del módulo y las sesiones de depuración en IntelliJ. |
```

---

##### Paso 2. Creación del Sprint Backlog 3 (`pi/backlog/sprint3-backlog.md`)

1. En tu carpeta `azahartech/nombre-equipo/apellidos-nombre/pi/backlog/`, crea el archivo `sprint3-backlog.md`.
2. Define la lista coordinada de tareas para el **Sprint 3 (26 oct – 13 nov)** abarcando los tres módulos:

```markdown
# Sprint Backlog 3 — [Nombre de tu proyecto]
**Periodo:** 26 de octubre – 13 de noviembre de 2026  
**Responsable:** [Tu nombre y apellidos]  

## Objetivo general del Sprint 3
Construir el incremento v0.3: estructurar la planificación temporal mediante el cronograma formal del proyecto, implementar algoritmos de control interactivos robustos con bucles, condiciones y excepciones en Programación, y aplicar técnicas de depuración paso a paso e inspección de variables en Entornos de Desarrollo.

---

## Tareas del Sprint

### Módulo: Proyecto Intermodular (PI)
- [ ] T-PI-10: Elaborar la EDT, secuenciación de tareas y cronograma del proyecto (`pi/docs/cronograma-proyecto.md`) (Semana 7)
- [ ] T-PI-11: Definir la matriz de riesgos técnicos y organizativos con planes de contingencia (Semana 8)
- [ ] T-PI-12: Establecer el protocolo de gestión y registro de incidencias técnicas (Semana 9)
- [ ] T-PI-13: Consolidar el dossier del Sprint 3 y preparar la demo técnica v0.3 (Semana 9)

### Módulo: Entornos de Desarrollo (ED)
- [ ] T-ED-08: Configurar y ejecutar pruebas con puntos de ruptura (*breakpoints*) condicionales en IntelliJ IDEA (Semana 7)
- [ ] T-ED-09: Practicar la navegación paso a paso (*Step Over F8 / Step Into F7*) e inspección del panel de variables (Semana 8)
- [ ] T-ED-10: Diseñar matriz de casos de prueba de valores límite y clases de equivalencia (Semana 9)

### Módulo: Programación (PR)
- [ ] T-PR-07: Implementar menú cíclico mediante estructuras de repetición (`while`, `do-while`, `for`) (Semana 7)
- [ ] T-PR-08: Programar lógica de bifurcación mediante condicionales complejos (`if-else`, `switch`) (Semana 8)
- [ ] T-PR-09: Blindar la entrada de datos frente a fallos de usuario mediante bloques `try-catch` (`InputMismatchException`) (Semana 9)
```

---

##### Paso 3. Confirmación y sincronización en GitHub

1. Abre el panel **Commit** en IntelliJ IDEA (`Ctrl + K`).
2. Verifica que están seleccionados los dos nuevos archivos:
    * `pi/docs/cronograma-proyecto.md`
    * `pi/backlog/sprint3-backlog.md`
3. Redacta el mensaje de confirmación siguiendo el formato de **Conventional Commits**:
```text
docs(pi): elaborar cronograma de fases y tareas y abrir sprint backlog 3
```
4. Haz clic en **Commit and Push** para subir los cambios a la rama principal de tu repositorio en GitHub.
5. Accede a tu repositorio en la web de GitHub y comprueba que tanto la tabla del cronograma como las listas de tareas del nuevo sprint se visualizan correctamente con su formato Markdown maquetado.

