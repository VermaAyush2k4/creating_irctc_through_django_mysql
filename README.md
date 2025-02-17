# creating_irctc_through_django_mysql

It offers users the ability to check seat availability, make reservations, and purchase tickets, simplifying the ticketing process and enhancing the travel experience. And also provides administrative functionalities. The admin can add new trains, cancel existing ones, and view passenger lists.

DOWNLOAD GIT BASH  
open new terminal  
select gitbash from plus button:  

> python -m venv environment-name  
> source environment-name/Scripts/activate  
> pip freeze  
> pip install django  
> pip freeze  
> django-admin startproject project-name  
> cd project-name  
> django-admin startapp appname  
> ls  
> python manage.py migrate  
> python manage.py createsuperuser  
     username --optional  
     email --optional  
     password --give your password  
     password(again) --give your password  
> python manage.py runserver  
> go to your created app and create a new templates folder(html files)  
> now create a new floder in templates appname  
> now create a new file in the templates\appname folder and name it        
  filename.html   
> go to settings.py file and insert appname in installed apps  
         ('app-name',)  
> go to url.py file  
      in second import line afte path add ",include"  
          (from django.urls import path,include)  
      in url patterns:  
          add,  
          path('',include("app-name.urls")),  
> go to views.py click on views.py and create a new file called "urls.py"  
    in the created urls.py file enter the below codes:  
	from.import views  
	from django.urls import path  

	urlpatterns = [  
		path("",views.file-name, name="file-name"),  
		]  
> go to views.py  
     type the below code:  

	def file-name(request):  
		context={}  
		return render(request, "app-name/file-name.html", context)  


Requirements:
	1. MySQL Installation 
 
	2. Visual Studio Code Setup
 
	3. Python Installation
 
	4. Django Installation
   
Common Extensions for Django Development in VS Code:  
	1. Python Extension
 
	2. Django Extension
 
	3. Git Extension  
 
	4. Database Extension (optional)
 
Clone or download this repository to your local machine:

1)Navigate to the project directory using the terminal in VS Code.  

2)Set up your MySQL database configurations in your Django project's settings.

3)Run migrations using the python manage.py migrate command.  

4)Create a superuser using the python manage.py createsuperuser command.

5)Start the development server with python manage.py runserver.


