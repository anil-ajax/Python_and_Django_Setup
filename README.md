## Install Python, Django on Windows* and create a sample project
* Following steps have been executed on Windows 10 with Python 3.7
## Step 1: Install Python
Download and install Python from https://www.python.org/downloads/
During installation make sure you tick the check box next to ‘Add Python 3.* to PATH’ 
Finally, in command line check if Python successfully installed: python --version
## Step 2: Install PIP. It’s a package manager for Python
Run in command line:
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
python get-pip.py
## Step 3: Install virtualenv and virtualenvwrapper
virtualenv and virtualenvwrapper provide a dedicated environment for each Django project you create. While not mandatory, this is considered a best practice and will save you time in the future when you’re ready to deploy your project. 
pip install virtualenvwrapper-win
mkvirtualenv myproject
workon myproject
## Step 4: Install Django
pip install django
## Step 5: Project setup 
mkdir django_project 
cd django_project
django-admin startproject locallibrary 	– locallibrary is name of your project
cd locallibrary
python manage.py startapp catalog
python manage.py makemigrations
python manage.py migrate

## Step 6: Start application  
python manage.py runserver
Front end URL: http://127.0.0.1:8000/ 
Admin URL: http://127.0.0.1:8000/admin/ 
Note: next time you do runserver, make sure you activate virtual environment using command:
workon myproject
Useful Info
The catalog/ directory contains files for the views, models, and other parts of the application. Open these files and inspect the boilerplate. 
Rotes to be added in urls.py (in django_project\locallibrary\locallibrary). URL-mapping for the Admin site has already been added here.
