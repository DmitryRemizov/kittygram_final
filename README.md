![Kittygram workflow](https://github.com/rdk7777/kittygram_final/actions/workflows/main.yml/badge.svg)

# Kittygram 

Социальная сеть для любителей котов. Можно регистрироваться, загружать фото питомцев, ставить лайки и комментировать.

##  Стек технологий
- **Backend:** Python 3.12, Django 5.1, DRF, PostgreSQL, Gunicorn
- **Frontend:** React 18, Node.js 18
- **Инфраструктура:** Docker, Nginx, GitHub Actions, Telegram Bot

##  Запуск локально
1. Клонируйте репозиторий и перейдите в папку:
   git clone https://github.com/rdk7777/kittygram_final.git
   cd kittygram_final
   
2. Создайте файл `.env` по примеру `.env.example`
3. Запустите контейнеры:
   docker compose up -d --build
   
4. Накатите миграции и соберите статику:
  
   docker compose exec backend python manage.py migrate
   docker compose exec backend python manage.py collectstatic --noinput
   
5. Создайте админа:
   
   docker compose exec backend python manage.py createsuperuser
   

Проект доступен по адресу: [http://localhost:9000](http://localhost:9000)

## Автор
[@rdk7777](https://github.com/rdk7777)
