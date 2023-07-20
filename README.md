# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![ERdiagram](https://github.com/DariusRijin07/django-orm-app/assets/138849120/76d0e4b8-47c1-479b-bade-0f5d4283161d)


## DESIGN STEPS

### STEP 1: 

create a table using required details in django-ORM

### STEP 2: 

upload the python code

### STEP 3:

Push the code to github


## PROGRAM

### models.py:
from django.db import models
from django.contrib import admin

class Student (models.Model):
    referencenumber=models.CharField(primary_key=True,max_length=20,help_text="reference number")
    name=models.CharField(max_length=50,help_text="name")
    age=models.IntegerField(null=False,blank=False,help_text="age")
    email=models.EmailField(blank=False,null=False,unique=True,max_length=100,help_text="email")
    mobile=models.IntegerField(default=0,help_text="mobile")


class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','mobile') 

### admin.py:
from django.contrib import admin
from .models import Student,StudentAdmin

admin.site.register(Student,StudentAdmin)    

## OUTPUT

### student:
![Student](https://github.com/DariusRijin07/django-orm-app/assets/138849120/e1f3b266-ff84-487a-9f1b-ed6f2855016e)


### error:
![Error](https://github.com/DariusRijin07/django-orm-app/assets/138849120/3a4d3d9e-833c-473f-a2ea-460579557f2e)


## RESULT:
The Program is executed successfully.
