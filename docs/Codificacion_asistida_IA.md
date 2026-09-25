# Codificación asistida por IA, revisión y concordancia

## Procedimiento
Las veinticinco piezas (12 generadas y 13 del corpus humano) se anonimizaron con un identificador aleatorio (P01-P25; semilla 20260903; clave en `datos/codificacion/clave_anonimizacion.csv`) y se codificaron en dos pasadas con asistencia de IA, separadas por catorce días:

| Pasada | Fecha | Modelo | Procedimiento |
|---|---|---|---|
| T1 | 11-9-2026 | Claude Sonnet 5 (Anthropic) | A partir de una lectura previa del material |
| T2 | 25-9-2026 | Claude Opus 5.5 (Anthropic) | Abriendo de nuevo cada pieza anonimizada |

Ninguna de las dos pasadas fue ciega en sentido estricto, porque el asistente tenía acceso a la clave. La autora, Blanca Hernández Pardo, revisó ambas codificaciones y arbitró las veinte discrepancias (`datos/codificacion/arbitraje.csv`); los resultados se calculan con los valores arbitrados.

## Error de atribución en la T1
Durante la revisión se detectó que la T1 visual había descrito dos piezas de IA con el contenido de otras: asignó a P17 (Qwen, E2) la valla y la sección duplicada que pertenecen a P20 (Gemini, E1), y a P04 (Copilot Designer, E2) la ausencia de figuras humanas y las erratas que pertenecen a P17. Se conservan las dos versiones:

- `visual_T1_ClaudeSonnet5_original.csv`: la T1 tal como se hizo.
- `visual_T1_ClaudeSonnet5_corregida.csv`: con las filas P04, P17 y P20 corregidas el 25-9-2026.

Las dos pasadas difieren en el modelo y en el procedimiento, por lo que el error no puede atribuirse solo al modelo.

## Concordancia (acuerdo simple y kappa de Cohen)

| Plano | Casillas | Acuerdo | Kappa |
|---|---|---|---|
| Verbal (18 recomendaciones) | 450 | 97,8 % | 0,77 |
| Visual, presencia (T1 original) | 175 | 95,4 % | 0,85 |
| Visual, peso (T1 original) | 175 | 93,7 % | 0,80 |
| Visual, presencia (T1 corregida) | 175 | 97,7 % | 0,92 |
| Visual, peso (T1 corregida) | 175 | 96,0 % | 0,87 |

La concordancia mide la estabilidad de la codificación asistida, no la fiabilidad entre codificadores humanos independientes.
