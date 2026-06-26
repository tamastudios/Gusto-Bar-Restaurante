# Gusto Bar Restaurante — web

Web de una sola página (`index.html`), sin dependencias ni build: se abre en el navegador y funciona. Basada en la plantilla de restaurante del estudio, con datos reales de Gusto Bar Restaurante (Plaça Augusta, 2, Sant Cugat del Vallès).

## Códigos de acceso al panel (`#admin` en la URL)

| Código | Rol | Acceso |
|---|---|---|
| `gusto2026` | Administrador | Todo el panel |
| `santcugat2026` | Dueño | Solo menú del día |

**Cámbialos desde Panel → General antes de publicar la web.**

## Pendiente antes de publicar

1. **Precios de la carta**: se han dejado en blanco a propósito (no se han inventado). Complétalos desde Panel → Carta.
2. **Fotos**: el hero, la galería y la foto de "Sobre nosotros" usan imágenes de stock de Unsplash como maqueta. Sustitúyelas por fotos reales del local desde Panel → Galería / Portada / Sobre nosotros.
3. **Logo**: la cabecera usa el nombre "Gusto" en una tipografía manuscrita (Pacifico) para imitar el rótulo de las sillas de la terraza, ya que no se proporcionó el archivo de logo. Si el propietario tiene el logo en alta resolución, se puede sustituir el texto por la imagen real.
4. **Horario**: consolidado a partir de agregadores públicos de restaurantes (no de una fuente oficial del propietario). Confirmar el horario de fin de semana antes de publicar.
5. **WhatsApp**: se ha configurado el mismo número que el teléfono fijo (+34 938 33 95 31). Confirmar que ese número tiene WhatsApp Business activo; si no, cambiarlo desde Panel → Ubicación y contacto.
6. **Menú del día**: la sección existe en el código pero está **desactivada** (no se conocían platos/precio reales). Si el restaurante ofrece menú del día, actívala desde Panel → Secciones visibles y rellena Panel → Menú diario.
7. **Reseñas**: la valoración (4,3 / 5, +200 opiniones) es la pública de Google a fecha 26/06/2026. No se han inventado citas de clientes — la sección enlaza directamente a las reseñas reales de Google Maps.
8. **Dominio**: el código usa `https://www.gustobarrestaurante.es/` como dominio provisional (canonical, Open Graph, schema.org, sitemap). Sustitúyelo por el dominio real en cuanto se compre.

## Cómo personalizar más adelante

Desde el panel de administración (`#admin`) se puede editar: nombre, portada, carta completa, menú diario, sobre nosotros, galería, horarios, colores, ubicación/contacto y visibilidad de secciones — sin tocar código.

Para cambios de texto fijo en otros idiomas (CA/EN/FR) o en el banner destacado de la terraza, hay que editar el código (buscar `TRANSLATIONS` y `MENU_T`).

## Notas técnicas

- Claves de localStorage con prefijo `gusto_` (no chocan con otras webs de la misma plantilla en el mismo dominio).
- Persistencia en localStorage por defecto; sincronización entre dispositivos opcional vía JSONBin (Panel → General).
- SEO: meta tags, Open Graph, Twitter Cards, schema.org (Restaurant + BreadcrumbList con horarios y valoración real) y `robots.txt` / `sitemap.xml` incluidos.
