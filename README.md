
# Memoria 3D – Static Landing Page

## Як запустити локально

1. Встанови **Node.js** (версія 18+).  
2. Перейди в директорію проєкту  
   ```bash
   cd memoria3d_site
   ```
3. Встанови http-сервер (одноразово)  
   ```bash
   npm install -g serve
   ```
4. Запусти сайт  
   ```bash
   serve public
   ```
   і відкрий посилання, яке покаже `serve` (типово http://localhost:3000).

> **Альтернативно:** якщо не хочеш ставити Node, відкрий `public/index.html` подвійним кліком – більшість браузерів коректно відкриють сторінку і картинки (3D-модель не працюватиме без https).

## Деплой безкоштовно на GitHub Pages

1. Створи новий репозиторій на GitHub.  
2. Завантаж в репозиторій вміст папки `public/`.  
3. У налаштуваннях → **Pages** вибери гілку `main` / папку `/ (root)` і натисни **Save**.  
4. Через кілька секунд сайт буде доступний за посиланням типу  
   ```
   https://your-username.github.io/your-repo
   ```

> Для Vercel/Netlify достатньо перетягнути папку `public/` у їхню дроп‑зону — система сама все підхопить.

### Де покласти 3D‑модель

1. Перетягни свій файл `memorial.glb` у `public/models/`.  
2. У `public/index.html` відредагуй атрибут `src` у тегу `<model-viewer>`:
   ```html
   <model-viewer src="models/memorial.glb" ...></model-viewer>
   ```

Enjoy!
