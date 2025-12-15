# Ex.06 Book Front Cover Page Design
# Date:13-12-2025
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
views.py
```
from django.shortcuts import render
def book_cover(request):
    return render(request,'cover.html')
```
urls.py
```
from django.contrib import admin
from django.urls import path
from bookapp import views
urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.book_cover),
]
```
cover.html
```
<!DOCTYPE html>
{% load static %}
<html lang="eng">
    <head>
        <meta charset="UTF-9">
        <meta name="viewsport" content="width=device-width, initial-scale=1.0">
        <title>Book Cover</title>
    <style>
        #cover{
            background-image:url("{% static 'alone.jpg' %}");
            height: 650px;
            width: 400px;
            position: relative;
            margin:50px auto;
            background-size: 100% 100%;
        }
        #border{
            top: 20px;
            bottom: 20px;
            left: 20px;
            right: 20px;
            border: 4px solid black;
            position: absolute;
        }
        #cover h1{
            text-align: center;
            font-style: oblique;
            color: rgb(240, 172, 45);
        }
        #cover h2{
            text-align: center;
            font-style: oblique;
        }
        #cover img{
            position: absolute;
            bottom: 50px;
            right: 20px;
            height: 120px;
            width: 120px;
            border-radius: 20px;
        }
        #cover h6{
            position: absolute;
            right: 30px;
            bottom: 0px;
            color: whitesmoke;

        }
    </style>
    <body>
        <div id="cover">
            <div id="border">
                <h1>THE LAST VOYAGE</h1>
                <h2>a novel of mystery and solitude </h2>
                <hr color="black" width="100%" size="4">
                <img src="{% static 'gosh.png' %}">
                <h6>BY AMITAV GHOSH</h6>

            </div>
        </div>

    </body>
    </head>
</html>
```

# OUTPUT:
![alt text](<Screenshot 2025-12-15 135608.png>)
# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
