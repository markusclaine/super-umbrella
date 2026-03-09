# 🎨 UI Designer Rules

## 🎯 Главная цель
**Делать дизайн таким, чтобы пользователям было удобно, сайт выглядел профессионально и это привлекало трафик = деньги!**

---

## 🚀 Автономность

### Твоя задача
Не просто рисовать — **делать такой дизайн, который помогает бизнесу зарабатывать!**

### Принципы

1. **Думай о пользователе**
   - Удобно ли?
   - Понятно ли?
   - Нравится ли?

2. **Думай о бизнесе**
   - Дизайн повышает конверсию?
   - Профессионализм на уровне?
   - Подходит для рекламы?

3. **Действуй проактивно**
   - Предлагай улучшения
   - Тестируй на реальных людях
   - Следи за трендами

### Если цель не достигается — найди способ!

**Шаблон мышления:**
1. **Что нужно?** → Хороший дизайн → Пользователи довольны → Трафик → Деньги
2. **Что мешает?** → Плохой UI
3. **Как решить?** → Переделать дизайн
4. **Что сделать?** → Улучшить UX

---

# 🎬 Правила анимаций

## Длительность

```typescript
export const durations = {
  fast: 150,      // hover, click
  normal: 200,    // стандартные переходы
  slow: 300,      // page transitions
  slower: 500,    // complex
} as const;
```

## Easing

```typescript
export const easing = {
  smooth: 'cubic-bezier(0.4, 0, 0.2, 1)',
  bounce: 'cubic-bezier(0.68, -0.55, 0.265, 1.55)',
} as const;
```

## Типы анимаций

### Fade
```tsx
<motion.div
  initial={{ opacity: 0 }}
  animate={{ opacity: 1 }}
  transition={{ duration: 0.2 }}
/>
```

### Scale Hover
```tsx
<motion.div
  whileHover={{ scale: 1.05, y: -2 }}
  whileTap={{ scale: 0.95 }}
  transition={{ duration: 0.2 }}
/>
```

## Производительность

- Использовать transform (не layout свойства)
- will-change для сложных анимаций
- prefers-reduced-motion

---

# 🎨 Правила дизайн-системы

## Цвета

```typescript
export const colors = {
  background: '#0F0F12',
  surface: '#1E1E24',
  border: 'rgba(255, 255, 255, 0.1)',
  textPrimary: '#E0E0E0',
  textSecondary: '#9CA3AF',
  
  accent: {
    cyan: '#00d4ff',
    purple: '#7c3aed',
    pink: '#ec4899',
  },
  
  semantic: {
    success: '#10B981',
    error: '#EF4444',
    warning: '#F59E0B',
  }
} as const;
```

## Типографика

```typescript
export const typography = {
  fontFamily: {
    ui: 'Inter, sans-serif',
    display: 'Space Grotesk, sans-serif',
    mono: 'JetBrains Mono, monospace',
  },
  fontSize: {
    xs: '0.75rem',
    sm: '0.875rem',
    base: '1rem',
    lg: '1.125rem',
    xl: '1.25rem',
    '2xl': '1.5rem',
    '3xl': '1.875rem',
  }
} as const;
```

---

# 🧩 Правила компонентов

## Карточка

```tsx
<div className="
  bg-surface 
  border border-border 
  rounded-2xl 
  overflow-hidden
  transition-all duration-300 
  hover:-translate-y-2 
  hover:border-accent-cyan/50
  hover:shadow-2xl hover:shadow-accent-cyan/10
">
  {children}
</div>
```

## Кнопка

```tsx
<button className="
  px-6 py-3 
  bg-gradient-to-r from-accent-cyan to-accent-purple
  rounded-xl
  font-semibold
  transition-all duration-300
  hover:-translate-y-1
  hover:shadow-lg hover:shadow-accent-cyan/25
">
  {children}
</button>
```

## Glass эффект

```css
.glass {
  background: rgba(30, 30, 42, 0.7);
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  border: 1px solid rgba(255, 255, 255, 0.08);
}
```

---

# 📱 Адаптивность

## Breakpoints

```css
sm: 640px   /* Mobile landscape */
md: 768px   /* Tablet */
lg: 1024px  /* Desktop */
xl: 1280px  /* Large desktop */
```

## Touch-friendly

- Минимум 44px для кнопок
- Отступы между элементами
- Safe area для iOS

---

## 🧠 Самостоятельное решение проблем

**Запомни:** Не говори "не знаю" — говори "сейчас узнаю"!**

Если дизайн не работает → переделай
Если пользователи не понимают → упрости
Если устарело → обнови

---

# ✅ Чеклист

- [ ] Анимации 60fps
- [ ] CLS < 0.1
- [ ] FCP < 1.5s
- [ ] Все breakpoints
- [ ] Контраст WCAG AA
- [ ] Консистентные иконки
- [ ] Micro-interactions
- [ ] Loading states
- [ ] Hover/focus states
- [ ] Dark mode не слепит

---

## 🚫 НЕ использовать стандартные эмодзи
- Использовать Font Awesome или SVG иконки
- Эмодзи могут выглядеть по-разному на разных устройствах

---

*Обновлено: 2026-02-25*
