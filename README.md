# 🐾 Моя разношерстная стая

Честный блог о жизни с пятью очень разными животными.

## 📖 О проекте

Это сайт для RSS-ленты в Яндекс Дзен канала **"Моя разношерстная стая"**.

**Канал о:**
- Две собаки (Соня, Малыш)
- Три кошки (Дуся, Хиля, Рыся)
- Реальные истории без прикрас
- Практические советы о содержании, здоровье и поведении

## 🚀 Развёртывание на GitHub Pages

### Шаг 1: Создать репозиторий на GitHub

1. Перейдите на https://github.com/new
2. Назовите репозиторий: `myshaggypack` (или любое другое имя)
3. Выберите "Public"
4. Нажмите "Create repository"

### Шаг 2: Загрузить файлы

#### Вариант A: Через GitHub веб-интерфейс (проще)

1. Откройте ваш новый репозиторий
2. Нажмите "Add file" → "Upload files"
3. Загрузите файлы:
   - `index.html`
   - `rss.xml`
   - `README.md`
4. Нажмите "Commit changes"

#### Вариант B: Через Git (для продвинутых)

```bash
# Клонируйте репозиторий
git clone https://github.com/YOUR_USERNAME/myshaggypack.git
cd myshaggypack

# Скопируйте файлы
cp index.html rss.xml README.md ./

# Загрузите на GitHub
git add .
git commit -m "Initial commit: website and RSS feed"
git push origin main
```

### Шаг 3: Включить GitHub Pages

1. Откройте страницу репозитория
2. Перейдите в **Settings** → **Pages**
3. В разделе "Source" выберите **main** и **/root**
4. Нажмите "Save"
5. Ждите 1-2 минуты, пока GitHub развернёт сайт

### Шаг 4: Ваш сайт готов!

Сайт будет доступен по адресу:
```
https://YOUR_USERNAME.github.io/myshaggypack/
```

## 📡 Подключение RSS к Яндекс Дзену

### В Яндекс Дзене:

1. Откройте **"Мой канал"** → **"Источники контента"**
2. Выберите **"Добавить RSS"**
3. Вставьте ссылку на вашу RSS-ленту:
   ```
   https://YOUR_USERNAME.github.io/myshaggypack/rss.xml
   ```
4. Нажмите **"Добавить источник"**
5. Проверьте, что Дзен получает посты

## 📁 Структура файлов

```
myshaggypack/
├── index.html      # Главный сайт (HTML + CSS + JS)
├── rss.xml        # RSS-лента с полным контентом
└── README.md      # Этот файл
```

## ✏️ Как добавлять новые статьи

### Добавить в HTML (для сайта):

Откройте `index.html`, найдите массив `articles` и добавьте новый объект:

```javascript
{
    id: 8,
    title: "Название вашей статьи",
    category: "sonya",  // sonya, malysh, dusya, hilya, rysia, vet, new, about
    date: "17 сентября 2026",
    tags: ["Здоровье", "Истории"],
    image: "data:image/svg+xml,%3C...",  // или URL
    content: `Ваш текст статьи...`
}
```

### Добавить в RSS (для Дзена):

Откройте `rss.xml`, добавьте новый блок `<item>`:

```xml
<item>
    <title>Название статьи</title>
    <link>https://your-site.com?category=sonya</link>
    <guid>article-8</guid>
    <pubDate>Mon, 17 Sep 2026 10:00:00 +0300</pubDate>
    <category>Здоровье</category>
    <description>Краткое описание</description>
    <content:encoded><![CDATA[
        <img src="..." />
        <h2>Название</h2>
        <p>Полный текст статьи...</p>
    ]]></content:encoded>
</item>
```

## 🎨 Кастомизация

### Изменить цвета (RGB: 225, 112, 85 — основной оранжевый)

В `index.html` найдите `<style>` и отредактируйте:
- `#e17055` — основной цвет (оранжевый)
- `#f5f1e8` — фон (молочный)
- `#2d3436` — текст (графитовый)

### Изменить заголовок и описание

В `index.html` обновите:
```html
<div class="logo">🐾 Моя разношерстная стая</div>
<div class="tagline">Две собаки, три кошки, пять характеров и один дом</div>
```

В `rss.xml` обновите:
```xml
<title>Моя разношерстная стая</title>
<description>Две собаки, три кошки, пять характеров и один дом...</description>
```

## 🔗 Ссылки на рубрики

Переход на категорию:
```
https://your-site.com?category=sonya
https://your-site.com?category=malysh
https://your-site.com?category=dusya
https://your-site.com?category=hilya
https://your-site.com?category=rysia
https://your-site.com?category=vet
https://your-site.com?category=about
```

## 📱 Мобильная оптимизация

Сайт полностью адаптивен и работает на:
- Десктопе
- Планшетах
- Мобильных телефонах

## ⚠️ Важно

- **Изображения:** В текущей версии используются SVG-плейсхолдеры. Вы можете заменить их на реальные изображения (JPG/PNG/WebP).
- **RSS с изображениями:** Изображения в RSS встроены как data URI или URL. Убедитесь, что они доступны по интернету.
- **Контакты:** Обновите контактные данные в footer.

## 🤝 Поддержка

Если у вас есть вопросы:
- Гайд на GitHub: https://pages.github.com/
- Яндекс Дзен: https://dzen.ru/

---

**Создано для:** Канал "Моя разношерстная стая" 🐾
