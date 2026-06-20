# Buildo Логотипы — Telegram-бот

> **Логотип и бренд-айдентика для бизнеса за 60 секунд**

Часть экосистемы **Buildo** (https://buildo.ru). MIT licensed. Open source.

![Buildo](https://img.shields.io/badge/Buildo-ecosystem-5B8DEF?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-green?style=for-the-badge)

---

## Что это

Telegram-бот для продукта Логотипы. Сервисный слой: вход в Mini App, оплата, ingestion, уведомления.

**Сценарий использования (Telegram-бот):** Опиши бренд → получи 5 вариантов логотипа

---

## Архитектура

```
Buildo Логотипы экосистема
├── shekelstrong/buildo-logo-tg          ← этот репо (Telegram-бот)
├── shekelstrong/buildo-logo-miniapp    ← Mini App
└── shekelstrong/buildo-logo-site        ← Маркетинговый сайт
```

---

## Стек

| Слой | Технология |
|---|---|
| Bot | aiogram 3.x + Redis FSM + Docker |
| Frontend | Vite + React 19 + Tailwind + lucide-react |
| Backend | FastAPI + SQLAlchemy Async + YandexART + ЮKassa |
| AI (image) | YandexART (генерация + вариации) |
| AI (text) | MiniMax M3 для генерации идей и копирайта |
| Deploy | VPS 108.165.164.85 / 31.76.29.244 через CI/CD (GitHub Actions → SSH) |

---

## Монетизация

1490 ₽ за пакет (5 логотипов + favicon + гайдлайн)

**Целевая аудитория:** Стартапы, ИП, малый бизнес, фрилансеры
**Конкуренты (РФ):** Турболого (5-15к ₽), Логастер (2-10к ₽), Tailor Brands (не в РФ)

---

## Деплой

```bash
cp .env.example .env
# заполни: TELEGRAM_BOT_TOKEN, OPENROUTER_API_KEY, YOOKASSA_*
docker compose up --build
```

Продакшен:
```bash
git push origin main  # GitHub Actions → SSH → VPS → docker compose up -d --build
```

---

## Связанные репо

- [buildo-logo-tg](https://github.com/shekelstrong/buildo-logo-tg) — этот репо
- [buildo-logo-miniapp](https://github.com/shekelstrong/buildo-logo-miniapp)
- [buildo-logo-site](https://github.com/shekelstrong/buildo-logo-site)
- [nemo-team-docs/projects/buildo/logo/](https://github.com/shekelstrong/nemo-team-docs/tree/main/projects/buildo/logo) — спецификация

---

## License

MIT (c) 2026 Buildo Ecosystem. Inspired by [awesome-generative-ai-apps](https://github.com/Anil-matcha/awesome-generative-ai-apps).