# Fantasy Chronicle

Crónicas épicas de tu liga de Fantasy Football, generadas con IA.

## Deployment en Vercel

### 1. Instalar Vercel CLI (si no lo tienes)
```bash
npm i -g vercel
```

### 2. Login
```bash
vercel login
```

### 3. Configurar variable de entorno
Ve a https://vercel.com → tu proyecto → Settings → Environment Variables

Agrega:
- **Name:** `ANTHROPIC_API_KEY`
- **Value:** `sk-ant-api03-...` (tu API key de Anthropic)

O por CLI:
```bash
vercel env add ANTHROPIC_API_KEY
```

### 4. Deploy
```bash
vercel --prod
```

## Estructura
```
fantasy-chronicle/
├── api/
│   └── claude.js      # Proxy serverless para Anthropic API
├── public/
│   └── index.html     # App principal
├── package.json
├── vercel.json
└── README.md
```

## Desarrollo local
```bash
# Crear archivo .env.local con tu API key
echo "ANTHROPIC_API_KEY=sk-ant-..." > .env.local

# Correr servidor local
vercel dev
```

## Costos estimados
- Vercel: Gratis (hobby plan)
- Anthropic API: ~$0.01-0.02 por crónica generada

## Funcionalidades
- ✅ Conexión a Sleeper API
- ✅ Múltiples tonos de crónica (Jocoso, Oficial, Dramático, etc.)
- ✅ Text-to-Speech en español
- ✅ Sistema de ratings ELO
- ✅ Exportar crónicas
