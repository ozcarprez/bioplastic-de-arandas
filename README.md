# Bioplastic de Arandas — sitio web

Sitio estático de una sola página (HTML + CSS, sin build ni dependencias) para
**Bioplastic de Arandas**, bolsas y desechables en Tijuana, B.C.

## Contenido

```
index.html      página completa
styles.css      estilos (modo claro y oscuro automáticos)
img/            logotipo en SVG + fotos del local (faltan las fotos)
vercel.json     headers y cleanUrls para el deploy
```

## Datos que muestra el sitio

| Dato        | Valor                                                     |
|-------------|-----------------------------------------------------------|
| Dirección   | Calle Contadores 2227, Otay Universidad, Tijuana, B.C.     |
| Teléfono    | 664 682 0211                                              |
| Celular     | 663 323 5406 (también WhatsApp)                            |
| Horario     | Lun–Vie 8:30 am – 4:30 pm · Sáb 8:30 am – 1:00 pm          |
| Referencia  | "Somos los que estábamos a un costado de la Tortillería Tijuana" |

## Logotipo

Está vectorizado en SVG, así que escala sin pixelarse y se puede recolorear:

- `img/logo.svg` — logotipo completo, verde (para fondos claros)
- `img/logo-blanco.svg` — logotipo completo, blanco (para fondos oscuros)
- `img/emblema.svg` y `img/emblema-blanco.svg` — solo la maceta, para el favicon y redes

## Fotos pendientes

Coloque los archivos en `img/` **con estos nombres exactos**:

- `fachada.jpg` — foto de la esquina / fachada del local.
- `local.jpg` — foto del interior con la mercancía.

No hay que tocar el HTML: en cuanto los archivos existan, aparecen solos.

## Ver la página en la computadora

Las rutas son relativas, así que se puede abrir `index.html` directo en el
navegador. Para que el mapa y las fuentes carguen igual que en producción,
mejor levante un servidor local:

```bash
npx -y serve .
```

## Publicar en Vercel

1. Crear el repositorio en GitHub (vacío, sin README):

   ```bash
   gh repo create bioplastic-de-arandas --public --source=. --remote=origin --push
   ```

   O manualmente: crear el repo en github.com y luego

   ```bash
   git remote add origin https://github.com/USUARIO/bioplastic-de-arandas.git
   git push -u origin main
   ```

2. En [vercel.com/new](https://vercel.com/new) importar el repositorio.
   - Framework Preset: **Other**
   - Build Command: *(vacío)*
   - Output Directory: *(vacío / raíz)*

   Vercel sirve `index.html` tal cual. Cada `git push` vuelve a desplegar.
