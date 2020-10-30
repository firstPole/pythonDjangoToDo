# pythonDjangoToDo

## Python django Project which consist of multiple apps for step by step learning

## Python and django version
* Python 3.x
* django 3.1.2

**Create django template project using**
*python manage.py startproject

- It consists of 3 applications for learning purpose (hello, newyear, ToDo-Tasks)
* To create 3 different application under django project
```python manage.py startapp```

- Under the project settings.py, include abvoe creted apps under 'INSTALLED_APPS'
- Under urls.py specify the urlpatterns by including paths for 3 different apps under 'urlpatterns' like 
```urlpatterns = [
    path('admin/', admin.site.urls),
    path('hello/',include("hello.urls")),
    path('tasks/',include("tasks.urls")),
    path('newyear/',include("newyear.urls"))
] ```

* Under each application add urls.py to specify local routing for that speicific application like
```urlpatterns = [
    path("",views.index,name="index"),
    path("add", views.add,name="add")
]```
