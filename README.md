# iac-lab01

Tenemos código de una aplicación web.
Se compone por un archivo HTML que tiene como contenido: WEB01

Quiero poder publicar esta web, especificamente una sola copia como primera instancia

TAREA:
- Desplegar dos web, mostrar Web01, y Web02 como contenido
- Los puertos deben estar configurados en 4000 y 4001
- Gestionar carpetas para orden
- Hacer uso de Gitflow/Conventional Commits

# Construcción de imágenes
docker build -t lab/web01 ./src/web01
docker build -t lab/web02 ./src/web02
# Ejecución de contenedores
docker run -d -p 4000:80 lab/web01
docker run -d -p 4001:80 lab/web02
# Acceso a las aplicaciones
Web01 → http://localhost:4000
Web02 → http://localhost:4001