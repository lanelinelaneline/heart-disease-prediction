# Heart Disease Prediction

## Описание
Проект по предсказанию наличия сердечного заболевания на основе медицинских показателей.

## Данные
Датасет содержит 600 000 записей (train) и 400 000 записей (test) со следующими признаками:
- Age (возраст)
- Sex (пол)
- Chest (тип боли в груди)
- Resting blood pressure (давление покоя)
- Serum cholesterol (холестерин)
- Fasting blood sugar (сахар натощак)
- Resting ECG (результаты ЭКГ)
- Max heart rate (максимальная ЧСС)
- Exercise induced angina (стенокардия при нагрузке)
- Oldpeak (депрессия ST)
- Slope (наклон ST)
- Number of major vessels (количество сосудов)
- Thal (дефект)

**Целевая переменная:** `class` (0 – нет болезни, 1 – болезнь).

## Предобработка
- Удаление невалидных значений (возраст 0–120, давление 50–250, холестерин 100–600 и т.д.)
- Округление и фильтрация категориальных признаков до разрешённых значений
- One‑hot encoding для категориальных переменных
- Масштабирование числовых признаков (StandardScaler)

## Тепловая карта корелляции
<img width="1124" height="989" alt="image" src="https://github.com/user-attachments/assets/95e07b6e-8f4d-4e44-ba5b-3aa6cdc13810" />

## Статистика выбросов
<img width="5589" height="593" alt="image" src="https://github.com/user-attachments/assets/3a107640-9a19-45d2-8767-9e274f5d198f" />

  
## Модели
- Logistic Regression (balanced)
- Random Forest (balanced)
- Deep Neural Network (4 слоя)

## ROC-кривые на валидации

<img width="691" height="547" alt="image" src="https://github.com/user-attachments/assets/a62b524c-c11e-497f-8439-6f92354401f8" />

## Сравнение моделей
<img width="1478" height="390" alt="image" src="https://github.com/user-attachments/assets/1bd05c4e-290d-4e29-aaa3-78e030564cb2" />


## Результаты на валидации

| Модель               | Accuracy | Precision | Recall | F1     | ROC_AUC |
|----------------------|----------|-----------|--------|--------|---------|
| Logistic Regression  | 0.8864   | 0.8653    | 0.8822 | 0.8736 | 0.9546  |
| Random Forest        | 0.8974   | 0.8926    | 0.8748 | 0.8836 | 0.9604  |
| Neural Network       | 0.9014   | 0.8942    | 0.8830 | 0.8886 | 0.9642  |
