# METODO KEYGEN — Web completa (para publicar)

Esta carpeta tiene **todo lo que la web necesita** para funcionar. No falta ningún archivo.

```
WEB-PARA-SUBIR/
├─ index.html                    ← la landing completa
└─ assets/web/
   ├─ alumnas/      (10 fotos de perfil)
   ├─ wins/         (37 capturas de resultados)
   └─ testimonios/  (4 videos + sus miniaturas)
```

El logo, el CSS y el JavaScript están **embebidos dentro del `index.html`**, por eso no hay carpetas de estilos ni de scripts.

Lo único que se carga de internet (no hay que subirlo): las tipografías de Google Fonts, el botón de agendar (Calendly) y el video de presentación (Loom).

---

## Cómo publicarla en Vercel

1. Entrá a **vercel.com** y creá una cuenta (podés entrar con Google o GitHub).
2. **Add New… → Project**.
3. Arrastrá esta carpeta completa (`WEB-PARA-SUBIR`).
4. Framework preset: **Other** (es un sitio estático, no necesita compilación).
5. **Deploy**. En segundos te da una URL pública.

> Para mostrarla, compartí **el link**, no el archivo `.html`. Si se manda el archivo por WhatsApp, se abre en un visor que no ejecuta JavaScript y la animación de entrada queda trabada.

---

## ⚠️ Dos cosas a tener en cuenta antes de subir

### 1. Los videos pesan mucho (la carpeta pesa 415 MB)

Los 4 videos de testimonios suman unos 407 MB:

| Archivo | Peso |
|---|---|
| testimonio-3-ina.mp4 | 145 MB |
| testimonio-2-camila.mp4 | 107 MB |
| testimonio-4-liliana.mp4 | 92 MB |
| testimonio-1-julia.mp4 | 64 MB |

Esto implica que:
- **No se puede subir a GitHub tal cual**: GitHub rechaza archivos de más de 100 MB (dos videos lo superan).
- Servir videos tan pesados desde Vercel hace que la página cargue **muy lenta** en celular.

**Recomendado:** comprimir los videos (se puede bajar a ~30 MB en total sin perder calidad visible) o subirlos a YouTube/Vimeo como "no listados" y embeberlos. Con eso la web queda liviana y carga rápido.

### 2. Falta el video de presentación del hero

En el código, el video principal apunta a `PLACEHOLDER_LOOM_ID`. Hasta que se reemplace por el ID real del Loom, ese recuadro se va a ver vacío.

Está marcado en el `index.html` con el comentario `<!-- PLACEHOLDER: reemplazar PLACEHOLDER_LOOM_ID ... -->`.

---

## Otros pendientes de la landing

- Fix: la animación de intro depende de JavaScript (si el visor no lo ejecuta, queda trabada).
- Fix: la intro no se reproduce si el dispositivo tiene activado "Reducir movimiento".
- Revisar que las capturas de wins no muestren datos personales de clientas (nombres, teléfonos, DNI/CUIT, comprobantes bancarios) antes de publicarlas.
