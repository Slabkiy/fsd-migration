## 1. Структура папок (kebab-case)

text

Copy

Download

src/
  pages/
    feature-name/       # Папка фичи в kebab-case
      index.ts          # Реэкспорт
      ui/               # UI-компоненты страницы
      model/            # Бизнес-логика
      lib/              # Вспомогательные функции
      ComponentName.tsx # Основной компонент

## 2. Именование файлов

|Тип|Конвенция|Пример|
|---|---|---|
|Страницы|PascalCase|`ProcessPage.tsx`|
|Компоненты|PascalCase|`EmployeeCard.tsx`|
|Хуки|useCamelCase|`useEmployeeData.ts`|
|Сервисы/API|camelCase + Service|`processService.ts`|
|Модели/Типы|PascalCase|`Employee.types.ts`|
|Тесты|SameName.test.ts|`ProcessPage.test.tsx`|
|Стили|module.scss|`ProcessPage.module.scss`|

**Пример полного пути для вашего случая**:

```bash
src/
  pages/
    process/
      index.ts            # export { ProcessPage } from './ui/ProcessPage'
      ui/
        ProcessPage.tsx   # Основной компонент
        ProcessList.tsx   # Список процессов
      model/
        useProcessData.ts # Логика загрузки
      lib/
        helpers.ts        # Утилиты
```

**Новые компоненты**:

```bash
# Старая структура:
src/components/EmployeeEditor/EmployeeEditor.tsx

# Новая структура:
src/features/employee-management/EmployeeEditor.tsx
```
