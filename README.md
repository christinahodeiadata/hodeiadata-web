# Hodeia Data — Web corporativa

Sitio web de [hodeiadata.es](https://hodeiadata.es) en **modo presentación** durante el periodo de formación de la sociedad. Construido con HTML + Tailwind CSS (CDN) + JavaScript vanilla. Sin formularios activos. Sin cookies de seguimiento. Sin tratamiento de datos personales automatizado.

---

## Estructura del proyecto

```
hodeiadata-web/
├── index.html                  ← Página principal (web pública)
├── aviso-legal.html            ← Aviso Legal (LSSI Art. 10)
├── politica-privacidad.html    ← Política de Privacidad (RGPD)
├── politica-cookies.html       ← Política de Cookies (LSSI Art. 22.2)
├── legal.css                   ← Estilos compartidos páginas legales
├── logo.png                    ← Logo Hodeia Data
├── robots.txt                  ← SEO
├── sitemap.xml                 ← SEO
└── README.md                   ← Este archivo
```

> **Nota:** `_preview.html` es solo para visualización local con el logo embebido. **No subir a GitHub.**

---

## Estado actual de la web

✅ **Modo presentación activado**
- Sin formularios activos (solo email `hola@hodeiadata.es` como CTA principal)
- Sin Google Analytics ni tracking
- Sin Google Fonts (sustituido por Bunny Fonts, compatible RGPD sin tracking de IP)
- Sin cookies propias ni de terceros
- Aviso Legal, Política de Privacidad y Política de Cookies enlazados desde el footer

✅ **Coherente con empresa en formación**
- Identificación legal mínima: "Hodeia Data (en formación)"
- Sin exposición de datos personales de las fundadoras
- Sección "Sobre Hodeia Data" presentando la filosofía sin nombrar personas

✅ **Cumplimiento RGPD / LSSI / AI Act**
- Documentación legal completa según el estado actual del proyecto
- Cuando se constituya la SL, actualizar los 3 documentos legales con datos definitivos

---

# PARTE 1 — Subir a GitHub Pages

## Paso 1 · Crear el repositorio

1. Entrar en [github.com](https://github.com) e iniciar sesión.
2. Pulsar el botón verde **New** o ir a [github.com/new](https://github.com/new).
3. Configurar el repositorio:
   - **Repository name:** `hodeiadata-web`
   - **Description:** `Web corporativa Hodeia Data · IA para auditoría y control interno`
   - **Visibility:** **Public** (obligatorio para GitHub Pages gratuito).
   - **No marcar** ninguna casilla adicional.
4. Clic en **Create repository**.

## Paso 2 · Subir los archivos

**Opción A — Desde la web de GitHub:**

1. En la pantalla "Quick setup" del repositorio, pulsar **"uploading an existing file"**.
2. Arrastrar los 9 archivos (NO subir `_preview.html`).
3. En "Commit changes" escribir: `Primer despliegue web Hodeia Data`.
4. Clic en **Commit changes**.

**Opción B — Desde terminal:**

```bash
cd /ruta/hasta/hodeiadata-web
git init
git add .
git commit -m "Primer despliegue web Hodeia Data"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/hodeiadata-web.git
git push -u origin main
```

## Paso 3 · Activar GitHub Pages

1. En el repositorio, pulsar la pestaña **Settings**.
2. En el menú lateral, buscar **Pages**.
3. **Source:** Deploy from a branch.
4. **Branch:** `main` · Folder: `/ (root)`.
5. Pulsar **Save**.
6. En 1-2 minutos, refrescar y aparece la URL pública.

---

# PARTE 2 — Conectar el dominio hodeiadata.es

## Paso 4 · Configurar el dominio en GitHub

1. En **Settings → Pages**, en **Custom domain** escribir: `hodeiadata.es`
2. Pulsar **Save**.

## Paso 5 · Configurar los DNS

Acceder al panel del registrador del dominio y añadir:

```
TIPO      HOST       VALOR                    TTL
─────────────────────────────────────────────────
A         @          185.199.108.153          Auto
A         @          185.199.109.153          Auto
A         @          185.199.110.153          Auto
A         @          185.199.111.153          Auto
CNAME     www        TU_USUARIO.github.io.    Auto
```

## Paso 6 · Esperar propagación DNS

- Tiempo: 1-4 horas (máximo 48h).
- Cuando esté listo, activar **Enforce HTTPS**.

---

# PARTE 3 — Cuando se constituya la SL

Actualizar los 3 archivos legales con los datos definitivos:

| Archivo | Reemplazar | Por |
|---|---|---|
| `aviso-legal.html` | "Hodeia Data (en formación)" | Hodeia Data, S.L. + datos completos |
| `politica-privacidad.html` | "empresa en proceso de constitución" | Datos del responsable definitivo |

Datos a añadir:
- Denominación social: Hodeia Data, S.L.
- NIF/CIF
- Domicilio social
- Datos registrales (Tomo, Folio, Hoja del Registro Mercantil)

---

# Despachos recomendados para revisión legal RGPD + IA

- **Letslaw** (Madrid)
- **Ecix Group** (Barcelona / Madrid)
- **Audens** (Madrid)
- **Pintos & Salgado** (Madrid)

Presupuesto orientativo: **600-1.500€** la primera revisión.

---

**Hodeia Data · hodeiadata.es · hola@hodeiadata.es**
