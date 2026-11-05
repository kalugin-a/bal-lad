# AGENTS.md — bal-lad

Простая статичная страница для GitHub Pages.
Репозиторий: `https://github.com/kalugin-a/bal-lad`, ветка `main`.
Прод: `https://kalugin-a.github.io/bal-lad/`

## Публикация

Любой пуш в `main` → автодеплой через GitHub Actions (`.github/workflows/pages.yml`).
Ручной деплой: Actions → Deploy Pages → Run workflow.

## Структура

- `index.html` — единственная страница
- `.github/workflows/pages.yml` — CI/CD (checkout → configure-pages → upload-pages-artifact → deploy-pages)

## Локальная разработка

```bash
cd /home/opencode/workspace/alex/bal-lad
# редактируй index.html
git add index.html && git commit -m "msg" && git push origin main
```

## Секреты

Токен GitHub не хранится в репозитории. Для пуша с сервера используй:
```bash
git push https://$GH_TOKEN@github.com/kalugin-a/bal-lad.git main
```
(`GH_TOKEN` — classic PAT с scopes `repo`, `workflow`)

## Версии

Версионирование не ведётся (простая статика). История — в git log.