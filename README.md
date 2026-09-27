# OP/ED calificados de ChobyMousepad — Releases

Repositorio público utilizado para distribuir las versiones oficiales de **OP/ED calificados de ChobyMousepad** y alimentar su sistema de actualización automática.

## Canal estable

La aplicación consultará el archivo `latest.json` de la rama `main` para conocer la última versión oficial disponible.

## Flujo de publicación

1. Compilar y probar la nueva versión de Windows x64.
2. Crear una nueva **GitHub Release** con un tag como `v1.0.0`, `v1.0.1`, `v1.1.0`, etc.
3. Adjuntar el ejecutable a la Release.
4. Calcular el SHA-256 del ejecutable.
5. Actualizar `latest.json` con la versión, URL de descarga, SHA-256 y notas.
6. Los clientes instalados detectarán la nueva versión al iniciar o al usar **Buscar actualizaciones**.

## Versionado

- `1.0.1`: correcciones pequeñas.
- `1.1.0`: funciones nuevas compatibles.
- `2.0.0`: cambios mayores o incompatibles.

## Seguridad

El actualizador comprobará el hash SHA-256 antes de reemplazar el ejecutable instalado. Más adelante se puede añadir firma digital de código para reforzar la confianza de Windows/SmartScreen.
