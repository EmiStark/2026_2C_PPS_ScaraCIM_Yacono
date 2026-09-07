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

# SCARA CIM

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
Este proyecto **[nombre del proyecto]** (tipo **[PPS/PF]**, **[AÑO] [CUATRIMESTRE]**) resuelve **[problema]** mediante **[solución]**.  
Está orientado a **[público objetivo]** y permite **[beneficio medible]**.  
Se implementa con **[tecnologías clave]** y se valida mediante **[pruebas/mediciones/demo]**.

### Problema
- **Contexto:** [laboratorio / industria / hogar / aula / etc.]
- **Dolor principal:** [qué falla / qué es lento / qué es costoso / qué es riesgoso]
- **Impacto:** [tiempo, costo, errores, seguridad, calidad]

### Solución propuesta
- **Qué hace (features):**
  - [Funcionalidad 1]
  - [Funcionalidad 2]
  - [Funcionalidad 3]
- **Cómo lo hace (alto nivel):** [sensor → control → actuador → visualización]
- **Valor diferencial:** [por qué es mejor / distinto]

### Alcance
**Incluye:**
- [X]
- [Y]

**No incluye (por ahora):**
- [A]
- [B]

### Estado del proyecto
- **Madurez:** [idea / prototipo / MVP / validado]
- **Qué funciona hoy:** [lista corta]
- **Próximos pasos:** [lista corta]

### Demo rápida
- **Video / GIF:** [link o ruta en MULTIMEDIA]
- **Instrucciones express (2 minutos):**
  1) [Paso 1]
  2) [Paso 2]
  3) [Paso 3]

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
