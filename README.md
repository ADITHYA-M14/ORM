# Ex02 Django ORM Web Application
# Developed by : ADITHYA M
# Register Number : 212224230008
# Date: 25/03/2025
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
admin.py
```
from django.contrib import admin
from .models import Loan,LoanAdmin

admin.site.register(Loan,LoanAdmin)
```
models.py
```
from django.db import models
from django.contrib import admin

class Loan(models.Model):
    loan_id = models.AutoField(primary_key=True)
    customer_name = models.CharField(max_length=100)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)
    interest_rate = models.DecimalField(max_digits=5, decimal_places=2)
    loan_term = models.IntegerField()
    disbursement_date = models.DateField()

class LoanAdmin(admin.ModelAdmin):
list_display=('loan_id','customer_name','loan_amount','interest_rate','loan_term','disbursement_date')
```
![Screenshot 2025-04-08 091701](https://github.com/user-attachments/assets/910cb204-d24e-4ad9-bf1c-94cdb755f32a)

# OUTPUT
![Screenshot 2025-04-08 091734](https://github.com/user-attachments/assets/10c0fa48-f9a8-4854-abff-5654502367f1)

![Screenshot 2025-04-08 091742](https://github.com/user-attachments/assets/3f2cb614-06bc-4706-aff9-75aabea1334c)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
