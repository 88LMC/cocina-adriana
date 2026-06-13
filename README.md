# 🌮 Mi Cocina Diaria — Adriana

App de nutrición infantil para Frida (10) y Emiliano (6) en Costa Rica.

## Deploy en Vercel (5 minutos)

### 1. Subir a GitHub
- github.com → New repository → `cocina-adriana`
- Arrastra los 3 archivos (`index.html`, `vercel.json`, `api/chat.js`)
- Commit changes

### 2. Conectar Vercel
- vercel.com → Add New Project → Import desde GitHub
- Selecciona `cocina-adriana` → **antes de hacer Deploy**:

### 3. Agregar la API Key (importante)
En Vercel, antes de hacer Deploy:
- Ve a **Environment Variables**
- Name: `ANTHROPIC_API_KEY`
- Value: `sk-ant-api03-...` (tu key de console.anthropic.com)
- Click **Add** → luego **Deploy**

Listo. La key nunca aparece en el código ni en GitHub.

## Personajes

| Personaje | Estilo |
|-----------|--------|
| 🤙 El Brayan | Chilango de barrio, puro slang CDMX |
| 💅 Pao | Fresa regia, súper positiva |
| 🌻 Mary | Mexicana normal, cálida como tía |
| 🎩 Don Finísima Persona | Purista dramático y florido |

## Estructura

```
cocina-adriana/
  index.html      ← App completa (sin key)
  vercel.json     ← Routing
  api/
    chat.js       ← Proxy serverless → Anthropic
```

## Stack
- HTML/CSS/JS puro — sin dependencias ni build step
- Claude Sonnet 4.6 via función serverless de Vercel
- LocalStorage para persistencia en el dispositivo
