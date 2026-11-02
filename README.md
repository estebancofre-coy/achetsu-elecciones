# Portal electoral ACHETSU

Portal público e independiente para informar sobre la preparación y el desarrollo del proceso electoral. El sitio institucional `achetsuweb` conserva su propio repositorio y publicación.

## Publicación

El workflow `.github/workflows/deploy-pages.yml` publica `index.html`, `CNAME` y `assets/` en GitHub Pages al actualizar `main`. El dominio configurado para este portal es `elecciones.achetsu.cl`.

## DNS pendiente

En Cloudflare, dentro de la zona `achetsu.cl`, agregar:

| Tipo | Nombre | Destino | Proxy |
|---|---|---|---|
| CNAME | `elecciones` | `estebancofre-coy.github.io` | DNS only (nube gris) |

El registro debe guardarse antes de que GitHub pueda validar el dominio y emitir HTTPS. No activar el proxy de Cloudflare durante la validación inicial.

## Criterios de contenido

- Publicar fechas, requisitos y padrón electoral solo cuando exista información oficial confirmada.
- No publicar instrucciones de pago hasta recibirlas de ACHETSU.
- Los enlaces de padrón y membresía llevan al sitio institucional.
- No copiar el padrón de personas ni otros datos personales a este repositorio.
