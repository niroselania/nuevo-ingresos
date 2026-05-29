# Consulta de articulos

App HTML estatica para consultar articulos por codigo, color, talle, descripcion, cantidad, precio, UPC o Team.

## Usar en Portainer

Crear un stack o contenedor desde este repositorio usando la imagen construida con el `Dockerfile`.

Puerto interno:

```text
80
```

Ejemplo de `docker-compose.yml` para Portainer:

```yaml
services:
  consulta-articulos:
    build: .
    container_name: consulta-articulos
    restart: unless-stopped
    ports:
      - "8080:80"
```

Luego abrir:

```text
http://IP-DEL-SERVIDOR:8080
```

## Archivos

- `consulta_articulos.html`: app final con los datos embebidos.
- `Dockerfile`: imagen nginx para servir la app.
- `nginx.conf`: configuracion del sitio.
- `generate_app.py`: script usado para regenerar el HTML desde la planilla original.
