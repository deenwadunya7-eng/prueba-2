# DeclarIA — MVP listo para desplegar

Landing + páginas legales + banner de cookies + checkout Stripe + endpoints IA/OCR.
Despliegue recomendado: **Vercel**.

## 🚀 Deploy en Vercel
1. Crea un repo nuevo en GitHub y sube todo este proyecto.
2. Entra a https://vercel.com/new e importa tu repo.
3. Variables de entorno (Project Settings → Environment Variables):
   - `NEXT_PUBLIC_APP_URL` → tu dominio (p. ej. https://declaria.vercel.app)
   - `OPENAI_API_KEY` → tu clave
   - `STRIPE_SECRET_KEY` y `STRIPE_WEBHOOK_SECRET`
   - `PRICE_BASIC_ID`, `PRICE_PRO_ID`, `PRICE_PREMIUM_ID` (de tus productos en Stripe)
4. Deploy.

## ▶️ Scripts
- `npm run dev` → entorno local
- `npm run build` → build de producción
- `npm start` → servidor de producción

## 🧠 IA
- `/api/ai/answer` → chat IA con prompt fiscal español
- `/api/docs/generate` → contrato de servicios

## 🧾 OCR
- `/api/invoices/parse` → subir factura (form-data: `file`)

## 💳 Stripe
- `/checkout` → botones → `/api/stripe/checkout`
- Webhook en `/api/webhooks/stripe`

## ⚖️ Legal
- `/terminos`, `/privacidad`

## 🍪 Cookies
- Banner con consentimiento y centro de preferencias `/ajustes-privacidad`

## 🛡️ Nota
Este MVP es de demostración. Revisa textos legales y seguridad antes de producción.
