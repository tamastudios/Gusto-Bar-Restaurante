# Gusto Bar Restaurante — web

Web de una sola página (`index.html`), diseño e implementación propios para este proyecto (sin reutilizar plantillas de otros negocios), sin dependencias ni build: se abre en el navegador y funciona. Datos reales de Gusto Bar Restaurante (Plaça Augusta, 2, Sant Cugat del Vallès).

## Código de acceso al panel (`#admin` en la URL)

| Código | Acceso |
|---|---|
| `gusto2026` | Panel completo |

**Cámbialo desde Panel → General antes de publicar la web.**

## Pendiente antes de publicar

1. **Precios de la carta**: se han dejado en blanco a propósito (no se han inventado). Complétalos desde Panel → Carta.
2. **Fotos**: el hero, la galería y la foto de "Sobre nosotros" usan imágenes de stock de Unsplash como maqueta. Sustitúyelas por fotos reales del local desde Panel → Galería / Portada / Sobre nosotros (solo hace falta pegar la URL de la imagen).
3. **Logo**: la cabecera usa el nombre "Gusto" en una tipografía manuscrita (Caveat) inspirada en el rótulo de las sillas de la terraza, ya que no se proporcionó el archivo de logo. Si tienes el logo en alta resolución, lo sustituimos por la imagen real.
4. **Horario**: consolidado a partir de agregadores públicos de restaurantes (no de una fuente oficial del propietario). Confirmar el horario de fin de semana antes de publicar, desde Panel → Horarios.
5. **WhatsApp**: se ha configurado el mismo número que el teléfono fijo (+34 938 33 95 31). Confirmar que ese número tiene WhatsApp Business activo; si no, cambiarlo desde Panel → Ubicación y contacto.
6. **Reseñas**: la valoración (4,3 / 5, +200 opiniones) es la pública de Google a fecha 26/06/2026. No se han inventado citas de clientes — la sección enlaza directamente a las reseñas reales de Google Maps.
7. **Dominio**: el código usa `https://www.gustobarrestaurante.es/` como dominio provisional (canonical, Open Graph, schema.org, sitemap). Sustitúyelo por el dominio real en cuanto se compre.

## Cómo personalizar más adelante

Desde el panel de administración (`#admin`) se puede editar sin tocar código: nombre, portada, carta completa (categorías y platos), sobre nosotros, galería, horarios, colores y ubicación/contacto.

La web está en un solo idioma (español). Si más adelante se quiere añadir catalán/inglés, hay que avisarlo: implica ampliar el código.

## Notas técnicas

- Una sola página, sin frameworks ni build. Persistencia de los cambios del panel en `localStorage` del navegador (clave `gusto_site_v1`).
- PIN del panel hasheado con SHA-256 + salt; bloqueo de 5 minutos tras 5 intentos fallidos.
- SEO: meta tags, Open Graph, Twitter Cards, schema.org (Restaurant + BreadcrumbList, con horarios y valoración real) y `robots.txt` / `sitemap.xml` incluidos.
- Despliegue automático a GitHub Pages mediante GitHub Actions (`.github/workflows/deploy.yml`) en cada push a `main`.
