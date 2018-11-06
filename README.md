# bizkik - web server

Django web server for bizkik website

Using Python 3.6.4 / Django 2.0.3 / PosgreSQL 10.5

## How to install

## Step 1: Clone Repo / Install Requirements

```
git clone https://github.com/sniperman23/bizkik.git
pip install -r requirements.txt

```

### Step 2: Install and Setup PostgreSQL
Once installed:
```javascript
// On the command line
psql

// Create the database
CREATE DATABASE django;

// Create a user
CREATE USER username WITH PASSWORD 'password';

// Allow the user to use the database
GRANT ALL PRIVILEGES ON DATABASE django TO username;
```

### Step 3: Change settings.py
```javascript
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'django',
        'USER' : 'username',
        'PASSWORD' : 'password',
        'HOST' : 'localhost',
        'PORT' : '5432',
    }
}
```

### Step 4: Run Migrations
```
python manage.py migrate
```

### Step 5: Run Server
```
python manage.py runserver
```

Runs on: localhost:8000 

Admin portal: localhost:8000/admin
