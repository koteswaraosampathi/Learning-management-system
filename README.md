# Learning-management-system
#!/usr/bin/env python 
"""Django's command-line utility for administrative tasks.""" 
 
import os 
import sys 
 
 
def main(): 
"""Run administrative tasks.""" 
os.environ.setdefault('DJANGO_SETTINGS_MODULE', 
'teaching_blog.settings') 
try: 
from django.core.management import execute_from_command_line 
except ImportError as exc: 
raise ImportError( 
"Couldn't import Django. Are you sure it's installed and " 
"available on your PYTHONPATH environment variable? Did you " 
"forget to activate a virtual environment?" 
) from exc 
execute_from_command_line(sys.argv) 
 
 
if  name == ' main ': 
main() 
<!DOCTYPE html> 
<html lang="en" dir="ltr"> 
<head> 
{% load static %} 
<meta charset="utf-8">
<title>{%block title%}{%endblock%}</title> 
<link rel="stylesheet" 
href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384- 
JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDG 
MN5t9UJ0Z" crossorigin="anonymous"> 
<link rel="stylesheet" href="{% static 'css/master_css.css' %}"> 
 
</head> 
<body> 
<!-- navigation bar --> 
<nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top 
scrolling-navbar"> 
<div class="container" > 
<a class="navbar-brand" href="{% url 'index' %}" 
style="color:#ff5722;" >Home</a> 
<button class="navbar-toggler" type="button" data- 
toggle="collapse" data-target="#basicExampleNav" 
aria-controls="basicExampleNav" aria-expanded="false" 
aria-label="Toggle navigation"> 
<span class="navbar-toggler-icon"></span> 
</button> 
<div class="collapse navbar-collapse" id="basicExampleNav" > 
<ul class=" navbar-nav mr-auto smooth-scroll " > 
<li class="nav-item"> 
<a class="nav-link" href="{% url 
'curriculum:standard_list' %}">Curriculum</a> 
</li> 
{% if user.is_superuser %} 
<li class="nav-item "> 
<a class="nav-link" href="{% url 'admin:index' 
%}">Admin</span> </a>  
%}">Logout</a> 
%}">Login</a> 
</li> 
{%endif%} 
{% if user.is_authenticated %} 
<li class="nav-item "> 
<a class="nav-link" href="{% url 'user_logout' 
 
</li> 
{% else %} 
<li class="nav-item "> 
<a class="nav-link" href="{% url 'user_login' 
 
</li> 
<li class="nav-item " > 
<a class="nav-link" href="{% url 'register' 
%}">Register</span> </a> 
</li> 
{% endif %} 
<li class="nav-item"> 
<a class="nav-link" href="{% url 'contact' %}">Contact 
Us</a>  
</li> 
<li class="nav-item"> 
<a class="nav-link" href=>GitHub</a> 
</li> 
<li class="nav-item"> 
<a class="nav-link" 
href="https://www.youtube.com/c/LearningBots">Youtube</a> 
</li> 
 
</ul> 
</div> 
</div> 
</nav> 
{% block image_block %} 
{% endblock %} 
 <div class="container"> 
{%block content%} 
{%endblock%} 
</div> 
<footer class="page-footer" style="background-color:#b2ebf2;"> 
<div class="container"> 
<div class="row mt-4"> 
<div class="col-md-4 mt-4"> 
<h3>About Us</h3> <br> 
<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim 
ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex 
ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit 
esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat 
non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p> 
</div> 
<div class="col-md-4 mt-4"> 
<h3>Other Useful Stuff</h3> 
<ul> 
<li>Item 1</li> 
<li>Item 2</li> 
<li>Item 3</li> 
</ul> 
</div> 
<div class="col-md-4 mt-4"> 
<h3>Contact Us</h3> 
<ul> 
<li>Address: Nearest you, state, country</li> 
<li>info@gmail.com</li> 
<li>contact number</li> 
</ul> 
</div> 
</div> 
<div class="footer-copyright text-center py-3"> 
<p></p> 
</div> 
</div> 
</footer> 
 
<script src="https://code.jquery.com/jquery-3.5.1.slim.min.js" 
integrity="sha384- 
DfXdz2htPH0lsSSs5nCTpuj/zy4C+OGpamoFVy38MVBnE+IbbVYUew+Or 
CXaRkfj" crossorigin="anonymous"></script> 
<script 
src="https://cdn.jsdelivr.net/npm/popper.js@1.16.1/dist/umd/popper.min.js" 
integrity="sha384- 
9/reFTGAW83EW2RDu2S0VKaIzap3H66lZH81PoYlFhbGU+6BZp6G7niu 
735Sk7lN" crossorigin="anonymous"></script> 
<script 
src="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js" 
integrity="sha384- 
B4gt1jrGC7Jh4AgTPSdUtOBvfO8shuf57BaghqFfPlYxofvL8/KUEfYiJOM 
MV+rV" crossorigin="anonymous"></script> 
<script type="text/javascript" src="{% static 'js/index.js' %}"></script> 
</body> 
</html> 
