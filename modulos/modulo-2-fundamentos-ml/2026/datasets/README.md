# Datasets — Módulo 2 (Fundamentos de ML), edición 2026

Datos usados en los notebooks del módulo. Se publican al repo público
`sebastiancontz/ust-diplomado-ia-modulo-ml` (job `colab` del workflow) y se consumen desde Colab por
URL raw (ver `_plantilla-notebook.ipynb`). **Todos los datos son sintéticos (generados para el curso)
o de uso público.** No se incluyen datos personales, reservados ni de marca.

| Archivo | Origen | Descripción | Usado en |
|---|---|---|---|
| `clientes.csv` | **Sintético** (generado para el curso) | ~2000 clientes de telecom con `fuga` (churn) sí/no. **Desbalanceado a propósito (~18% fuga)** para enseñar por qué el accuracy engaña y para qué sirve la validación estratificada. Columnas: `edad`, `antiguedad_meses`, `plan`, `cargo_mensual`, `llamadas_soporte`, `fuga`. La antigüedad baja y las llamadas a soporte son los predictores fuertes. | Clase 4 (clasificación) |
| `vivienda.csv` | **Sintético** (generado para el curso) | Precios de viviendas (UF) con superficie, comuna, etc. | — (sin uso actual; era candidato para la Clase 3, que finalmente reutiliza `precios_casas_rm.csv`) |
| `precios_casas_rm.csv` | **Uso público** (avisos inmobiliarios de la Región Metropolitana, Chile) | Casas de la RM: área, dormitorios, baños, comuna, cercanía a metro y `precio_uf`. Datos reales, agregados y sin identificadores personales. | Clases 2 y 3 (datos/preparación y regresión) |

## Notas

- **`precios_casas_rm.csv`**: re-guardado en **UTF-8** (la fuente venía en latin-1; afectaba `baños`).
  Los valores de `precio_uf` corresponden a **precio de venta** (no arriendo). Para la práctica de la
  Clase 2 se introducen algunos **valores faltantes de forma deliberada** (documentado en el notebook)
  con el fin de enseñar imputación; el dataset original viene completo.
- Procedencia/licencia de los datos públicos: usar solo con fines **educativos**. Si se conoce la
  fuente original y su licencia, anotarla aquí.
