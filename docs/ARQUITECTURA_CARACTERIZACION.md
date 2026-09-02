# Arquitectura prevista para caracterización autorizada

La página `caracterizacion.html` usa Firebase Authentication con Google y Cloud Firestore. Los permisos efectivos se aplican mediante `firestore.rules`, no mediante la interfaz del navegador.

## Requisitos antes de conectar información real

1. Autenticación institucional mediante Google Workspace, Microsoft 365 u otro proveedor aprobado.
2. Autorización aplicada en el servidor, no únicamente mediante filtros de JavaScript.
3. Tabla de asignación `usuario → rol → cursos autorizados`.
4. API que entregue a docentes solamente registros de sus cursos.
5. Vista completa reservada a coordinación y orientación.
6. Registro de accesos, cambios y consultas relevantes.
7. Cifrado en tránsito, copias de seguridad y política de conservación/eliminación.

## Campos mínimos sugeridos para la API

`codigo_anonimo, nivel, grado, curso, conectividad, dispositivo, afectacion_vivienda, estado_emocional, modalidad_viable, necesidad_acompanamiento, estado_envio, actualizado`

La API para docentes no debe devolver documentos de identidad, direcciones, teléfonos, correos ni datos de acudientes. Si coordinación requiere relacionar el código anónimo con una persona, esa relación debe permanecer en una fuente separada, con permisos más restrictivos.

## Sustitución de la fuente demostrativa

La fuente activa es la colección privada `caracterizaciones` de Firestore. El archivo demostrativo no es consultado por el módulo autenticado. No debe publicarse una hoja de cálculo con datos sensibles ni almacenarse información real dentro del repositorio público.
