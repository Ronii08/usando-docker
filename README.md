# Mi App Docker

Aplicación web hecha con Next.js y contenerizada con Docker.

## Requisitos

- Docker Desktop instalado y corriendo

## Construir la imagen

```bash
docker build -t mi-app-docker .
```

## Ejecutar el contenedor

```bash
docker run -p 3000:3000 mi-app-docker
```

Luego abre http://localhost:3000 en el navegador.

## Detener el contenedor

Presiona `Ctrl + C` en la terminal, o desde otra terminal:

```bash
docker ps
docker stop <ID_DEL_CONTENEDOR>
```

## Detalles técnicos

- Imagen base: `node:20-alpine`
- Multi-stage build (deps, builder, runner)
- Puerto expuesto: 3000
- `.dockerignore` excluye `node_modules`, `.next`, `.env` y archivos temporales

## Autor

Roni Sura