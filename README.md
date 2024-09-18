# Ex02 Django ORM Web Application
## Date: 18.09.2024

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## Entity Relationship Diagram:

<img width="963" alt="Bank ORM" src="https://github.com/user-attachments/assets/87b846e0-18df-406d-a276-21a83fe6da4d">

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

```
Models.py 
from django.db import models
from django.contrib import admin
# Create your models here.

class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

class Loandetails(admin.ModelAdmin):
    list_display= ('customer_id','customer_name','account_type','loan_amount','monthly_interest','due_date')

admin.py 
from django.contrib import admin
from .models import Bank,Loandetails

# Register your models here.
admin.site.register(Bank,Loandetails)
```

## OUTPUT
![Django_new3](https://github.com/user-attachments/assets/e1cf7ad6-b50b-40a8-8826-a056253fe2fc)

![Django_new2](https://github.com/user-attachments/assets/e8bd342e-6241-4eb9-ad08-3af742eee115)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
