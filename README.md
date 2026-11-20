# Parley Public · Carpeta para Netlify Drop

Esta carpeta contiene los frontends listos para subir a Netlify Drop y obtener una URL pública HTTPS accesible desde cualquier dispositivo (PC, móvil, tablet).

## 📦 Contenido

```
parley-public/
├── index.html                      # Menú principal (página de inicio)
├── Parley_Tata_Iraka_2026-27.html  # Calculadora Smart Money por liga
└── Parley_Linemate_2026-27.html    # Calculadora Smart Money multideporte
```

## 🚀 Cómo subirlo a Netlify (3 minutos)

1. Ve a https://app.netlify.com/drop
2. Arrastra **esta carpeta completa** (`parley-public`) a la zona "Drag and drop your site output folder here".
3. En 5-10 segundos tendrás una URL pública tipo:
   `https://parley-public-abc123.netlify.app`
4. Abre la URL en el navegador del PC y del móvil para verificar.

## ⚙️ Configuración

Los HTML ya están apuntando al backend de Render:

```javascript
window.SM_BACKEND_URL = 'https://tatairaka.onrender.com';
```

Si en el futuro cambias el backend, edita esta línea en ambos HTML y vuelve a subir la carpeta a Netlify.

## 📱 Añadir como app en el móvil

### iPhone (Safari)
1. Abre la URL de Netlify en Safari.
2. Botón Compartir → "Añadir a inicio".

### Android (Chrome)
1. Abre la URL en Chrome.
2. Menú ⋮ → "Añadir a pantalla de inicio".

## 🔗 URLs finales

| Qué | URL |
|---|---|
| Frontend (Netlify) | `https://mis-cuotas.netlify.app` (personalízala) |
| Backend (Render) | `https://tatairaka.onrender.com` |
| Health check | `https://tatairaka.onrender.com/health` |
| Cuota restante | `https://tatairaka.onrender.com/api/quota` |

## ✏️ Personalizar el subdominio de Netlify

Por defecto Netlify te da una URL aleatoria. Para personalizarla:

1. Entra en https://app.netlify.com → tu sitio.
2. Barra lateral → **Domain management** → **Domains**.
3. **Set custom domain** → introduce el nombre que quieras (p. ej. `mis-cuotas`).
4. Tu URL final será `https://mis-cuotas.netlify.app`.

## 🔄 Actualizar los HTML en el futuro

Si modificas los HTML en tu PC:

1. Sustituye los archivos en esta carpeta.
2. Entra en https://app.netlify.com → tu sitio → pestaña **Deploys**.
3. Arrastra la carpeta `parley-public` actualizada a la zona "Drag and drop your site folder here".
4. En 5 segundos, el sitio está actualizado.

## ⚠️ Notas

- El backend en Render free "se duerme" tras 15 min sin actividad. La primera carga puede tardar ~30s (cold start). Las siguientes son instantáneas.
- Los datos provienen de The Odds API (plan free: 500 req/mes). Revisa la cuota restante en el menú principal (`index.html` muestra el estado en tiempo real).
- Para uso informativo. Apuesta con responsabilidad. +18.
