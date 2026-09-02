# Carrasquilla Aprende

Portal institucional de guías y recursos de aprendizaje de la Institución Educativa Carrasquilla Industrial.

## Fuente de información

El portal consulta automáticamente la hoja pública `DATOS_PORTAL` de Google Sheets. Solo deben publicarse allí los campos destinados a estudiantes y familias:

`NIVEL, GRADO, CURSO, ID_ASIGNATURA, ASIGNATURA, CODIGO, TITULO, TIPO_GUIA, FECHA, URL`

No deben incorporarse nombres de estudiantes, correos, observaciones internas ni datos personales.

## Publicación

El archivo principal es `index.html` y está preparado para GitHub Pages. Cada actualización enviada a la rama principal se publica automáticamente.

El módulo `caracterizacion.html` es una demostración privada por rol con datos anonimizados. Su arquitectura de producción está documentada en `docs/ARQUITECTURA_CARACTERIZACION.md`; no debe conectarse a datos reales mientras el acceso sea exclusivamente del lado del navegador.

## Administración institucional

- Mantener al menos dos propietarios autorizados en la organización de GitHub.
- Activar verificación en dos pasos en todas las cuentas administradoras.
- No compartir contraseñas.
- Conservar privados los archivos de revisión, carga docente y archivo institucional.
