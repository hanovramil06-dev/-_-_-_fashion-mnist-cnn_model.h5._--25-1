# Fashion-MNIST CNN Classification

## Архитектура
- 3 свёрточных блока (Conv2D + BatchNormalization + MaxPooling + Dropout)
- Полносвязные слои: Dense(256) -> Dense(128) -> Dense(10) с softmax
- Аугментация: поворот, сдвиг, горизонтальное отражение
- Оптимизатор: Adam, функция потерь: sparse_categorical_crossentropy

## Результаты
- Тестовая точность: ~93.2%
- EarlyStopping остановлен на ~25 эпохах

## Анализ ошибок
Чаще всего путает:
1. Pullover ↔ Coat (схожая форма).
2. Shirt ↔ T-shirt/top (похожий силуэт).
3. Sandal ↔ Sneaker (сходство подошвы).
