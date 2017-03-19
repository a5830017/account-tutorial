# account-tutorial
Tutorial 1 Setup
- create project
1. run django-admin startproject project_name and run server to check it
2. run python manage.py startapp app_name
3. create urls.py in app directory (same directory have view.py)
4. add url(r'^polls/', include('polls.urls')), in urls.py of project (in second directory)


-----------------------------------------------------------------------------------------------------------------------------------

Tutorial 2 create model
- about model
you should design your app and make it in table style
- create model
after you have idea now you can create model

look and try to understand this guide :

    class Account(models.Model): ===> Name/Type of table|
        account_text = models.CharField(max_length=200) &and&
        total_money = models.IntegerField(default=0)    ===> } head in table
-----------------------------------------------------------------------------------------------------------------------------------

Tutorial 3 
