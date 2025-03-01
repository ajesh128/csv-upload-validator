# csv-upload-validator
The repository contains an API that allows users to upload csv file containing user data

##  use correct version of Python when creating VENV
python3 -m venv venv

##  activate on Unix or MacOS
source venv/bin/activate

##  activate on Windows (cmd.exe)
venv\Scripts\activate.bat

##  activate on Windows (PowerShell)
venv\Scripts\Activate.ps1

## Setting up requirement.txt
pip install -r requirements.txt

## Main libraries used here are
    Django==5.1.6
    djangorestframework==3.15.2
    pandas==2.2.3
    redis==5.2.1

## How to set up/ run application
    > Clone the repository by this link https://github.com/ajesh128/csv-upload-validator.git
    > Install all the requirements using the command "pip install -r requirements.txt"
    > python manage.py runserver

## Usage
    > A post request is there to handle the csv data (upload/csv/data)

## Creating .env file
cp dotenv.sample .env
    

#### Start Celery

Celery is needed for background tasks.

Follow the url and install and configure rabbitMQ which the message broker url for celery.
https://redis.io/docs/latest/operate/oss_and_stack/install/install-redis/

```
celery -A user_data_validator worker --loglevel=INFO
