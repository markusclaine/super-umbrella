## AI-DIGEST.RU - ПРАВИЛА РАБОТЫ С ИНСТРУМЕНТАМИ

### 🔐 SSH ДОСТУП
```
Хост: ai-digest.ru (141.8.192.25)
Пользователь: f1237247
Пароль: unhigafafi
Путь к сайту: /home/f1237247/domains/ai-digest.ru/public_html
```

### 🗄️ ДОСТУП К БАЗЕ ДАННЫХ
```
База: f1237247_app_wordpress_1
Пользователь: f1237247_app_wordpress_1
Пароль: 7UoHf3PT84
Хост: localhost
```

### 🛠️ ИНСТРУМЕНТЫ УПРАВЛЕНИЯ

#### 1. SSH КОМАНДЫ
```bash
# Доступ к сайту
sshpass -p 'unhigafafi' ssh f1237247@141.8.192.25

# Просмотр файлов
cd domains/ai-digest.ru/public_html
ls -la

# Проверка базы данных
mysql -u f1237247_app_wordpress_1 -p7UoHf3PT84 -e "USE f1237247_app_wordpress_1; SELECT * FROM wp_posts LIMIT 5;"
```

#### 2. WordPress API
```php
# Добавление поста
wp_insert_post([
    'post_title' => $title,
    'post_content' => $content,
    'post_status' => 'publish',
    'post_type' => 'post'
]);

# Получение постов
$args = [
    'post_status' => 'publish',
    'posts_per_page' => 10
];
$posts = get_posts($args);
```

#### 3. Скрипты управления
```bash
# Добавление изображений через Unsplash
php add_images.php

# Публикация новостей
php publish_news.php
```

### 📋 ПРАВИЛА ИСПОЛЬЗОВАНИЯ

#### 1. БЕЗОПАСНОСТЬ
- Никогда не хранить пароли в открытом виде
- Использовать sshpass только для автоматизации
- Регулярно менять пароли

#### 2. ОПТИМИЗАЦИЯ
- Проверять скорость загрузки через SSH
- Оптимизировать изображения через add_images.php
- Использовать CDN для статики

#### 3. КОНТЕНТ
- Публиковать минимум 3 новости в день
- Использовать publish_news.php для автоматизации
- Добавлять изображения через add_images.php

#### 4. МОНИТОРИНГ
- Проверять базу данных через MySQL
- Мониторить логи ошибок
- Отслеживать трафик через WordPress

### ❌ ОШИБКИ КОТОРЫЕ НЕЛЬЗЯ ДЕЛАТЬ

1. **Неправильные команды SSH** - всегда проверять синтаксис
2. **Отсутствие паролей** - использовать sshpass для автоматизации
3. **Игнорирование ошибок** - всегда проверять коды возврата
4. **Неправильный путь** - всегда проверять пути к файлам
5. **База данных** - всегда использовать правильные параметры подключения

### ⚙️ АВТОМАТИЗАЦИЯ

#### 1. Ежедневные задачи
```bash
# Публикация новостей
every 6 hours php publish_news.php

# Оптимизация изображений
every 12 hours php add_images.php
```

#### 2. Мониторинг
```bash
# Проверка доступности сайта
every 5 minutes curl -s https://ai-digest.ru

# Проверка базы данных
every 1 hour mysql -u f1237247_app_wordpress_1 -p7UoHf3PT84 -e "SELECT COUNT(*) FROM wp_posts;"
```

### ⌨️ КОНТАКТЫ
- **Хост:** 141.8.192.25
- **SSH:** f1237247@unhigafafi
- **База:** f1237247_app_wordpress_1/7UoHf3PT84
- **Путь:** /home/f1237247/domains/ai-digest.ru/public_html

---

*Обновлено: 2026-03-06*
*Следующее обновление: 2026-03-13*