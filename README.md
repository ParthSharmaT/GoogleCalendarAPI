
# Google Calendar Event List API

It is an API to List the Events in Google Calendar of a Google User using Google OAuth2.0 and Google Calendar API.

## Getting Started

### Fork and clone locally

Fork [Google CalendarAPI](https://github.com/ParthSharmaT/GoogleCalendarAPI.git) repository and clone at your local 

- Fork and Clone the repo using
```
$ git clone https://github.com/ParthSharmaT/GoogleCalendarAPI.git
```

### Setting Environment First Time

#### Basic Requirements 
1. [Python](https://www.python.org/downloads/)
1. [pip](https://pip.pypa.io/en/stable/installation/)

#### Creating [Virtual Environment](https://docs.python.org/3/library/venv.html) 

A virtual environment is a tool that helps keep dependencies required and the project isolated. If you wish to install a new library and write
```
pip install name_of_library
``` 
on the terminal without activating an environment, all the packages will be installed globally which is not a good practice if you’re working with different projects on your computer.

If this sounds a bit complicated, don’t worry so much because a virtual environment is just a directory that will contain all the necessary files for our project to run.

**Installing venv (required once)**

**Windows**
```
py -m pip install --user virtualenv
py -m venv env
```
**Linux**
```
python3 -m pip install --user virtualenv
python3 -m venv env
```

You have to start virtual environment everytime you start new terminal -

**Windows**

Using gitbash
```
. env/Scripts/activate
```
Using Powershell
```
. env\Scripts\activate
```
**Linux**
```
source env/bin/activate
```

#### Installing Requirements 

**Windows**
```
pip install -r requirements.txt
```
**Linux**
```
pip install -r requirementstxt
```
#### Setting up Environment File

**Configuring Environment Variables**

Make environment file by copying the example file -


#### Migrating Database
**Windows**
```
python3 manage.py migrate
```
**Linux**
```
python3 manage.py migrate
```

#### Create Superuser
**Windows**
```
python3 manage.py createsuperser
```
**Linux**
```
python3 manage.py createsuperser
```

### Starting Development Server
**Windows**
```
py manage.py runserver
```
**Linux**
```
python3 manage.py runserver
``` 

### Leaving the virtual environment
```
deactivate
```

### Update requirements file (Critical)
If you have installed new dependency, the pip freeze command lists the third-party packages and versions installed in the environment. 

**Windows**
```
pip freeze > requirements.txt
```
**Linux**
```
pip3 freeze > requirements.txt
```

### Update Database  
Everytime you change db models, you need to run makemigrations and migrate to update on database.

**Windows**
```
py manage.py makemigrations
py manage.py migrate
```
**Linux**
```
python3 manage.py makemigrations
python3 manage.py migrate

```


## How to use
**Method : GET**
```
url: http://localhost:8000/rest/v1/calendar/init
Response: 
You will be redirected to google authentication page and then to http://localhost:8000/rest/v1/calendar/redirect
```
