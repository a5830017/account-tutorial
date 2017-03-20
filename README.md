# account-tutorial

#### Follow this https://github.com/a5830017/account-web-app if you can't understand and create account app

#### Tutorial 1 Setup
- **create project**
1. run django-admin startproject project_name and run server to check it
2. run python manage.py startapp app_name
3. create urls.py in app directory (same directory have view.py)
4. add url(r'^polls/', include('polls.urls')), in urls.py of project (in second directory)


-----------------------------------------------------------------------------------------------------------------------------------

#### Tutorial 2 create model
- **about model**
    
    you should design your app and look it in table style
- **create model**
    
    after you have idea now you can create model

    look and try to understand this guide :

        class Account(models.Model): ===> Name/Type of table
            account_text = models.CharField(max_length=200) ===> } head in table
            total_money = models.IntegerField(default=0)    ===> } head in table
-----------------------------------------------------------------------------------------------------------------------------------

#### Tutorial 3 web page
- **views**
    
    in file views.py you can create any function or class to make web page respond with user
    
    Example function in view.py :
    
        def addlist(request, account_id):
            account = get_object_or_404(Account, pk=account_id)
            return render(request, "account/addlist.html", {'account': account },)
- **urls**
    in file urls.py use this file to create urls pattern and call function or class in view.py
    
    Example function in urls.py :
        
        urlpatterns = [
            url(r'^(?P<account_id>[0-9]+)/addlist/$', views.addlist, name='addlist'),
        ]

- **template**
    use by views.py use for create static style in web page or create user input
    
    to use template follow this link https://docs.djangoproject.com/en/1.10/intro/tutorial03/#use-the-template-system

-------------------------------------------------------------------------------------------------------------------------------------
[Wiki version](https://github.com/a5830017/account-tutorial/wiki)
