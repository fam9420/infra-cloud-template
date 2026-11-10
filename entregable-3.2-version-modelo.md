# Entregable 3.2 - Versionado del modelo

Los pesos del modelo de ejemplo viven dentro de la imagen Docker del servicio
`model`, en `/app/model.joblib`. La version del artefacto se documenta como
`iris-v1` y queda asociada al commit que construye la imagen; futuras versiones
se identifican como `iris-v2`, `iris-v3`, etc., y se publican con el mismo
esquema de tags versionados del pipeline. El servicio selecciona el archivo
mediante la variable de entorno `MODEL_PATH`, cuyo valor por defecto es
`/app/model.joblib`. El archivo se genera una sola vez durante el build y se
carga al iniciar el contenedor.
