# shpesfba
SHPE San Francisco Bay Area Website -- [www.shpesfba.org](http://www.shpesfba.org)
* Created by: Luis Cuellar
* Contributions by: Patricia Carranza

# Contents
* Installation
  * MacOS
  * Windows
 * Development
 * Deploying the Site
 * Django Admin Panel

# Installation
1. Clone project
`git clone https://github.com/shpe-sfba/shpesfba.git`
2. Create a file named `.env` at the root of the project directory and add the following lines (get the real values from Luis/Patty).
```
export SMTP_SERVER='email.email.com'
export SMTP_PASSWORD='password'
export SMTP_USER='user@email.com'
export SECRET_KEY='SUPER_SECRET_KEY'
```

## MacOS
3.Install python-virtualenv:
`sudo apt-get install python-virtualenv`

4. Setup Python environment by running the following commands
```
virtualenv venv
source venv/bin/activate (on windows venv\Scripts\activate.bat)
pip install -r requirements.txt
source .env
python manage.py migrate
python manage.py collectstatic
python manage.py runserver
```

## Windows

# Development
## MacOS
Run the following commands and then navigate to localhost:8000
```
source venv/bin/activate
source .env
python manage.py runserver
```
Note:
* While running the server any code changes made will be automatically reflected
* After making any changes to the models, run:
```
python manage.py makemigrations
python manage.py migrate
```

# Deploying the Site
`./deploy.sh`

# Django Admin Panel
