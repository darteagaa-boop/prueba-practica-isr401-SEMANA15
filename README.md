# Prueba Práctica — Unidad IV — Ingeniería de Requisitos (ISR-401)

**Estudiante:** Danela Arteaga Alava
**Curso:** 4to "Software A"
**Asignatura:** Ingeniería de Requisitos (ISR-401)
**Docente:** Ing. Gleiston Guerrero, Mg.
**Caso:** Sistema de Gestión de Pedidos

Este repositorio contiene el desarrollo completo de las 10 actividades prácticas
(P1–P10) de la Unidad IV: modelo de clases, diagrama de actividades, máquina de
estados, consistencia entre perspectivas, especificación de requisitos, priorización
MoSCoW, validación por inspección (ISO/IEC/IEEE 29148), pruebas de aceptación,
matriz de trazabilidad y gestión del cambio con línea base.

## Estructura del repositorio

```
.
├── main.tex          # Documento LaTeX principal (contiene P1–P10 y la carátula)
├── figuras/           # Carpeta para imágenes adicionales (si se agregan capturas)
├── main.pdf           # PDF compilado (se genera / se sube ya compilado)
└── README.md          # Este archivo
```

> Nota: los diagramas UML (P1 clases, P2 actividades, P3 máquina de estados) están
> construidos directamente en LaTeX/TikZ dentro de `main.tex`, por lo que no dependen
> de imágenes externas. Si se agregan las capturas del cuestionario del SGA, deben
> colocarse dentro de `figuras/` y enlazarse en la carátula (sección `titlepage` de
> `main.tex`) usando `\includegraphics`.

## Requisitos previos

- Distribución LaTeX con soporte para `pdflatex` (por ejemplo, **TeX Live** 2022 o
  posterior, o **MiKTeX**).
- Paquete de idioma español para `babel` (`texlive-lang-spanish` en distribuciones
  basadas en Debian/Ubuntu).
- Paquetes: `tikz`, `booktabs`, `longtable`, `hyperref`, `fancyhdr`, `titlesec`,
  `geometry`, `enumitem`, `amssymb` (incluidos en cualquier instalación completa de
  TeX Live, p. ej. `texlive-full` o `texlive-latex-extra` + `texlive-lang-spanish`).

## Instrucciones de compilación

1. Clonar el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   cd <NOMBRE_DEL_REPOSITORIO>
   ```
2. Compilar el documento con `pdflatex` (se ejecuta dos veces para generar
   correctamente el índice/tabla de contenidos):
   ```bash
   pdflatex -interaction=nonstopmode main.tex
   pdflatex -interaction=nonstopmode main.tex
   ```
3. El PDF resultante se genera como `main.pdf` en la raíz del repositorio.

### Instalación rápida de dependencias (Ubuntu/Debian)

```bash
sudo apt-get update
sudo apt-get install -y texlive-latex-base texlive-latex-extra \
    texlive-lang-spanish texlive-pictures texlive-fonts-recommended
```

## Archivo principal

- **Archivo principal:** `main.tex`
- **Compilador:** `pdflatex`
- **Orden de compilación:** `pdflatex main.tex` (×2, para resolver referencias
  cruzadas y la tabla de contenidos)
- **Dependencias:** ver sección de requisitos previos arriba.

## Contenido del documento (`main.tex`)

| Sección | Actividad |
|---|---|
| Carátula | Datos de identificación, URL del repositorio, capturas del cuestionario SGA |
| P1 | Diagrama de clases UML (Cliente, Pedido, LíneaPedido, Producto) |
| P2 | Diagrama de actividades UML — "Registrar pedido" |
| P3 | Máquina de estados UML del ciclo de vida de un Pedido |
| P4 | Consistencia entre las tres perspectivas + corrección de inconsistencia |
| P5 | Especificación de requisitos (2 RF + 2 RNF) con esquema de atributos |
| P6 | Priorización MoSCoW |
| P7 | Validación por inspección (ISO/IEC/IEEE 29148): defectos + retrabajo |
| P8 | Pruebas de aceptación trazadas |
| P9 | Matriz de trazabilidad (fuente, modelos, pruebas, dependencia horizontal, huérfanos) |
| P10 | Gestión del cambio (SC-01), decisión CCB y declaración de línea base 1.1 |

## Licencia / uso académico

Trabajo desarrollado con fines académicos para la asignatura Ingeniería de
Requisitos (ISR-401), Universidad Técnica Estatal de Quevedo.
