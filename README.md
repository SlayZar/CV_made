* Для определения ключевых точек лица использовалась предобученная модель ResNet50.
* Пробовались и другие модели, однако они либо слишком вычислительны сложны (ResNet101) или показывали заметно худший скор 
(VGG50, GoogleNet)
* Модель обучалась на всех данных с оптимизатором AdamW и понижением лёрнинг рейта при достижении двух эпох без улучшения лосса.
* Для более качественной работы модели оптимизировалась метрика Smooth L1 Loss, а не MSE.
* Лучшую модель удалось достичь на 28-ой эпохе.

Для воспроизведения решения можно скачать веса модели по ссылке (ссылка есть и в ноутбуке):
https://www.dropbox.com/s/iqd056eltyd2sza/baseline_1_best.pth?dl=0

И далее запустить предикт.

Данный файл генерирует решение (9.33968)
![](https://wampi.ru/image/6o2XinV)

После пробовал дообучать эти веса с другим оптимизатором и варьировать лёрнинг рейт, удалось улучшить прайват скор до 9.31876, 
но улучшение в месте на лидерборде не дало.
