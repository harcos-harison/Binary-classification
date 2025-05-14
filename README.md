Проект: Бинарная классификация для предиктивного обслуживания оборудования
Описание
Проект направлен на разработку модели машинного обучения для предсказания отказов оборудования на основе датасета AI4I 2020 Predictive Maintenance Dataset. Датасет содержит 10,000 записей с 14 признаками, описывающими состояние оборудования. Целевая переменная — Machine failure (0 = без отказа, 1 = отказ, 3.39% случаев). Подробное описание доступно на UCI Machine Learning Repository.
Установка и запуск

Клонируйте репозиторий:git clone <ссылка на репозиторий>


Создайте виртуальное окружение:python -m venv E:\app\.venv
E:\app\.venv\Scripts\activate  # На Windows


Установите зависимости:pip install -r requirements.txt

Если возникает ошибка с streamlit-reveal-slides, установите вручную:pip install streamlit-reveal-slides==0.1.0


Поместите датасет predictive_maintenance.csv в папку data/ или используйте загрузку через интерфейс/uciimlrepo.
Запустите приложение:streamlit run E:\app\app.py



Структура репозитория

app.py: Основной файл приложения.
pages/analysis_and_model.py: Страница с анализом данных и моделью.
pages/presentation.py: Страница с презентацией проекта.
requirements.txt: Файл с зависимостями.
data/predictive_maintenance.csv: Датасет.
README.md: Описание проекта.
video/demo.mp4: Видео-демонстрация (добавить самостоятельно).
report_template.docx: Шаблон отчёта.

Использование

Анализ и модель:
Загрузите датасет (CSV, ucimlrepo, или встроенный).
Изучите визуализации (распределения, корреляции, метрики).
Обучите модели (Logistic Regression, Random Forest, XGBoost, SVM) и получите метрики (accuracy, ROC-AUC, confusion matrix, classification report).
Используйте форму для предсказания отказов.


Презентация:
Просмотрите слайды с описанием проекта (введение, датасет, этапы, приложение, заключение).


Тестирование:
Пример данных отказа (UDI=51):
Product ID: L
Air temperature [K]: 298.9
Process temperature [K]: 309.1
Rotational speed [rpm]: 2861
Torque [Nm]: 4.6
Tool wear [min]: 143


Ожидаемый результат: Отказ с вероятностью >0.3.



Устранение ошибок

Ошибка импорта reveal_slides:
Активируйте виртуальную среду: E:\app\.venv\Scripts\activate.
Установите модуль: pip install streamlit-reveal-slides==0.1.0.
Проверьте версию Python (3.8–3.12): python --version.
Обновите pip: python -m pip install --upgrade pip.
Проверьте конфликты: pip check.


Пустое окно:
Проверьте терминал и консоль браузера (F12 → Console).
Очистите кэш: rmdir /s /q E:\app\.streamlit\cache.


KeyError для столбцов:
Проверьте имена столбцов на странице «Анализ и модель» (вывод data.columns).
Используйте ucimlrepo для загрузки стандартного датасета.



Видео-демонстрация
Ссылка на видео (добавить самостоятельно после записи).
Отчёт
Шаблон отчёта в формате DOCX находится в report_template.docx. Следуйте структуре из задания (стр. 22–24).
