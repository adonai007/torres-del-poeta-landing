# Guía de Publicación en Vercel - Torres del Poeta

Este proyecto es una página web estática (HTML/CSS/JS) optimizada, por lo que su despliegue en Vercel es extremadamente sencillo y gratuito.

## Requisitos Previos

1. Una cuenta en [Vercel](https://vercel.com) (puedes registrarte con tu GitHub).
2. Tener este código en un repositorio de GitHub (Recomendado).

## Opción 1: Publicar desde GitHub (Recomendada)

Esta opción permite que cada vez que hagas un cambio y lo subas a GitHub, la página se actualice automáticamente.

1. **Sube este proyecto a GitHub:**
   - Crea un **nuevo repositorio** en GitHub (puede ser público o privado).
   - Sigue las instrucciones de GitHub para subir el código existente:
     ```bash
     git remote add origin https://github.com/TU_USUARIO/torres-del-poeta.git
     git branch -M main
     git push -u origin main
     ```

2. **Conecta Vercel:**
   - Ve a tu Dashboard en [https://vercel.com/dashboard](https://vercel.com/dashboard).
   - Haz clic en **"Add New..."** button > **Project**.
   - Selecciona **"Import"** al lado del repositorio `torres-del-poeta` que acabas de crear.

3. **Configura el Proyecto:**
   - **Framework Preset:** Déjalo en `Other` (Vercel detectará que es HTML estático).
   - **Root Directory:** Déjalo en `./` (por defecto).
   - Haz clic en **"Deploy"**.

¡Listo! Vercel te dará una URL (ej: `torres-del-poeta.vercel.app`) en menos de un minuto.

## Opción 2: Publicar manualmente (Vercel CLI)

Si no quieres usar GitHub y prefieres subirlo directamente desde tu computadora:

1. Instala Vercel CLI (necesitas Node.js instalado):
   ```bash
   npm i -g vercel
   ```

2. Desde la carpeta del proyecto (`c:\PRODUCTION\45_web_depto`), ejecuta:
   ```bash
   vercel
   ```

3. Sigue las instrucciones en la terminal:
   - *Set up and deploy?* **Yes**
   - *Which scope?* **Selecciona tu cuenta**
   - *Link to existing project?* **No**
   - *Project name?* **torres-del-poeta** (o el que gustes)
   - *In which directory?* **./** (enter)
   - *Want to modify settings?* **No**

El sistema subirá los archivos y te dará una URL de producción inmediata.

---

## Archivos Importantes

- `index.html`: La estructura y contenido.
- `styles/main.css`: Estilos personalizados (si los hubiera en el futuro, actualmente integrados).
- `images/`: Carpeta con todas las fotos HD optimizadas.

## Dominio Personalizado

Si tienes un dominio (ej: `torresdelpoeta.com`):
1. Ve al proyecto en Vercel > **Settings** > **Domains**.
2. Escribe tu dominio y haz clic en **Add**.
3. Vercel te dará unos registros DNS (tipo A o CNAME) para que los configures en tu proveedor de dominio (GoDaddy, Namecheap, etc.).
