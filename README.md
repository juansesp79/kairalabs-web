# Kaira Labs — Sitio web corporativo

Sitio web estático de **Kaira Labs SAS** — empresa de IA para el cuidado del adulto mayor.

**Producción:** https://kairalabs.ai
**Deploy preview:** https://kairalabs-web.juan-espinosa.workers.dev

---

## Stack

- HTML + CSS + JS vanilla (sin framework, sin build)
- Cloudflare Workers Assets (deploy vía `wrangler`)
- Fuentes: Google Fonts (Inter)
- Formulario de contacto: Formspree
- Email: Zoho Mail (`juan.espinosa@kairalabs.ai`, alias `privacidad@`, `hola@`)

---

## Estructura

```
kairalabs-web/
├── index.html              # Landing page principal
├── privacidad.html         # Política de tratamiento de datos (Ley 1581/2012)
├── assets/
│   ├── css/style.css       # Estilos (dark premium, variables CSS, responsive)
│   └── img/
│       ├── favicon.svg     # Ícono tab browser (corazón teal)
│       ├── kaira_icon.svg  # Ícono nav + footer (Kaira_Nav_Final)
│       └── kaira_logo_corazon.svg  # Logo grande (1042×923, disponible para uso)
└── wrangler.toml           # Configuración Cloudflare Workers Assets
```

---

## Secciones del sitio

1. **Hero** — propuesta de valor + chat demo animado
2. **El problema** — 3 cards: coordinación, información dispersa, burnout del cuidador
3. **Nuestra plataforma** — panel visual con signos vitales, medicamentos, agenda
4. **Funcionalidades** — 6 cards (recordatorios, signos vitales, medicamentos, citas, evaluación, formación)
5. **WhatsApp** — diferenciador: cero barrera de adopción
6. **Contacto** — formulario Formspree + datos de contacto

---

## Deploy

```bash
# Requiere token de Cloudflare en /tmp/token_kl.txt o como variable de entorno
CLOUDFLARE_API_TOKEN=$(cat /tmp/token_kl.txt) npx wrangler deploy
```

---

## Paleta de colores

| Variable CSS | Valor | Uso |
|---|---|---|
| `--accent` | `#4DB0AD` | Teal principal (coincide con logo SVG) |
| `--accent-dim` | `#3a9190` | Hover/activo |
| `--bg` | `#0a1628` | Fondo principal (navy oscuro) |
| `--bg-card` | `#0f2240` | Cards |
| `--text` | `#f1f5f9` | Texto principal |

---

## Pendientes

- [ ] Reemplazar Formspree ID `XXXXXXXX` con ID real de cuenta Formspree
- [ ] Usar `kaira_logo_corazon.svg` en alguna sección si se desea logo grande visible
- [ ] Configurar auto-deploy desde GitHub a Cloudflare (actualmente manual)

---

*Kaira Labs SAS — NIT 902.048.250-4 — Bogotá, Colombia*
