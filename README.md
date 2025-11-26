# Ex02 Django ORM Web Application
# Date:26.11.25
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 cars

# PROGRAM
admin.py

from django.contrib import admin
from .models import car

class carAdmin(admin.ModelAdmin):
    list_display = ['car_name','car_price','car_model','car_color']

admin.site.register(car, carAdmin)

model.py
from django.db import models

class car(models.Model):
    car_name = models.CharField(max_length=20)
    car_price = models.IntegerField()
    car_model = models.CharField(max_length=20)
    manufacture_date = models.DateField()
    car_color=models.CharField()

    def __str__(self):
        return self.car_name
# OUTPUT
Include the screenshot of your admin page.

<img src="C:\Users\acer\OneDrive\Pictures\Screenshots\Screenshot 2025-11-26 091705.png">

<img src="C:\Users\acer\OneDrive\Pictures\Screenshots\Screenshot 2025-11-26 093744.png">

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
