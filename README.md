# Integración del proyecto de Bases de Datos (ETL / Data Mart)

Este repositorio contiene una estructura base para integrar los artefactos de tu trabajo: esquemas SQL, diagramas UML (modelo estrella), scripts ETL para transformar desde la base de staging hacia el Data Mart, scripts de backup y plantillas de pruebas y reportes de calidad.

Estructura propuesta

- sql/
  - staging_schema.sql        -> esquema de la base de datos *staging* (ejemplo)
  - datamart_schema.sql       -> esquema del Data Mart (modelo estrella)
  - sample_data_staging.sql   -> datos de ejemplo para staging
- etl/
  - staging_to_datamart.sql   -> transformaciones ETL (SQL)
  - backup.ps1                -> script de backup (PowerShell, ejemplo)
- uml/
  - star_schema.puml          -> diagramado PlantUML del modelo estrella (editable)
- docs/
  - quality_checks.md         -> checklist y queries para pruebas de calidad
  - quality_report_template.md-> plantilla de informe de calidad
- scripts/
  - run_checks.ps1            -> script para ejecutar checks básicos (ejemplo)
- .gitignore

Cómo usar

1. Reemplaza los placeholders en los scripts SQL con los nombres reales de tus bases/servidores.
2. Si usas PlantUML, instala PlantUML o usa un editor que lo renderice (VSCode + PlantUML extension) para exportar PNG del archivo `uml/star_schema.puml`.
3. Para ejecutar los checks y ETL en Windows: abre PowerShell y adapta las variables al principio de los scripts en `etl/` y `scripts/`.

Si me dices el motor de BD que usas (SQL Server, MySQL, PostgreSQL), ajusto los scripts de backup/ETL para ese motor y puedo ayudarte a volcar tus dumps en el repositorio.
