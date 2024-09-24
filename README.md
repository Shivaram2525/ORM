# EX 03 Django ORM Web Application

## Date: 24-09-2024
# Name: Shivaram M.
# Reg. No.: 212223040195
## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).


## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 bank loan records

## PROGRAM

## Admin.py

```
from django.contrib import admin
from .models import Loan

@admin.register(Loan)
class LoanAdmin(admin.ModelAdmin):
    list_display = ('loan_id', 'customer_name', 'amount', 'interest_rate', 'duration_months', 'start_date')
    search_fields = ('customer_name', 'loan_id')
```

## Models.py

```
from django.db import models

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)  # Auto incrementing primary key
    customer_name = models.CharField(max_length=100)
    address = models.CharField(max_length=255)
    phone_number = models.CharField(max_length=15)
    email = models.EmailField()
    amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.FloatField()
    duration_months = models.PositiveIntegerField()
    start_date = models.DateField()

    def __str__(self):
        return f"Loan ID: {self.loan_id} - {self.customer_name}"
```

## SAMPLE ER DIAGRAM:

![Web_Exp_2(3)](https://github.com/user-attachments/assets/61d6937c-4d6e-4622-94b6-dd81f0610ec8)



## OUTPUT

![Web_Exp_2(1)](https://github.com/user-attachments/assets/78cbaed8-8f3a-40ab-bd2e-5bc415993c41)



![Web_Exp_2(2)](https://github.com/user-attachments/assets/41c1d0fa-6f66-4d02-a934-d820318a1e05)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully
