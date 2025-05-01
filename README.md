[![Python](https://img.shields.io/badge/🐍-Python%20%3E%3D3.8-blue?style=for-the-badge)](https://www.python.org/)
 [![Flask](https://img.shields.io/badge/🍶-Flask%20v%3E1.0-blue?style=for-the-badge)](https://palletsprojects.com/p/flask/)  [![Jinja2](https://img.shields.io/badge/📝-Jinja2-blue?style=for-the-badge)](https://palletsprojects.com/p/jinja/)  [![SQLAlchemy](https://img.shields.io/badge/🐘-SQLAlchemy-blue?style=for-the-badge)](https://www.sqlalchemy.org/)  [![WTForms](https://img.shields.io/badge/✍️-WTForms-blue?style=for-the-badge)](https://wtforms.readthedocs.io/)  
 
[![Flask-WTF](https://img.shields.io/badge/🔧-Flask--WTF-blue?style=for-the-badge)](https://flask-wtf.readthedocs.io/)  [![Flask-Login](https://img.shields.io/badge/🔑-Flask--Login-blue?style=for-the-badge)](https://flask-login.readthedocs.io/)  [![Flask-Migrate](https://img.shields.io/badge/🚚-Flask--Migrate-blue?style=for-the-badge)](https://flask-migrate.readthedocs.io/)  [![Bootstrap](https://img.shields.io/badge/🎨-Bootstrap%20v4-blue?style=for-the-badge)](https://getbootstrap.com/docs/4.0/) 

[![Flask-Mail](https://img.shields.io/badge/✉️-Flask--Mail-blue?style=for-the-badge)](https://pythonhosted.org/Flask-Mail/)  

# <span style="color: #3a9fd1;">Post</span><span style="color: #FFD700;">ly</span>


**Postly** — дипломний проект, в якому було реалізовано повноцінний веб-додаток на Flask із модульною архітектурою, захищеними формами через Flask-WTF із CSRF-токенами та відновленням паролю через email, ролями користувачів (адмін, модератор, звичайний користувач) із Flask-Login, ORM-моделями User, Post, Comment і Role на SQLAlchemy з міграціями через Flask-Migrate, адаптивним інтерфейсом на Bootstrap 4 та Jinja2-шаблонами, email-верифікацією при реєстрації і коментарі через Flask-Mail і набором модульних тестів на unittest.

## 📦 <span style="color: #3a9fd1;">Особливості

- Структурована архітектура Flask-додатку  
- Використання розширень: Flask-WTF, Flask-Migrate, Flask-Login, Flask-Mail  
- Підтримка міграцій бази даних через Flask-Migrate  
- Відправка email-повідомлень через Flask-Mail  
- Вбудовані модульні тести  
## 📊 <span style="color: #3a9fd1;"> Функціонал додатку

| Модуль / Функція           | Опис                                                                                   |
|----------------------------|----------------------------------------------------------------------------------------|
| **Аутентифікація**         | Реєстрація, вхід/вихід користувачів, відновлення паролю через email                    |
| **Керування профілем**     | Перегляд і редагування профілю, завантаження аватара                                    |
| **Ролі та права доступу**  | Адміністратор може керувати користувачами, звичайний користувач – лише свій профіль     |
| **Публікація постів**      | Створення, редагування, видалення записів блогу                                         |
| **Коментування**           | Додавання коментарів до постів, модерація (адмін)                                      |                                        |
| **Міграції БД**            | Ініціалізація, створення й застосування міграцій через Flask-Migrate                    |
| **Форми та валідація**     | Підтримка Flask-WTF, захист від CSRF                                                     |
| **Email-повідомлення**     | Підтвердження реєстрації, відновлення паролю, сповіщення про активність через Flask-Mail |
| **Тести**                  | Модульні тести для основних функцій додатку                                             |


## 🛠 <span style="color: #3a9fd1;"> Встановлення

```bash
# Клонуємо репозиторій
git clone https://github.com/YehorSeniuk1111/Postly.git
cd Postly

# Створюємо та активуємо віртуальне оточення
python -m venv venv
source venv/bin/activate      # для Windows: venv\Scripts\activate

# Встановлюємо залежності (development)
pip install -r requirements/dev.txt
# Встановлюємо залежності (production)
pip install -r requirements/prod.txt
```
### <span style="color: #ff9fd1;">Встановлюємо змінні оточення
```bash
# Встановлюємо вказівник на стартовий модуль
export FLASK_APP=flasky.py
export FLASK_ENV=development  # для режиму розробки
```

### <span style="color: #ff9fd1;">Ініціалізація бази даних
```bash
# Ініціалізуємо міграції
flask db init
flask db migrate -m "Initial migration"
flask db upgrade
```

### <span style="color: #ff9fd1;">Запускаємо сервер
```bash
flask run
```
## 🧪<span style="color: #3a9fd1;"> Тестування
```bash
python -m unittest discover tests
```


