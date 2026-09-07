![Logo Institucional](https://github.com/JonatanBogadoUNLZ/PPS-Jonatan-Bogado/blob/9952aac097aca83a1aadfc26679fc7ec57369d82/LOGO%20AZUL%20HORIZONTAL%20-%20fondo%20transparente.png)

# UNLZ — Facultad de Ingeniería (Plantilla de Proyecto)
## Ingeniería Mecatrónica — README + estructura estándar

Este repositorio es una **PLANTILLA**.  
Los estudiantes deben **usar este repo como base** (fork o “Use this template”) y **reemplazar los textos entre corchetes** `[ ... ]` con la información real de su proyecto.

---

## 📛 Naming del repositorio (OBLIGATORIO)

El nombre del repositorio debe seguir este esquema:

**`ANIO_CUATRIMESTRE_TIPO_PROYECTO_APELLIDOS`**

Donde:
- **ANIO**: año de cursada (ej. `2026`)
- **CUATRIMESTRE**: `1C` o `2C`
- **TIPO**: `PPS` o `PF` (Proyecto Final)
- **PROYECTO**: nombre corto *sin espacios* (recomendado: `kebab-case` o `CamelCase`)
- **APELLIDOS**: apellidos de integrantes separados por `_` (sin tildes, sin ñ)

✅ Ejemplos:
- `2026_1C_PPS_ComederoSmart_Salto_Vazquez`
- `2026_2C_PF_MecaChess_Duarte_Diaz`
- `2025_2C_PPS_Escaner3D_DalleRivePrieto_Labreniuk`

> Nota: GitHub **no permite** usar “/” en el nombre del repositorio.  
> Por eso se usa **TIPO = PPS o PF** como campo separado.

---

## 🧩 Cómo usar esta plantilla (estudiantes)

0) **Crear el repo con el nombre correcto (OBLIGATORIO)**  
   Esquema: `ANIO_CUATRIMESTRE_TIPO_PROYECTO_APELLIDOS`

1) Crear tu repositorio desde esta plantilla:
   - Opción A (recomendada): **Use this template** → Create a new repository  
   - Opción B: **Fork**

2) Editar este archivo `README.md` completando todos los campos `[ ... ]`.

3) Subir archivos a las carpetas correspondientes:
   - Código en `CODIGO/`
   - Planos y esquemas en `PLANOS/`
   - Fotos / videos en `MULTIMEDIA/`
   - Datasheets en `DATASHEET/`
   - Informes en `INFORMES/`

---

## ✅ Checklist de entrega
- [ ] Naming correcto del repo: `ANIO_CUATRIMESTRE_TIPO_PROYECTO_APELLIDOS`
- [ ] Título, autores, materia, **tipo (PPS/PF)**, año y cuatrimestre completos
- [ ] Brief completo (one-liner + pitch + problema + solución + alcance + estado)
- [ ] Instrucciones de uso reproducibles (otro puede correrlo)
- [ ] Lista de componentes con cantidades y modelos
- [ ] Esquemáticos/planos adjuntos en `PLANOS/`
- [ ] Fotos / video demostración en `MULTIMEDIA/`
- [ ] Informe PDF en `INFORMES/` (si aplica)

---

# Puesta a punto y programación del robot SCARA del CIM

**Tipo:** PPS  
**Año:** 2026 — **Cuatrimestre:** 2C  

**Carrera:** Ingeniería Mecatrónica  
**Materia / Curso:** Laboratorio de Robótica (CIM)  
**Docente / Cátedra:** GONZÁLEZ, Martín; HIRAK, Matías; FRANCO, Nicolás  
**Autor/es:** YÁCONO, Emiliano — 2008-00310

---

## Introducción / Objetivo

**Contexto:**  
El laboratorio de la facultad dispone de una línea didáctica de montaje automatizado destinada a la formación práctica en el área de automatización y robótica industrial. La línea está compuesta por una cinta transportadora y cuatro robots que intervienen en distintas etapas del proceso, entre ellos un robot SCARA de cuatro grados de libertad encargado de realizar operaciones sobre las piezas ensambladas. En el marco de la presente PPS, se plantea continuar con la puesta a punto y el desarrollo de las funcionalidades de dicho robot, con el objetivo de favorecer su integración en la línea y facilitar su utilización en futuras actividades académicas.

**Problema a resolver:**  
El robot SCARA se encuentra operativo, pero parte de sus programas y funcionalidades no están correctamente documentados, lo que dificulta su uso y continuidad por parte de futuros estudiantes.
En este contexto, se debe desarrollar una secuencia que permita programar las tareas de ensamblaje y control de calidad deseados, estudiar las funcionalidades del robot, sus periféricos y su programación para que el sistema quede listo para futuras intervenciones.

**Objetivo general:**  
Continuar con la puesta a punto del robot SCARA de la línea de montaje del CIM, mediante el desarrollo y programación de las tareas asignadas, buscando lograr su funcionamiento autónomo dentro de la línea y generar la documentación necesaria para facilitar su utilización y futuras intervenciones.

