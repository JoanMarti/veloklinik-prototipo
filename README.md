# VeloKliniK — Prototipo de mejora UX

Prototipo interactivo para presentar al cliente tres ideas de mejora de experiencia sobre el sitio actual [velo-klinik.ch](https://velo-klinik.ch/).

**Demo pública:** https://joanmarti.github.io/veloklinik-prototipo/

## Las tres ideas

1. **Buscador de servicio interactivo.** Un cuestionario de 3 preguntas (uso de la bici, último servicio, tipo de bici) que recomienda el paquete Bronze, Silver, Gold o Platinum con su precio, en forma de "ticket de diagnóstico", y enlaza a la reserva online.
2. **Sucursales con estado en vivo.** Las tres sedes (Europaallee Zürich HB, Altstetten Zürich y Sattel Schwyz) indican si están abiertas ahora mismo según la hora real del navegador, con botones directos a la ruta y a la reserva.
3. **Proceso y confianza.** Un recorrido de 4 pasos (entrega, presupuesto, reparación, recogida) y un bloque de reseñas para reducir la incertidumbre de dejar la bici en un taller nuevo.

## Características

- Héroe a pantalla completa con foto de taller.
- 4 idiomas: alemán (por defecto), francés, italiano e inglés, con selector en la barra superior.
- Adaptable a móvil.
- Sin dependencias ni proceso de build: un único `index.html` más la carpeta `assets/`.

## Estructura

```
index.html        Página completa (HTML, CSS y JS)
assets/
  hero.jpg        Foto del héroe (referencia)
  europaallee.jpg Foto de la sucursal Europaallee
  altstetten.jpg  Foto de la sucursal Altstetten
  sattel.jpg      Foto de la sucursal Sattel
```

## Ejecutar en local

Basta con abrir `index.html` en el navegador. Para servirlo con un servidor local:

```bash
python3 -m http.server 8000
```

y abrir http://localhost:8000.

## Datos de ejemplo

- Los **paquetes, precios y direcciones** están tomados del sitio actual de VeloKliniK.
- Los **horarios de apertura** de cada sucursal son valores de ejemplo, no los reales.
- Las **reseñas** son textos ficticios etiquetados como ejemplo; hay que sustituirlas por reseñas reales de Google.
- Las **fotos** son imágenes de referencia visual para el prototipo. La del héroe es de otro taller y las de las sucursales proceden de Google Maps o de capturas de pantalla, así que deben sustituirse por fotos propias de VeloKliniK antes de una publicación final.

## Publicación

El sitio se sirve con GitHub Pages desde la rama `main`, carpeta raíz.
