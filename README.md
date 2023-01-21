# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone into the repository and create dataproject.

### STEP 2:
Create myapp and do the necessary changes in settings.py

### STEP 3:
Write the codes in models.py and admin.py and runserver to get the Employee table output.

## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin

class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()    

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

admin.py

from django.contrib import admin
from.models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```
## OUTPUT
![emp](https://user-images.githubusercontent.com/119104131/213872215-33f0e98e-04f7-4a9c-a336-0333fbe7d99c.jpg)

## RESULT
The ORM Employee table is created successfully.
