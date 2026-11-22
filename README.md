# ISR401-ContX

Repositorio del equipo **ContX** para la asignatura **Ingeniería de Requerimientos (ISR-401)**,
Carrera de Software, Facultad de Ciencias de la Computación, Universidad Técnica Estatal de
Quevedo (UTEQ). Período SPA 2026–2027 · 4.º nivel · Paralelo A.

**Docente:** Gleiston Cicerón Guerrero Ulloa, PhD

**Organización del Proyecto Fin de Curso:** Taller JC|cell, cantón Quevedo, Los Ríos.

## Integrantes

| Integrante | Rol en el equipo |
|------------|------------------|
| Alvarez Rubio Rai Eduardo | Análisis y documentación |
| Holguin Mendoza Jonathan Alexander | Validación y trazabilidad |
| Basurto Anchaguano Jordan Steven | Coordinación y elicitación |

## Índice de carpetas

| Carpeta / archivo | Contenido |
|-------------------|-----------|
| [`PFC/E1/`](PFC/E1/) | **TA-PFC-E1**: visión, alcance, partes interesadas, contexto y plan de elicitación |
| [`PFC/E1/main.tex`](PFC/E1/main.tex) | Documento principal de la entrega 1 |
| [`PFC/E1/main.pdf`](PFC/E1/main.pdf) | PDF compilado de la entrega 1 |
| [`PFC/E1/referencias.bib`](PFC/E1/referencias.bib) | Referencias BibTeX (estilo IEEE) |
| [`PFC/E1/secciones/`](PFC/E1/secciones/) | Una sección del documento por archivo `.tex` |
| [`PFC/E1/instrumentos/`](PFC/E1/instrumentos/) | Guion de entrevista, cuestionario, guía de observación y modelo de consentimiento |
| [`PFC/E1/modelos/`](PFC/E1/modelos/) | Fuentes editables (TikZ) del diagrama de contexto y la matriz poder–interés |
| [`PFC/E1/figuras/`](PFC/E1/figuras/) | Imágenes exportadas y capturas anonimizadas |
| [`PFC/E1/evidencias/MANIFIESTO.md`](PFC/E1/evidencias/MANIFIESTO.md) | Registro (nombre, fecha, duración, SHA-256) de las evidencias privadas |
| [`entrega-sga/`](entrega-sga/) | Fuente del PDF de una página que se sube al SGA |

```
ISR401-ContX/
├── README.md
├── .gitignore
├── entrega-sga/
│   └── TA-PFC-E1-sga.tex
└── PFC/
    └── E1/
        ├── main.tex
        ├── main.pdf
        ├── referencias.bib
        ├── secciones/      01-introduccion.tex … 10-declaracion-ia.tex
        ├── instrumentos/   guion-entrevista.tex, cuestionario.tex,
        │                   guia-observacion.tex, consentimiento-informado.tex
        ├── modelos/        diagrama-contexto.tex, matriz-poder-interes.tex
        ├── figuras/
        └── evidencias/     MANIFIESTO.md
```

## Compilación

### Dependencias

- Distribución LaTeX: **TeX Live 2023+** (Linux/macOS) o **MiKTeX 23+** (Windows).
  También compila en **Overleaf** (compilador pdfLaTeX).
- Compilador: **pdfLaTeX**. Bibliografía: **BibTeX** con el estilo **`IEEEtran.bst`**
  (paquete `ieeetran`, incluido en TeX Live y MiKTeX).
- Paquetes LaTeX usados: `inputenc`, `fontenc`, `lmodern`, `babel` (spanish), `geometry`,
  `fancyhdr`, `setspace`, `graphicx`, `booktabs`, `tabularx`, `longtable`, `array`, `multirow`,
  `xcolor`, `enumitem`, `caption`, `float`, `amssymb`, `tikz`, `hyperref`, `url`.
  MiKTeX los instala automáticamente la primera vez; en TeX Live vienen con `scheme-full`
  (o instalar con `tlmgr install <paquete>`).
- No se requieren herramientas externas: los diagramas se dibujan con TikZ desde `modelos/`.

### Entrega 1 (`PFC/E1`)

Archivo principal: `PFC/E1/main.tex`. Desde la raíz del repositorio:

```bash
cd PFC/E1
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Orden: **pdflatex → bibtex → pdflatex → pdflatex** (la segunda y tercera pasada resuelven
citas, referencias cruzadas e índices; no deben quedar `??` en el PDF).

Alternativa equivalente con `latexmk`:

```bash
cd PFC/E1
latexmk -pdf main.tex
```

Resultado: `PFC/E1/main.pdf`.

Alternativa con **Tectonic** (requiere acceso a su repositorio de paquetes en la primera
compilación):

```bash
cd PFC/E1
tectonic --untrusted main.tex
```

### PDF para el SGA

```bash
cd entrega-sga
pdflatex TA-PFC-E1-sga.tex
```

Comprobar que el PDF tiene **una sola página** y que la URL cabe en una sola línea.

## Datos personales y evidencias

Ningún dato personal de terceros (cédulas, teléfonos, correos personales, audios, videos o
consentimientos firmados) se publica en este repositorio. Los originales se guardan en la
carpeta institucional privada del equipo y se registran en
[`PFC/E1/evidencias/MANIFIESTO.md`](PFC/E1/evidencias/MANIFIESTO.md) con su huella SHA-256.
