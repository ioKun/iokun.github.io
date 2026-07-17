# Публикация резюме на GitHub Pages

Репозиторий: `git@github.com:ioKun/iokun.github.io.git`  
Сайт после деплоя:
- **RU:** https://iokun.github.io/
- **EN:** https://iokun.github.io/en/

---

## Первый пуш (уже настроено локально)

В папке `resume-site` remote уже указывает на ваш репозиторий. Осталось:

```powershell
cd C:\Workspace\AI\InterviewPreparation\resume-site
git push -u origin main
```

Если репозиторий на GitHub ещё пустой / только что создан — этого достаточно.

Если GitHub ругается на non-fast-forward (там уже есть файлы, например README):

```powershell
git pull origin main --rebase
git push -u origin main
```

Или, если уверены, что remote можно перезаписать:

```powershell
git push -u origin main --force
```

(force только если в remote нет нужной истории.)

---

## Включение GitHub Pages

1. GitHub → репозиторий **iokun.github.io** → **Settings** → **Pages**
2. Source: **Deploy from a branch**
3. Branch: **main** / folder: **/ (root)** → Save
4. Через 1–3 минуты откройте https://iokun.github.io/

---

## Дальнейшие обновления

```powershell
cd C:\Workspace\AI\InterviewPreparation\resume-site
git add .
git commit -m "Update resume"
git push
```

---

## Локальный просмотр

```powershell
cd C:\Workspace\AI\InterviewPreparation\resume-site
python -m http.server 8080
```

Откройте http://localhost:8080 (RU) и http://localhost:8080/en/ (EN).

---

## В откликах

```
Resume: https://iokun.github.io/
Resume (EN): https://iokun.github.io/en/
```
