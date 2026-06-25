# Диаграммы Mermaid в Markdown

Mermaid позволяет создавать диаграммы и схемы с помощью текстового описания.

## 1. Flowchart (Блок-схема)
```mermaid
flowchart LR
    A[Начало] --> B{Решение}
    B -->|Да| C[Действие 1]
    B -->|Нет| D[Действие 2]
    C --> E[Конец]
    D --> E
```

## 2. Sequence Diagram (Диаграмма последовательности)
```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, как дела?
    Bob-->>Alice: Отлично!
    Bob->>Alice: А у тебя?
    Alice-->>Bob: Всё хорошо
```

## 3. Gantt Chart (Диаграмма Ганта)
```mermaid
gantt
    title План проекта
    dateFormat  YYYY-MM-DD
    section Дизайн
    Исследование    :a1, 2024-01-01, 7d
    Прототип       :after a1, 5d
    section Разработка
    Бэкенд         :2024-01-10, 10d
    Фронтенд       :2024-01-12, 8d
```

## 4. Class Diagram (Диаграмма классов)
```mermaid
classDiagram
    class Animal {
        +String name
        +makeSound()
    }
    class Dog {
        +breed
    }
    class Cat {
        +color
    }
    Animal <|-- Dog
    Animal <|-- Cat
```

## 5. State Diagram (Диаграмма состояний)
```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> Running
    Running --> Idle
    Running --> Completed
    Completed --> [*]
```

## 6. Pie Chart (Круговая диаграмма)
```mermaid
pie
    title Распределение времени
    "Работа" : 8
    "Сон" : 7
    "Отдых" : 5
    "Другое" : 4
```

## 7. User Journey (Путь пользователя)
```mermaid
journey
    title Мой рабочий день
    section Утро
      Проснуться: 5: Я
      Завтрак: 3: Я
    section Работа
      Писать код: 8: Я, Коллеги
```

## 8. Git Graph (Граф Git)
```mermaid
gitGraph
    commit
    commit
    branch develop
    checkout develop
    commit
    commit
    checkout main
    merge develop
    commit
```

> 💡 Для рендеринга Mermaid-диаграмм используйте поддержку в GitHub, GitLab, VS Code (расширение Markdown Preview Mermaid Support) или Obsidian.
