# Expense Tracker App built with Django (Python)
This is an Expense Tracker app, built using Django (Python).


## To use Email Authentication and Verification Features
Create a '.env' file along with 'manage.py' files 
Then, add following configurations

```.env
export EMAIL_HOST_PASSWORD=your_email_password
export EMAIL_HOST_USER=your_email_address
export DEFAULT_FROM_EMAIL=your_email_address
export EMAIL_HOST=smtp.gmail.com
```

*The above example is using gmail host, 'You might need to change based on your email-service'*

Also on 'settings.py' file you need to add following settings at the bottom
``` python
EMAIL_HOST = os.environ.get('EMAIL_HOST')
EMAIL_HOST_USER = os.environ.get('EMAIL_HOST_USER')
EMAIL_USE_TLS = True
DEFAULT_FROM_EMAIL = os.environ.get('EMAIL_HOST_USER')
EMAIL_PORT = 587
EMAIL_HOST_PASSWORD = os.environ.get('EMAIL_HOST_PASSWORD')
```

And before starting server, use the following command
```
$ source .env
```
