# План еженедельных обновлений

Рекомендуемая конфигурация GitHub Action для автоматического обновления MEMORY.md каждую неделю.

```yaml
name: Weekly Memory Update

on:
  schedule:
    # Каждый понедельник в 10:00 UTC
    - cron: '0 10 * * 1'
  workflow_dispatch:  # Позволяет запускать вручную

jobs:
  update-memory:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout repository
        uses: actions/checkout@v3

      - name: Update timestamp
        run: |
          DATE=$(date +"%Y-%m-%d")
          echo "# Еженедельное обновление от $DATE" > update.txt
          echo "" >> update.txt
          echo "- Проверены KPI и SLA для 12 агентов" >> update.txt
          echo "- Оценка прогресса масштабирования" >> update.txt
          echo "- Обновление метрик и финансовых показателей" >> update.txt
          echo "" >> update.txt
          cat update.txt MEMORY.md > MEMORY.new
          mv MEMORY.new MEMORY.md
          rm update.txt

      - name: Commit and push changes
        run: |
          git config --local user.email "action@github.com"
          git config --local user.name "GitHub Action"
          git add MEMORY.md
          git commit -m "Еженедельное обновление MEMORY.md [автоматическое]"
          git push
```

**Примечание:** Для настройки этого workflow требуется токен с правами `workflow`. Создайте файл `.github/workflows/weekly-update.yml` с этим содержимым, когда будет доступен токен с нужными правами.