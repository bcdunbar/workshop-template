# Workshop Template

This repo serves as a template to copy and paste workshop material. Simply, copy and paste example code into the `app.py` file, save, and then run the code.

### About the Repo

`app.py`

This is the entry point to your application, it contains your Dash app code.
This file must contain a line that defines the `server` variable:
```server = app.server```


`.gitignore`

Determines which files and folders are ignored in git, and therefore
ignored (i.e. not copied to the server) when you deploy your application.
An example of its contents would be:

```
venv
*.pyc
.DS_Store
.env
```


`Procfile`

Declares what commands are run by app's containers. This is commonly,
```web: gunicorn app:server --workers 4``` where app refers to the file
`app.py` and server refers to the variable named server inside that file.
gunicorn is the web server that will run your application, make sure to
add this in your requirements.txt file.


`requirements.txt`

Describes the app's python dependencies. For example,

```
dash==0.21.1
dash-auth==1.0.1
dash-renderer==0.11.3
dash-core-components==0.22.1
dash-html-components==0.9.0
```

`/assets`

An optional folder that contains CSS stylesheets, images, or
custom JavaScript files. [Learn more about assets](/external-resources).

### Setup Repo

First clone the repo:

```
git clone https://github.com/bcdunbar/workshop-template.git
```

Next, create a virtualenv and pip install the dependencies:

```
cd workshop-template

pip install virtualenv
virtualenv venv
source venv/bin/activate

pip install -r requirements.txt
```

or on a windows machine
```
cd workshop-template

pip install virtualenv
virtualenv venv
venv/Scripts/activate

pip install -r requirements.txt
```

### Run examples

Simply copy and paste the example code into the `app.py` file, save, and then in the command line type:

```
python app.py
```
