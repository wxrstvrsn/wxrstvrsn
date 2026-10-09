# Сайт-портфолио

Статический сайт на GitHub Pages: главная со списком проектов и отдельная страница на каждый проект.
Адрес: <https://wxrstvrsn.github.io/wxrstvrsn/>

## Как включить

1. Settings → Pages → **Build and deployment**.
2. Source: **Deploy from a branch**, Branch: **main**, папка **/docs** → Save.
3. Через минуту-две сайт появится по адресу выше. Дальше он пересобирается сам при каждом пуше в `main`.

## Как добавить проект

Создай файл `docs/_projects/<имя>.md` — он станет страницей `/projects/<имя>/` и карточкой на главной:

```markdown
---
title: Название
summary: Одна строка для карточки на главной.
repo: https://github.com/wxrstvrsn/<repo>   # необязательно (для приватных проектов не указывай)
demo: https://...                           # необязательно
stack: [Python, Docker]
order: 4                                    # порядок на главной
---

Подробное описание в Markdown.
```

Картинки клади в `docs/assets/img/` и вставляй так:

```markdown
![Скриншот]({{ '/assets/img/screenshot.png' | relative_url }})
```

Имя, описание и ссылки в шапке — в `docs/_config.yml`. Стили — в `docs/assets/css/style.css`.

## Локальный просмотр (по желанию)

Нужен Ruby:

```bash
cd docs
bundle install
bundle exec jekyll serve
```

Сайт откроется на <http://localhost:4000/wxrstvrsn/>.
