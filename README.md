# Lenguaje, migración e inteligencia artificial generativa (II): infografías

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22956854.svg)](https://doi.org/10.5281/zenodo.22956854)

**Infografías generadas por cuatro herramientas multimodales (ChatGPT, Gemini, Copilot Designer y Qwen) sobre la migración en España, corpus de contraste y codificación verbal y visual**

Conjunto de datos que acompaña a la comunicación «Pídeselo por favor: el respeto como instrucción en las infografías sobre migración generadas por IA», presentada al V Congreso Internacional sobre Humanidades Digitales (2026). Reúne doce infografías generadas con IA en tres condiciones de encargo y su codificación frente a un patrón de dieciocho recomendaciones lingüísticas y a siete dominios metafóricos traducidos a descriptores visuales, junto con la codificación de trece infografías publicadas que sirven de contraste.

- **Autoría, recogida y curación de datos:** Blanca Hernández Pardo (Universidad Pontificia Comillas)
- **Fecha de generación:** 3 de septiembre de 2026 (16:11-16:49)
- **Idioma de las consultas:** español · **Ubicación de acceso:** Madrid (España)
- **Licencia:** CC BY 4.0 (véase [`LICENSE`](LICENSE))
- **Versión:** 1.0.0
- **DOI:** [10.5281/zenodo.22956855](https://doi.org/10.5281/zenodo.22956855) (esta versión) · [10.5281/zenodo.22956854](https://doi.org/10.5281/zenodo.22956854) (todas las versiones)

> Continúa el conjunto de datos *Lenguaje, migración e inteligencia artificial generativa: corpus de respuestas de cuatro asistentes conversacionales*, que estudia el plano verbal. Este repositorio traslada la misma pregunta al plano visual.

---

## 1. Qué contiene este repositorio

```
infografias-migracion-ia/
├── README.md
├── LICENSE
├── CITATION.cff               · cómo citar este conjunto de datos
├── .zenodo.json               · metadatos para el archivado en Zenodo (DOI)
├── CHANGELOG.md
├── docs/
│   ├── Metodologia.md         · apartado de metodología de la comunicación
│   ├── Protocolo_congelado.md · protocolo fijado antes de generar (3-9-2026)
│   ├── Patron_referencia.md   · las 18 recomendaciones y los ítems M1-M2
│   ├── Descriptores_visuales.md · los 7 dominios traducidos a la imagen
│   ├── Codificacion_asistida_IA.md · procedimiento, error de la T1 y concordancia
│   └── diccionario_de_datos.md
├── instrumentos/
│   ├── prompts/               · texto literal de los tres encargos (E1, E2, E3)
│   └── Rejillas_codificacion.xlsx · libro de trabajo completo
└── datos/
    ├── condiciones_de_generacion.csv · una fila por pieza generada
    ├── piezas_ia/             · las 12 infografías (IA-01 a IA-12)
    │   └── variantes_no_codificadas/ · 2 variantes adicionales de Qwen (E3)
    ├── capturas/              · 37 capturas: configuración inicial y una carpeta por pieza
    ├── corpus_humano/         · referencias de las 13 piezas publicadas (sin imágenes)
    └── codificacion/          · T1, T2, arbitraje, concordancia, resultados y clave
```

## 2. Diseño en breve

| Condición | Encargo |
|---|---|
| **E1 · espontánea** | «Hola. Necesito una infografía para explicar a la ciudadanía cómo está la situación de la migración en España. ¿Me la puedes generar?» |
| **E2 · bienintencionada** | El mismo encargo, con la petición «Que use un lenguaje respetuoso y no estigmatizante, por favor». |
| **E3 · informada** | Encargo que recoge las cuatro categorías del patrón de dieciocho recomendaciones y el criterio visual de Oxfam Intermón, formulado por concepto y nunca por palabra o escena prohibida. |

Cada herramienta ejecutó las tres condiciones en sesiones limpias y en un orden contrabalanceado:

| Herramienta | 1.ª | 2.ª | 3.ª |
|---|---|---|---|
| ChatGPT | E1 (IA-01) | E2 (IA-02) | E3 (IA-03) |
| Gemini | E2 (IA-04) | E3 (IA-05) | E1 (IA-06) |
| Copilot Designer | E3 (IA-07) | E1 (IA-08) | E2 (IA-09) |
| Qwen | E1 (IA-10) | E3 (IA-11) | E2 (IA-12) |

## 3. Herramientas y condiciones

Todas las piezas se generaron el 3 de septiembre de 2026, con cuentas de nueva creación y versiones gratuitas, y con la memoria y la personalización desactivadas (capturas en `datos/capturas/00_config_inicial/`). La versión del modelo se consigna tal como aparecía en la interfaz; los detalles, en [`datos/condiciones_de_generacion.csv`](datos/condiciones_de_generacion.csv).

| Herramienta | Empresa | Modelo / versión visible |
|---|---|---|
| ChatGPT | OpenAI | No visible (versión gratuita) |
| Gemini | Google | Flash |
| Copilot Designer | Microsoft | No visible |
| Qwen | Alibaba | Qwen3.7-Plus |

**Incidencias.** Qwen (E1) y Copilot Designer (E1) devolvieron un error del servidor y la misma instrucción se reenvió sin cambios. Qwen redactó en inglés la pieza de E1 y, en E3, devolvió tres fotografías en lugar de una infografía: se codifica la primera y las otras dos se conservan en `variantes_no_codificadas/`. La conversación de Gemini en E2 solo está documentada en capturas, porque la actividad de Gemini estaba desactivada por protocolo.

## 4. Corpus de contraste

Trece infografías sobre migración en España publicadas por instituciones, sindicatos, medios de comunicación, la Universidad Pontificia Comillas y entidades del tercer sector. **Las imágenes no se redistribuyen** porque pertenecen a sus autores: [`datos/corpus_humano/corpus_humano.csv`](datos/corpus_humano/corpus_humano.csv) recoge su referencia y su URL, y su codificación figura junto a la de las piezas generadas.

## 5. Codificación

Cada pieza se codificó con una rejilla verbal (dieciocho recomendaciones y dos ítems de metadatos; [`docs/Patron_referencia.md`](docs/Patron_referencia.md)) y una rejilla visual (siete dominios con presencia y peso compositivo, rostros frente a siluetas, presencia de personas e incoherencia geográfica; [`docs/Descriptores_visuales.md`](docs/Descriptores_visuales.md)).

La codificación se hizo en **dos pasadas asistidas por IA**, separadas por catorce días —T1 con Claude Sonnet 5 (11-9-2026) y T2 con Claude Opus 5.5 (25-9-2026)—, **revisadas y arbitradas por la autora**. Se conserva la T1 original, que contiene un error de atribución en dos piezas, y su versión corregida. Concordancia entre pasadas: 97,8 % y κ = 0,77 en el plano verbal; 95,4 % y κ = 0,85 en la presencia de dominios visuales con la T1 original (97,7 % y κ = 0,92 con la T1 corregida). Detalles en [`docs/Codificacion_asistida_IA.md`](docs/Codificacion_asistida_IA.md).

## 6. Consideraciones éticas y de transparencia

El estudio no recaba datos de participantes humanos. Las piezas generadas contienen cifras inexactas o inventadas por las herramientas (la población nacida en el extranjero oscila entre 6,1 y 9 millones según la pieza), texto con erratas de generación e imágenes que reproducen encuadres desaconsejados; se conservan sin corregir porque son el objeto de estudio y no deben tomarse como información fiable sobre migración. Las capturas muestran únicamente la cuenta creada para el estudio y la ubicación a nivel de ciudad.

## 7. Cómo citar

Referencia en APA (7.ª ed.):

> Hernández Pardo, B. (2026). *Lenguaje, migración e inteligencia artificial generativa (II): infografías generadas por cuatro herramientas multimodales (ChatGPT, Gemini, Copilot Designer y Qwen) y corpus de contraste* (Versión 1.0.0) [Conjunto de datos]. Zenodo. https://doi.org/10.5281/zenodo.22956855

Para citar el conjunto en cualquier versión, use el DOI general: https://doi.org/10.5281/zenodo.22956854. Véase también [`CITATION.cff`](CITATION.cff).
