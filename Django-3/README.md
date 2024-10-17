# Building Web Applications in Django

# Django Coursera Week 1
#### This is the code for the auto-grader assignment for week 1 of **Building Web Applications in Django**. This code is to be uploaded to your personal accounts on [PythonAnywhere](https://www.pythonanywhere.com). Please follow the instructions below to do the same and get the site live.

#### *Part 1 - Getting our project live on PythonAnywhere*

##### Step 1: Clone the repository by running the command below in the bash console of your pythonanywhere beginner account.
```
git clone https://github.com/saumyasarkar11/mysite.git
```

##### Step 2: Create virtual environment and make sure you put proper python version(We will be using 3.10 here).
```
mkvirtualenv --python=/usr/bin/python3.10 mysite-env
```

##### Step 3: Install all the requirements for our application.
```
cd mysite
pip install -r requirements.txt
```

##### Step 4: Migrate database for our application followed by generation of a single static file for CSS, JS, images, etc.
```
python manage.py migrate
python manage.py collectstatic
```

##### Step 5: Go to *Web* tab on the top right and click on it. You will see *Create a Web Application* button, click on it. Select python version 3.10, click *Next* click on *Manual Configuration*(make sure you do not click on the “Django” option).

##### Step 6: Change source code and virtualenv location to that of your respective project by changing the username only. Refer to the image below.
<kbd>![Screenshot 2022-11-04 195107](https://user-images.githubusercontent.com/76894046/199999856-3ad8c6c3-6cfe-4e03-ab4b-5e1d4b004c72.png)</kbd>

##### Step 7a: Change the WSGI configuration file by clicking on the link. Clicking the link will lead you to an editor. Refer to the image to locate the required file.
<kbd>![Screenshot 2022-11-04 200245](https://user-images.githubusercontent.com/76894046/200001260-04d166bd-2255-4906-a846-fb85446ec96f.png)</kbd>

##### Step 7b: Just remove everything from the file and paste the below given code. Make sure you change *<your_username>* to your respective username and save the file by clicking *Save* at the top right.
```
import os
import sys

path = '/home/<your_username>/mysite'
if path not in sys.path:
     sys.path.insert(0, path)

os.environ['DJANGO_SETTINGS_MODULE'] = 'mysite.settings'
from django.core.wsgi import get_wsgi_application
application = get_wsgi_application()
```

##### Step 8: Add path for static files. Please change your account username. Refer to the image below.
<kbd>![Screenshot 2022-11-05 003606](https://user-images.githubusercontent.com/76894046/200100588-99c654ec-6c50-4034-8ee2-4680e0d22799.png)</kbd>

##### Step 9: Refresh the site by clicking on the green button at the top of the page. Refer to the image below.
<kbd>![Screenshot 2022-11-04 201043](https://user-images.githubusercontent.com/76894046/200002630-10b80d69-be26-4dd7-828f-334f87193178.png)</kbd>

#### *Part 2 - Configuring our application for the Auto-Grader*

#### Step 1: Visit the url of your deployment with the extension */admin/* (<your_username>.pythonanywhere.com/admin/) to view the application. Login with the credentials "*admin*" and "*password*" as username and password respectively.

#### Step 2: Click on *users* and after logging in and delete the existing user with username "*dj4e*".
<kbd>![Screenshot 2022-11-04 203424 (1)](https://user-images.githubusercontent.com/76894046/200050365-6a1129d3-9bf9-46e2-a7d7-323208c6f3ba.png)</kbd>

##### Step 3: Create a new user with the username and password provided by the auto-grader. Refer to the image below.(Note: The password provided for every coursera student is different)
<kbd>![Screenshot 2022-11-04 203759](https://user-images.githubusercontent.com/76894046/200051687-94dbd2fb-e8b9-4545-ba3e-19be919601fc.png)</kbd>

<kbd>![Screenshot 2022-11-04 204000](https://user-images.githubusercontent.com/76894046/200053304-4df0457c-830d-4377-a0bc-695acca0b929.png)</kbd>

<kbd>![Screenshot 2022-11-04 204335](https://user-images.githubusercontent.com/76894046/200053012-bb6f3401-8eca-422d-a235-d22ebbab747b.png)</kbd>

##### Step 4: Add priviledges to the newly created user by clicking "*Choose All*" and add "*Staff Status*" to the user. Refer to the image below.
<kbd>![Screenshot 2022-11-04 204605](https://user-images.githubusercontent.com/76894046/200054109-89cf2634-94ef-431e-81dc-27441a38d914.png)</kbd>

<kbd>![Screenshot 2022-11-04 204752](https://user-images.githubusercontent.com/76894046/200054215-02e45f04-2afa-46cf-82c0-dfda2a746152.png)</kbd>

##### Step 5: Paste your url in the auto-grader and evaluate.
<kbd>![Screenshot 2022-11-04 205339](https://user-images.githubusercontent.com/76894046/200055686-7decc57f-2c96-4ace-82de-b808180d35ed.png)</kbd>

<p align="center" width="50%"><img src="https://user-images.githubusercontent.com/76894046/200056910-b5c2f2f1-fdf2-4bd8-ae4f-f72df35a0348.jpg" alt="meme"></p>
