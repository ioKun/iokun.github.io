# Публикация резюме на GitHub Pages

После деплоя сайт будет доступен по адресу:

**https://iokun.github.io/**

(если репозиторий называется `iokun.github.io` — регистр GitHub username может отличаться, проверьте свой: https://github.com/ioKun)

---

## Вариант 1 — Рекомендуемый: `username.github.io`

1. Создайте на GitHub новый **публичный** репозиторий с именем **`iokun.github.io`** (или `ioKun.github.io` — GitHub обычно нечувствителен к регистру в URL).

2. Скопируйте содержимое папки `resume-site/` в корень репозитория:
   ```
   index.html      ← русская версия
   en/index.html   ← английская версия
   css/style.css
   ```

3. Закоммитьте и запушьте в ветку `main`.

4. GitHub → **Settings** → **Pages** → Source: **Deploy from branch** → `main` / `/ (root)`.

5. Через 1–3 минуты:
   - RU: `https://<username>.github.io/`
   - EN: `https://<username>.github.io/en/`

Переключатель **RU / EN** в правом верхнем углу обеих страниц.

---

## Вариант 2 — Отдельный репозиторий `resume`

1. Создайте репозиторий `resume` (публичный).
2. Залейте файлы из `resume-site/`.
3. Settings → Pages → branch `main`, folder `/ (root)`.
4. URL: `https://iokun.github.io/resume/` (если repo называется `resume`).

В сопроводительных письмах указывайте полную ссылку.

---

## Локальный просмотр

Из папки `resume-site`:

```powershell
# Python (если установлен)
python -m http.server 8080

# или npx
npx serve .
```

Откройте http://localhost:8080

---

## Что указать в резюме и откликах

В шапке PDF и LinkedIn добавьте строку:

```
Резюме (web): https://iokun.github.io/
```

Для рекрутеров это удобнее PDF: открывается с телефона, есть кликабельные ссылки на Play Store и GitHub.

---

## Обновление

При смене работы или новых метриках — правьте `index.html` и пушьте. GitHub Pages обновится автоматически.

---

## Опционально: свой домен

Settings → Pages → Custom domain → например `ivanlobanov.dev` (нужен DNS CNAME на `username.github.io`).