**Objetivos específicos:**
•	Analizar el sistema existente:
Estudiar los programas, rutinas y configuraciones que ya están cargados en el robot para comprender su funcionamiento y determinar cuáles pueden ser reutilizados. 
•	Investigar las funcionalidades del sistema:
Comprender el funcionamiento del lenguaje ACL, el ATS, el Manager, las entradas/salidas y los periféricos asociados al SCARA.
•	Desarrollar la secuencia de trabajo:
Programar la tarea iniciada mediante IN[10], incluyendo la recepción de la pieza, carga de bolillas, traslado a la estación de control de calidad y devolución a la cinta. 
•	Realizar pruebas y puesta a punto:
Ajustar posiciones, movimientos y secuencias para lograr que la tarea se ejecute correctamente de manera autónoma. 
•	Documentar y respaldar el trabajo:
Documentar los programas y procedimientos desarrollados y establecer un sistema de versionado y respaldo mediante GitLab para facilitar la continuidad del proyecto.

---

## Índice
- [Brief](#brief)
- [Descripción técnica](#descripción-técnica)
- [Arquitectura del sistema](#arquitectura-del-sistema)
- [Instrucciones de uso](#instrucciones-de-uso)
- [Tecnologías utilizadas](#tecnologías-utilizadas)
- [Listado de componentes](#listado-de-componentes)
- [Esquemáticos / Planos](#esquemáticos--planos)
- [Fotos / Videos](#fotos--videos)
- [Estructura del repositorio](#estructura-del-repositorio)
- [Autor](#autor)
- [Licencia](#licencia)

---

## Brief

**One-liner (1 frase):**  
[Qué hace el proyecto + para quién + beneficio principal.]
Puesta a punto y programación y documentación del robot SCARA perteneciente a la línea didáctica de montaje automatizado del CIM.

**Elevator pitch (30 segundos):**
Este proyecto Puesta a punto y programación del robot SCARA del CIM (tipo PPS, 2026 2º cuatrimestre) resuelve la falta de documentación y conocimiento sobre parte de los programas y funcionalidades disponibles en el robot mediante el análisis del sistema existente, la investigación de sus herramientas y el desarrollo y puesta a punto de nuevas secuencias de trabajo.
Está orientado a estudiantes y docentes que utilizan el CIM y permite disponer de un robot capaz de ejecutar de manera autónoma las tareas asignadas y de una base documentada para futuras intervenciones.
Se implementa con un robot SCARA Eshed Robotics, el lenguaje ACL, el software ATS, el Manager y los periféricos asociados a la línea de montaje y se valida mediante pruebas de funcionamiento de las secuencias programadas, verificando los movimientos, posiciones y la interacción con los distintos elementos de la estación.

### Problema
- **Contexto:** Laboratorio universitario
- **Dolor principal:** Programas y funcionalidades del SCARA que no están suficientemente identificados, comprendidos o documentados, dificultando su aprovechamiento y continuidad.
- **Impacto:** Mayor dificultad para utilizar, mantener y ampliar el sistema por parte de futuros alumnos.

### Solución propuesta
- **Qué hace (features):**
  - Análisis y clasificación de programas y rutinas existentes.
  - Investigación de las herramientas de programación y periféricos del sistema.
  - Desarrollo de la secuencia JOB01, activada mediante IN[10].
  - Integración de la secuencia con el dispensador de bolitas, el robot cartesiano y la cinta transportadora.
  - Pruebas y ajuste de movimientos y posiciones.
  - Respaldo y versionado de los programas en GitLab.
  - Documentación para facilitar la continuidad del proyecto.
- **Cómo lo hace (alto nivel):** Entrada del Manager → ejecución de programas ACL mediante el controlador → movimiento del robot SCARA y accionamiento de los periféricos → transferencia de la pieza a las distintas estaciones de la línea.
- **Valor diferencial:** El proyecto no se limita a desarrollar una nueva secuencia de funcionamiento, sino que busca recuperar, organizar y documentar el conocimiento asociado al robot y sus funcionalidades, facilitando su reutilización y la continuidad de futuros trabajos realizados por estudiantes.

### Alcance
**Incluye:**
- Relevamiento y análisis de los programas, rutinas y funcionalidades existentes en el robot SCARA.
- Investigación y utilización del lenguaje ACL, ATS, Manager y los periféricos asociados.
- Desarrollo, programación y puesta a punto de la secuencia JOB01, incluyendo la interacción con el dispensador de bolillas, el robot cartesiano y la cinta transportadora.
- Realización de pruebas para verificar el funcionamiento autónomo de la secuencia desarrollada.
- Documentación de los programas, procedimientos y funcionalidades estudiadas.
- Respaldo y versionado de los programas desarrollados mediante GitLab.

**No incluye (por ahora):**
- Desarrollo de las tareas correspondientes a JOB02, JOB03 y JOB04.
- Implementación definitiva del sistema de control de calidad mediante la cámara.
- Puesta en funcionamiento completa de la línea de montaje, ya que existen otros trabajos en desarrollo sobre los demás robots y estaciones.
- Desarrollo de funcionalidades que excedan las tareas asignadas para la presente PPS.

### Estado del proyecto
- **Madurez:** Prototipo funcional en desarrollo
- **Qué funciona hoy:**
  - Robot SCARA operativo y capaz de ejecutar movimientos programados.
  - Comunicación entre el PC, ATS, controlador y robot.
  - Activación de tareas mediante las entradas del Manager.
  - Secuencia JOB01 en desarrollo, incluyendo la manipulación de la pieza y la carga de bolillas.
  - Interacción con el dispensador de bolitas y el robot cartesiano.
  - Posicionamiento de la pieza en la estación destinada al control de calidad.
- **Próximos pasos:**
  - Completar la programación y puesta a punto de JOB01.
  - Realizar pruebas de funcionamiento autónomo de la secuencia.
  - Continuar investigando y documentando las funcionalidades y programas existentes.
  - Respaldar y versionar los programas desarrollados en GitLab.
  - Documentar los procedimientos para facilitar la continuidad del proyecto.
  - Evaluar la puesta en funcionamiento de la cámara para el control de calidad.

### Demo rápida
- **Video / GIF:** [Demostración de JOB01](Multimedia/SCARA_CIM_JOB01.mp4)
- **Instrucciones express (2 minutos):**
  1) Encender el controlador del robot SCARA y establecer la comunicación con el PC mediante el software ATS.
  2) Preparar una pieza ensamblada en la cinta transportadora y activar la entrada IN[10] del Manager para iniciar la secuencia JOB01.
  3) Verificar que el SCARA recibe la pieza, realiza la carga de bolillas, la traslada a la estación de control de calidad y finalmente la devuelve a la cinta transportadora.

---

## Descripción técnica
[Explicación técnica del funcionamiento, decisiones de diseño y consideraciones.]

---

## Arquitectura del sistema

**Entradas (sensores / señales):**
- [Sensor 1]
- [Sensor 2]

**Procesamiento / Control:**
- [Microcontrolador / PC / algoritmo / lógica]

**Salidas (actuadores / señales):**
- [Actuador 1]
- [Actuador 2]

**Interfaz (si aplica):**
- [Pantalla / dashboard / app / web]

> (Opcional) Insertar diagrama:
![Diagrama de bloques](PLANOS/diagrama_bloques.png)

---

## Instrucciones de uso

### Requisitos previos
- [Software / IDE]
- [Drivers / librerías]
- [Hardware mínimo]

### Instalación / Puesta en marcha
1) [Clonar / descargar]
2) [Instalar dependencias]
3) [Cargar firmware / ejecutar]
4) [Validar funcionamiento]

### Uso
- **Modo normal:** [cómo se usa]
- **Calibración (si aplica):** [pasos]
- **Notas:** [cuidados, recomendaciones]

### Troubleshooting (opcional)
- **Problema:** [X] → **Solución:** [Y]
- **Problema:** [X] → **Solución:** [Y]

---

## Tecnologías utilizadas
- **Robótica / Control:** [Arduino / ESP32 / Raspberry / etc.]
- **Electrónica:** [sensores / drivers / etc.]
- **Programación:** [C/C++ / Python / etc.]
- **Plataformas / Tools:** [ROS / OpenCV / etc.]
- **IA (si aplica):** [modelo / técnica]

---

## Listado de componentes

| Componente | Cantidad | Modelo / Especificación | Función |
|---|---:|---|---|
| [Componente 1] | [1] | [Modelo] | [Función] |
| [Componente 2] | [2] | [Modelo] | [Función] |
| [Componente 3] | [1] | [Modelo] | [Función] |

---

## Esquemáticos / Planos
- [Plano/Esquemático 1] → `PLANOS/[archivo]`
- [Plano/Esquemático 2] → `PLANOS/[archivo]`

---

## Fotos / Videos
- Foto 1 → `MULTIMEDIA/[archivo]`
- Foto 2 → `MULTIMEDIA/[archivo]`
- Video demo → `MULTIMEDIA/[archivo]` o [link]

---

## Estructura del repositorio
- `CODIGO/` — Código fuente del proyecto.
- `MULTIMEDIA/` — Imágenes y videos.
- `PLANOS/` — Esquemáticos y diagramas.
- `DATASHEET/` — Hojas de datos y especificaciones.
- `INFORMES/` — Informes, Gantt, manuales, PDFs.

---

## Autor
**[APELLIDO, Nombre]** — [Legajo]  
Contacto (opcional): [mail / LinkedIn]

---

## Licencia
[Definir según la cátedra: MIT / uso académico / etc.]

---

## About (descripción corta del repositorio)

Usar este texto (o similar) en el campo **About** de GitHub:

**[PPS | PF] — [Proyecto] — FI-UNLZ — [2026] [1C|2C] — [Apellido1, Apellido2]**
