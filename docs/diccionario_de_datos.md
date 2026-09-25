# Diccionario de datos

## Identificadores
- **id_real**: `IA-01` a `IA-12` (piezas generadas) y `HU-01` a `HU-13` (corpus humano).
- **id_ciego**: `P01` a `P25`, identificador aleatorio usado durante la codificación.
- **condicion**: `E1` espontánea, `E2` bienintencionada, `E3` informada (texto literal en `instrumentos/prompts/`).

## `datos/condiciones_de_generacion.csv`
Una fila por pieza generada: herramienta, versión visible del modelo, condición, fecha, hora, tipo de cuenta, idioma, ubicación de acceso, orden de ejecución dentro de la herramienta, negativa a generar, archivo de imagen, disponibilidad de transcripción, carpeta de capturas e incidencias.

## `datos/codificacion/verbal_*.csv`
Una fila por pieza. Columnas `M1` y `M2` (sí/no) y `A1`-`D3` con la escala 1 = cumple, 2 = parcial, 3 = incumple, 0 = no aplica. Las recomendaciones se describen en `docs/Patron_referencia.md`.

## `datos/codificacion/visual_*.csv`
Una fila por pieza. `V1_presencia`-`V7_presencia` (0/1) y `V1_peso`-`V7_peso` (0 ausente, 1 accesorio, 2 organiza la composición); `rostros_individualizados` y `siluetas_indiferenciadas` (recuento aproximado); `aparece_persona` (sí/no); `evidencia` (descripción); `incoherencia_geografica` (sí/no) y `nota_incoherencia`. Dominios descritos en `docs/Descriptores_visuales.md`.

## Otros ficheros de `datos/codificacion/`
- `evidencia_verbal_T2.csv`: cita literal que justifica cada valor 2 o 3, y los «no» de M1 y M2.
- `arbitraje.csv`: discrepancias entre T1 (corregida) y T2, propuesta y decisión de la autora.
- `concordancia.csv`: acuerdo simple y kappa por plano.
- `resultados.csv`: indicadores por condición, total de IA y corpus humano, con los valores arbitrados.
- `clave_anonimizacion.csv`: correspondencia entre identificador ciego y real.

## `datos/corpus_humano/corpus_humano.csv`
Organización, título, URL, fecha de publicación y de consulta de cada pieza del corpus de contraste. Las imágenes no se incluyen.

## `datos/capturas/`
Capturas de pantalla de la sesión del 3 de septiembre de 2026, una carpeta por pieza más `00_config_inicial` (comprobación de memoria y personalización desactivadas). El nombre del archivo es la hora de la captura.

## `instrumentos/Rejillas_codificacion.xlsx`
Libro de trabajo completo con todas las hojas del proceso (diseño, prompts, descriptores, registro, corpus, clave, T1, T1 original, T2, concordancia, arbitraje y resultados).
