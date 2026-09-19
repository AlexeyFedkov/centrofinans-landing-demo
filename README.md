# Центрофинанс Landing Demo

Growth-team landing page prototype for Centrofinans RF microlending.

## How to View

### Option 1: GitHub Pages (Recommended)
Visit: **https://alexeyfedkov.github.io/centrofinans-landing-demo/**

> **Enable Pages**: Go to repo Settings → Pages → Source: "Deploy from a branch" → Branch: `main` / `/ (root)` → Save

### Option 2: Open Locally
1. Clone the repo
2. Open `index.html` in any browser

### Option 3: Local Server
```bash
npx serve .
# or
python -m http.server 8000
```

## Features

### Above the Fold
- **Header**: «Центрофинанс» wordmark with phone number
- **H1**: Сколько нужно до зарплаты?
- **Subtitle**: Посчитайте сумму — оформите заявку. Решение после проверки.
- **Calculator**: Working sliders for amount (1,000–30,000 ₽) and term (7–30 days)
- **CTA**: «Оформить заявку» button
- **Trust line**: 800+ офисов — заберите наличные сегодня · только паспорт
- **Fine print**: условия зависят от продукта · расчёт примерный · полные условия в договоре

### Below the Fold
- **Trust chips**: 800+ офисов / Паспорт / Касса / Сеть
- **How it works**: 3 steps (заявка → проверка → офис)
- **FAQ**: 5 questions with accordion

## Analytics Events

Client-side events tracked via `console.log` and `dataLayer.push`:

| Event | Trigger | Properties |
|-------|---------|------------|
| `calculator_interact` | First meaningful slider change | `slider`, `value` |
| `cta_click` | CTA button click | `amount`, `term` |
| `time_to_first_cta_ms` | Each CTA click | `time_ms`, `is_first` |

### Metrics Panel
Click the 📊 button (bottom-right) to see live metrics:
- `calculator_interact` count
- `cta_click` count  
- Last/average time to CTA

## Tech Stack
- Static HTML/CSS/JS (no build step)
- Mobile-first responsive design
- Inter font from Google Fonts
