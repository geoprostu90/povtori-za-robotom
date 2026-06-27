# Ян, помоги роботу! 🤖

PWA-игра для детей 4+ лет. Робот показывает последовательность из 3 действий (⬆️ ⬇️ 🔄), ребёнок повторяет.

## Как играть

1. Нажми **«Играть»**
2. Смотри, какие кнопки подсвечивает робот
3. Повтори ту же последовательность
4. За правильный ответ — звук и машинка 🚗!

## Локальный запуск

Service Worker работает только через HTTP(S), не через `file://`.

```bash
# Python 3
python -m http.server 8080

# или Node.js (npx)
npx serve .
```

Открой в браузере: `http://localhost:8080`

## Деплой на GitHub Pages

### 1. Создай репозиторий на GitHub

Например: `povtori-za-robotom`

### 2. Загрузи файлы

```bash
git init
git add index.html manifest.json sw.js README.md
git commit -m "PWA-игра: Повтори за роботом"
git branch -M main
git remote add origin https://github.com/ВАШ_ЛОГИН/povtori-za-robotom.git
git push -u origin main
```

### 3. Включи GitHub Pages

1. Открой репозиторий на GitHub
2. **Settings** → **Pages**
3. **Source**: Deploy from a branch
4. **Branch**: `main` → папка `/ (root)` → **Save**

Через 1–2 минуты игра будет доступна по адресу:

```
https://ВАШ_ЛОГИН.github.io/povtori-za-robotom/
```

### 4. Установка на телефон (PWA)

**Android (Chrome):**
- Открой сайт → меню (⋮) → «Установить приложение» / «Добавить на главный экран»

**iPhone (Safari):**
- Открой сайт → кнопка «Поделиться» → «На экран Домой»

## Структура проекта

```
povtori-za-robotom/
├── index.html      # игра (HTML + CSS + JS)
├── manifest.json   # PWA-манифест
├── sw.js           # service worker
└── README.md
```

## Технологии

- Чистый HTML/CSS/JS, без внешних зависимостей
- Web Audio API для звуков
- Service Worker для офлайн-кэширования
- Адаптивная вёрстка до 480px
