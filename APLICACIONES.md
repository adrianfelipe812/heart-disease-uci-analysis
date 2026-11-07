# Aplicación de este conocimiento en otras áreas

Este proyecto no es solo sobre cardiología: es un ejercicio de **calidad de datos, tratamiento de faltantes y análisis descriptivo riguroso**, que es la base de cualquier proyecto analítico. Estas son algunas formas de llevarlo a otros contextos.

## Habilidades que se transfieren

| Habilidad del proyecto | Para qué sirve en general |
|---|---|
| Detectar faltantes no aleatorios por fuente (centro clínico) | Identificar sesgos cuando los datos vienen de varias sucursales, sistemas o regiones |
| Convertir valores imposibles (colesterol = 0) en faltantes | Limpiar códigos centinela: edades de 999, precios en 0, fechas 1900-01-01 |
| Imputación Hot Deck | Completar encuestas, historiales de clientes o censos sin inventar valores extremos |
| Estadística descriptiva por grupo | Comparar segmentos de clientes, productos o regiones |
| Comunicar limitaciones | Evitar que un hallazgo descriptivo se lea como causal en una decisión de negocio |

## Ejemplos por sector

- **Salud y aseguradoras.** Perfilar pacientes o afiliados por nivel de riesgo, auditar la calidad de historias clínicas entre IPS y preparar datos para modelos de riesgo cardiovascular o de siniestralidad.
- **Banca y fintech.** Las solicitudes de crédito tienen campos faltantes que dependen del canal (app, oficina, aliado). El mismo diagnóstico por fuente evita que el modelo de scoring aprenda el canal en lugar del riesgo.
- **Retail y consumo.** Datos de ventas consolidados de varias tiendas con sistemas distintos: tiendas que reportan 0 cuando en realidad no reportan, imputación de inventarios, comparación de categorías.
- **Encuestas y sector público.** Encuestas de hogares o de satisfacción con preguntas no respondidas; Hot Deck es una técnica estándar en institutos de estadística.
- **Recursos humanos.** Análisis de rotación o clima laboral con encuestas incompletas, comparando áreas o sedes.

## Cómo se adaptaría

1. Reemplazar `num` por la variable de interés (mora, abandono, compra, rotación).
2. Repetir el diagnóstico de faltantes **por fuente de origen** antes de cualquier modelo.
3. Mantener la separación entre análisis descriptivo y conclusiones causales.
4. Si el objetivo es predecir, el siguiente paso natural es un modelo de clasificación con imputación múltiple y validación cruzada.
