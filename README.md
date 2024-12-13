# Ex02 Django ORM Web Application
# Date:20/09/2024
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
        from django.contrib import admin
        from .models import Loan,LoanAdmin
        
        admin.site.register(Loan,LoanAdmin)
    
    
    models.py
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


# ER DIAGRAM

![WhatsApp Image 2024-12-13 at 10 30 22_db3078e1](https://github.com/user-attachments/assets/73e275f7-1d5b-44ef-9aae-1905e56266ae)

# OUTPUT
![WhatsApp Image 2024-12-13 at 10 30 40_525f8caf](https://github.com/user-attachments/assets/9cce9b4f-d2f5-4240-a1c1-2b8ecf9d4838)
![image](https://github.com/user-attachments/assets/df8e9157-d719-4652-ada0-5759e3a16c59)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
