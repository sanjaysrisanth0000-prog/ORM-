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
<img width="1920" height="1080" alt="Screenshot 2025-11-26 093744" src="https://github.com/user-attachments/assets/7896d67f-ced2-436b-a467-58513f3360c4" />

<img width="1920" height="1080" alt="Screenshot 2025-11-26 091705" src="https://github.com/user-attachments/assets/9206b2bf-8090-4369-81c6-1d3e42eb6043" />


# RESULT
Thus the program for creating a database using ORM hass been executed successfully
