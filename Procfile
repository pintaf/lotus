release: chmod u+x scripts/heroku_release.sh && ./scripts/heroku_release.sh
web: gunicorn lotus.wsgi:application -w 4 --threads 4 --preload
worker: celery -A lotus worker -l info
beat: celery -A lotus beat -l info --scheduler django_celery_beat.schedulers:DatabaseScheduler
