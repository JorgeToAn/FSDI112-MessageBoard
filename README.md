# FSDI 112 - Message Board
This project counts as assignment #3 for FSDI 112.
It presents an app that lets you view posts in a list, in detail and create new posts through a form.

NOTE: The project doesn't have a home page, please go to '/posts' to enter the site.

## Heroku URL
https://warm-springs-26515.herokuapp.com/

## Heroku setup instructions
https://dashboard.heroku.com/apps
1. Install Heroku CLI (it’s a local installation)
2. Be sure to create a git repository for the project
3. Install gunicorn – pip3 install gunicorn
4. Configure gunicorn – gunicorn config.wsgi
5. Install whitenoise – pip3 install whitenoise
6. Configure config/settings.py for whitenoise
-> http://whitenoise.evans.io/en/stable/ 
-> http://whitenoise.evans.io/en/stable/django.html?highlight=local%20noserver#using-whitenoise-in-development
7. Update project’s requirements.txt
8. Collect static files – python3 manage.py collectstatic
9. Update ALLOWED_HOSTS on settings.py to include localhosts and '.herokuapp.com'
10. Create a Procfile in your project and include 'web: gunicorn config.wsgi --log-file -'
11. Log in to Heroku – heroku login
12. Create the Heroku app – heroku create
13. Push to the Heroku repository – git push heroku main
14. Open the server – heroku open
