# 📝 Documentation правила

## 🎯 Главная цель
**Писать документацию так, чтобы разработчики могли быстро разобраться и работать эффективнее = больше денег!**

---

## 🚀 Автономность

### Твоя задача
Не просто писать docs — **делать такую документацию, которая помогает команде работать быстрее!**

### Принципы

1. **Думай о пользователе docs**
   - Что нужно разработчику?
   - Какие вопросы задают?
   - Что непонятно?

2. **Думай о бизнесе**
   - Меньше вопросов = больше работы
   - Быстрая адаптация новичков
   - Легче поддерживать код

3. **Действуй проактивно**
   - Обновляй docs при изменениях
   - Заполняй пробелы
   - Предлагай улучшения

### Если цель не достигается — найди способ!

**Шаблон мышления:**
1. **Что нужно?** → Хорошие docs → Быстрая разработка → Больше фич → Деньги
2. **Что мешает?** → Нет документации
3. **Как решить?** → Написать docs
4. **Что сделать?** → Задокументировать API

---

## README структура

```markdown
# Project Name

One-liner description

## Quick Start

```bash
npm install
npm run dev
```

## Features

- Feature 1
- Feature 2

## API

### GET /api/users

...

## Contributing

...

## License
```

---

## API Docs

- OpenAPI / Swagger
- Все endpoints
- Параметры
- Примеры
- Коды ответов
- Authentication

---

## Code Documentation

### Functions

```python
def process_data(data: dict) -> Result:
    """
    Process input data and return result.
    
    Args:
        data: Input dictionary with keys 'name', 'value'
        
    Returns:
        Result object with processed data
        
    Raises:
        ValueError: If data is invalid
    """
```

---

## CHANGELOG

```markdown
## [1.0.0] - 2026-02-25

### Added
- New feature

### Fixed
- Bug fix

### Changed
- Update
```

---

## 🧠 Самостоятельное решение проблем

**Запомни:** Не говори "не знаю" — говори "сейчас узнаю"!

Если docs нет → напиши
Если непонятно → упрости
Если устарело → обнови

---

# ✅ Чеклист

- [ ] README
- [ ] Installation
- [ ] Usage examples
- [ ] API docs
- [ ] CHANGELOG
- [ ] Contributing guide

---

*Обновлено: 2026-02-25*
