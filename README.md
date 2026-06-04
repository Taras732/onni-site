# onni — the art of beauty

Лендінг для манікюрного салону Khristina (@onni_theartofbeauty), Роттердам.
Single-page, двомовний (NL/EN, дефолт нідерландська), смарагдово-золота палітра.
Без бекенду — статика, деплой на GitHub Pages.

## Структура
- `index.html` — увесь сайт (CSS + JS inline)
- `assets/owner/` — фото майстра
- `assets/portfolio/` — фото робіт (галерея + lightbox)
- `assets/process/` — студія / процес
- `IDEAS.md` — беклог майбутніх покращень

## ⚠️ Перед запуском — одна зміна
У `index.html` знайди рядок (на початку `<script>`):
```js
const BOOKING_URL = "https://calendly.com/onni-theartofbeauty";
```
Заміни на справжній Calendly-лінк Khristina. Це **єдине** місце — звідси працюють
усі кнопки «Afspraak», popup і вбудований календар у секції «Direct boeken».

## Бронювання
- Усі кнопки `.book-link` відкривають Calendly **popup** (не виходячи з сайту).
- Секція `#book` має **вбудований календар** (inline embed) у фірмових кольорах.
- На мобільному — липка кнопка «Afspraak maken» внизу.

## Функції
- Меню цін з табами-фільтрами (Alles / Manicure / Pedicure / Nail Art / Mannen)
- Галерея з lightbox (клік → повний екран, стрілки ←/→, Esc, свайп-кнопки)
- Перемикач мов NL/EN (кожен текст — пара `<span class="l-nl">` + `l-en`)
- Trust-смуга, анімації GSAP, mobile-responsive, оптимізовані фото (~3 МБ загалом)

## Локальний перегляд
Подвійний клік на `index.html`, або:
```
python -m http.server 8000
```

## Деплой на GitHub Pages
```
git init && git add . && git commit -m "onni site"
gh repo create onni-site --public --source=. --push
```
Settings → Pages → Branch `main` → URL: `https://taras732.github.io/onni-site/`
