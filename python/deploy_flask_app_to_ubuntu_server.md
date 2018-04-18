# Deploy flask app to ubuntu server

## login to the server
``` ssh root@ip```
## install python and nginx
``` sudo apt-get install python-pip nginx```
## configure nginx
### start nginx
` sudo /etc/init.d/nginx start`
### removethe exsingting configuration file 
`sudo rm /etc/nginx/sites-enabled/default`
### create new configuration file 
`sudo touch /etc/nginx/sites-available/flask_settings` I will create like ..../todo_settings
### connect the configuration file 
`sudo ln -s /etc/nginx/sites-available/flask_settings /etc/nginx/sites-enabled/flask_settings` 
### edit configuration file 
`vi /etc/nginx/sites-enabled/flask_settings`
- edit 
```
server {

    location / {
        proxy_pass http://127.0.0.1:8000;
        proxy_set_header Host $host;
        proxy_set_header X-Real-IP $remote_addr;
    }
}
``` 
### restart nginx
`sudo /etc/init.d/nginx restart`
## set up the python part
### installl virtualenv
`pip install virtualenv`
### create new virtual environtment
```
 mkdir my_flask_app
 cd my_flask_app
 virtualenv env
 source env/bin/activate
 ```
 ### install flask and gunicorn
 ``` bash
 pip install flask gunicorn
 which gunicorn
 touch hello.py
 vi hello.py
 ```
 * edit hellp.py

``` python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
    return 'hello There!!!'
```
### run gunicorn 
`gunicorn hello:app`

