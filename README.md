# EX01 Developing a Simple Webserver

# Date:18-11-2026
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
views.py
'''
from django.shortcuts import render

def home(request):
    return render(request,'new.html')

'''
urls.py
'''
"""
URL configuration for web project.

The `urlpatterns` list routes URLs to views. For more information please see:
    https://docs.djangoproject.com/en/6.1/topics/http/urls/
Examples:
Function views
    1. Add an import:  from my_app import views
    2. Add a URL to urlpatterns:  path('', views.home, name='home')
Class-based views
    1. Add an import:  from other_app.views import Home
    2. Add a URL to urlpatterns:  path('', Home.as_view(), name='home')
Including another URLconf
    1. Import the include() function: from django.urls import include, path
    2. Add a URL to urlpatterns:  path('blog/', include('blog.urls'))
"""
from django.contrib import admin
from django.urls import path
from serverapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.home,name='home'),
]
'''
new.html
'''
<html>
    <head>
        <title>EXPERIMENT</title>
    </head>
     <body>
         <table>
            <style>
                table,tr,th,td{
                     width:60%;
                     border:3px solid rgb(206, 19, 175);
                     border-collapse:collapse;
                     margin-left: auto;
                     margin-right: auto;
                     table-layout: fixed;
                }
                th,td{
                    font-size: 20px;
                    padding: 15px;
                }
                body{
                    background-image: url(" /static/laptop.img.jpeg");
                    background-size:cover;
                    background-repeat:no-repeat;
                }
                caption{
                    font-weight: bold;
                    font-size: 30px;
                }
            </style>
            <caption>LAPTOP CONFIGURATION</caption>
            <tr>
                <th> Device Name </th>
                <td>  TL15-53M-G2 </td>
            </tr>
            <tr>
                <th> Processor </th>
                <td>  Intel(R) Core(TM) 5 210H (2.20 GHz)  </td>
            </tr>
            <tr>
                <th> Installed RAM </th>
                <td> 16.0 GB (15.7 GB usable) </td>
            </tr>
            <tr>
                <th>Graphics card</th>
                <td>Intel(R) Graphics (128 MB) </td>
            </tr>
            <tr>
                <th>Storage</th>
                <td>120 GB of 477 GB used</td>
            </tr>
            <tr>
                <th> Device ID   </th>
                <td>  DB084765-DA2D-41EA-9FC1-2C87B0FF08AA  </td>
            </tr>
            <tr>
                <th>  Product ID   </th>
                <td>   00342-42954-08683-AAOEM </td>
            </tr>
            <tr>
                <th>  System type  </th>
                <td>   64-bit operating system, x64-based processor </td>
            </tr>
            <tr>
                <th>  Pen and touch </th>
                <td>  No pen or touch input is available for this display  </td>
            </tr>
            <tr>
                <th> Edition   </td>
                <td>  Windows 11 Home Single Language  </td>
            </tr>
            <tr>
                <th>  Version  </th>
                <td> 25H2   </td>
            </tr>
            <tr>
                <th>  OS build  </th>
                <td> 26200.9974  </td>
            </tr>
            <tr>
                <th> Experience   </th>
                <td>   Windows Feature Experience Pack 1000.26100.385.0 </td>
            </tr>
         </table>
    </body>
</html>
'''
# OUTPUT:
<img width="1920" height="1080" alt="WEB EXP-1" src="https://github.com/user-attachments/assets/08eaa660-e047-406d-9987-71924d8610af" />


# RESULT:
The program for implementing simple webserver is executed successfully.
