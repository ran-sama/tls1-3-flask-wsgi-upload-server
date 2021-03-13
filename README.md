# flask-wsgi-upload-server
A powerful and secure upload server for uWSGI and Flask.

## Dependencies:

https://pypi.org/project/Flask/  
https://pypi.org/project/uWSGI/  
https://pypi.org/project/Werkzeug/  
https://pypi.org/project/streaming-form-data/  

## How to launch the server:

```uwsgi --ini /home/ran/uwsgi.ini```

## Screenshots:

![alt text](https://raw.githubusercontent.com/ran-sama/flask-wsgi-upload-server/master/screenshots/login_page.png)

![alt text](https://raw.githubusercontent.com/ran-sama/flask-wsgi-upload-server/master/screenshots/logged_in.png)

![alt text](https://raw.githubusercontent.com/ran-sama/flask-wsgi-upload-server/master/screenshots/upload_dialogue.png)

![alt text](https://raw.githubusercontent.com/ran-sama/flask-wsgi-upload-server/master/screenshots/successful_upload.png)

![alt text](https://raw.githubusercontent.com/ran-sama/flask-wsgi-upload-server/master/screenshots/unauthorized.png)

## Generate your own PBKDF2 credentials:

Edit the [derive_key.py](https://github.com/ran-sama/tls1-3-flask-wsgi-upload-server/blob/master/derive_key.py#L7) and state your username and password as ONE single string:

```
$ python3 derive_key.py
Your salt (use in the login html):
qNv83XARvwWcGeBYPvbXAg==
Your PBKDF2 key (use in the WSGI code):
b31300bd83a0bfc3e5197df305fbc00b864526f6ac6ac4f91c4352a36fa79088
```

Must edit 
[server_UL.py](https://github.com/ran-sama/tls1-3-flask-wsgi-upload-server/blob/master/server_UL.py) and [login.html](https://github.com/ran-sama/tls1-3-flask-wsgi-upload-server/blob/master/templates/login.html#L112) with your OWN keys. Don't use the defaults.


## License
Licensed under the WTFPL license.
