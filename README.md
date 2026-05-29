# Consulta de articulos

App HTML estatica para consultar articulos por codigo, color, talle, descripcion, cantidad, precio, UPC o Team.

## Funciones

- Busqueda general o por campo especifico.
- Filtros combinados por Team, color, talle y season.
- Vista de detalle original.
- Vista agrupada por codigo, color, talle, Team y descripcion, sumando cantidades e importes.
- Resumen por Team con modelos, cantidad e importe.
- Resumen por color y por talle.
- Indicadores de filas, unidades, articulos unicos, importe total, Teams visibles y Team principal.
- Exportacion CSV de la vista actual.

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
      - "7073:80"
```

Luego abrir:

```text
http://IP-DEL-SERVIDOR:7073
```

## Archivos

- `consulta_articulos.html`: app final con los datos embebidos.
- `Dockerfile`: imagen nginx para servir la app.
- `nginx.conf`: configuracion del sitio.
- `generate_app.py`: script usado para regenerar el HTML desde la planilla original.
