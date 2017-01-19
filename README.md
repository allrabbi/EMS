# Examination Management System <a href="http://www.djangoproject.com/"><img src="https://www.djangoproject.com/m/img/badges/djangomade124x25.gif" border="0" alt="Made with Django." title="Made with Django." /></a>

## Setup
1. Clone the repo
	```
	git clone https://github.com/faheel/examination-management-system.git
	cd examination-management-system
	```

2. Create virtual environment (Python 3.5)
	```
	sudo apt install python3-dev python-virtualenv
	virtualenv --python=/usr/bin/python3.5 ve
	```
	`ve` is the name of the virtual environment

3. Activate virtual environment
	```
	source ve/bin/activate
	```

4. Install Django
	```
	pip install django
	```

### Create a PostgreSQL database
1. Install PostgreSQL
	```
	sudo apt install postgresql postgresql-contrib libpq-dev
	```

2. Open the PostgreSQL shell
	```
	sudo -u postgres psql postgres
	```

3. Create a user with the name `dev`
	```
	CREATE USER dev;
	```

4. Create a database with the name `ems`
	```
	CREATE DATABASE ems OWNER dev;
	```
	Now exit the PostgreSQL shell by entering `\q`. You should be back in the shell with `ve` activated

5. Apply migrations
	```
	python3.5 manage.py migrate
 	```

#### Create Django superuser
```
python3.5 manage.py createsuperuser --username admin
```

**Setup is now complete!** :tada:

## Launch
First, make sure that the virtual environment we created, i.e. `ve`, is activated. Then run
```
python3.5 manage.py runserver
```
Once the development server has started, you may visit [http://127.0.0.1:8000/](http://127.0.0.1:8000/) to check out the app.
