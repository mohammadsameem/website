# Ex.07 Restaurant Website
# Date:19/12/2025
# AIM:
To develop a static Restaurant website to display the food items and services provided by them.

# DESIGN STEPS:
## Step 1:
Requirement collection.

## Step 2:
Creating the layout using HTML and CSS.

## Step 3:
Updating the sample content.

## Step 4:
Choose the appropriate style and color scheme.

## Step 5:
Validate the layout in various browsers.

## Step 6:
Validate the HTML code.

## Step 7:
Publish the website in the given URL.

# PROGRAM:
Home.html
~~~
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ARYABHAVAN | HOME</title>
    <link rel="stylesheet" href="{% static 'home.css' %}">
</head>
<body>
<header>
<div style="text-align: center; margin: 40px;">
    <img src="{% static 'ashna.png' %}" alt="LOGO"
         style="display:block;margin:auto;width:300px;height:300px;">

    <h1 style="font-size:80px;font-family:'Cinzel Decorative',cursive;
    color:maroon;margin-top:20px;letter-spacing:3px;
    text-shadow:2px 2px 6px rgba(0,0,0,0.3);">
        Aryabhavan
    </h1>

    <hr style="width:300px;height:4px;border:none;
    background:linear-gradient(to right,transparent,goldenrod,transparent);
    margin:10px auto;border-radius:50px;">

    <p style="font-size:28px;font-family:'Great Vibes',cursive;
    color:#5a3e2b;letter-spacing:2px;font-style:italic;">
        “Where Taste Meets Elegance”
    </p>
</div>

<nav class="container">
<ul>
<li><a href="{% url 'home' %}">Home</a></li>
<li><a href="{% url 'menu' %}">Menu</a></li>
<li><a href="{% url 'administration' %}">Administration</a></li>
<li><a href="{% url 'contact' %}">Contact Us</a></li>
</ul>
</nav>
</header>

<br><br>

<main>
<div class="offer">
<pre><h1 class="head"> DHAMAKKA OFFER!! --------->>> AVAIL UPTO 80% OFF *</h1></pre>
</div>

<br><br>

<div class="container_">
<div id="item1">
<center>
<h2>Our Menu</h2>
<img src="https://images.unsplash.com/photo-1512621776951-a57141f2eefd"
     style="width:250px;height:250px;">
<p>
At Aryabhavan, dining is a celebration of flavour and tradition.
Every dish is prepared with care, warmth, and authenticity,
making each meal feel like home.
</p>
</center>
</div>

<div id="item2">
<center>
<h2>Book A Table</h2>
<img src="https://plus.unsplash.com/premium_photo-1681841594224-ad729a249113"
     style="width:250px;height:250px;">
<p>
Reserve your table at Aryabhavan and enjoy comforting flavours,
warm hospitality, and memorable moments.
</p>
</center>
</div>

<div id="item3">
<center>
<h2>Opening Hours</h2>
<img src="https://plus.unsplash.com/premium_photo-1665203630695-1db105e4ea9d"
     style="width:250px;height:250px;">
<p>
Open daily to serve you delicious meals in a welcoming atmosphere.
Every visit is a celebration at Aryabhavan.
</p>
</center>
</div>
</div>
</main>

<footer>
<div class="footer-bottom">
Made with ♥ by Aryabhavan © 2025. All Rights Reserved.
</div>
</footer>
</body>
</html>
~~~
Menu.html
~~~
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aryabhavan | Menu</title>
<style>
body{
background-image:url("https://c8.alamy.com/comp/EMEY0B/template-for-menu-card-with-cutlery-vector-illustration-EMEY0B.jpg");
background-size:cover;
font-family:'Segoe UI',sans-serif;
}
nav{height:65px;width:70%;margin:auto;margin-top:100px;
background:maroon;border-radius:50px;text-align:center;}
ul{display:flex;justify-content:space-between;align-items:center;}
li{font-size:xx-large;font-family:Impact;}
a{text-decoration:none;color:#f4d03f;}
.container_{display:flex;flex-wrap:wrap;gap:20px;justify-content:center;}
.item1,.item2,.item3,.item4{
width:500px;height:70vh;padding:20px;
box-shadow:0 8px 20px rgba(0,0,0,0.5);}
h2{text-align:center;background:#8B0000;color:white;padding:10px;}
h3{color:#c0392b;border-bottom:2px solid #f4d03f;}
li{display:flex;justify-content:space-between;}
.footer-bottom{text-align:center;padding:15px;background:#333;color:white;}
</style>
</head>

<body>
<header>
<div style="text-align:center;margin:40px;">
<img src="{% static 'ashna.png' %}" style="width:300px;height:300px;">
</div>

<nav>
<ul>
<li><a href="{% url 'home' %}">Home</a></li>
<li><a href="{% url 'menu' %}">Menu</a></li>
<li><a href="{% url 'administration' %}">Administration</a></li>
<li><a href="{% url 'contact' %}">Contact Us</a></li>
</ul>
</nav>
</header>

<!-- MENU CONTENT UNCHANGED -->

<footer>
<div class="footer-bottom">
Made with ♥ by Aryabhavan © 2025. All Rights Reserved.
</div>
</footer>
</body>
</html>
~~~
Adminstration.html
~~~
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Administration | Aryabhavan</title>
<style>
body{background:#fdf1dc;font-family:'Segoe UI';}
.team-container{display:flex;flex-wrap:wrap;gap:30px;justify-content:center;}
.team-member{width:400px;padding:20px;
box-shadow:0 6px 18px rgba(0,0,0,0.2);text-align:center;}
.team-member img{width:120px;height:120px;border-radius:30px;}
nav{height:65px;width:70%;margin:auto;margin-top:100px;
background:maroon;border-radius:50px;text-align:center;}
ul{display:flex;justify-content:space-between;}
a{color:#f4d03f;text-decoration:none;}
.footer-bottom{text-align:center;padding:15px;background:#333;color:white;}
</style>
</head>

<body>
<header>
<div style="text-align:center;margin:40px;">
<img src="{% static 'ashna.png' %}" style="width:300px;height:300px;">
</div>

<nav>
<ul>
<li><a href="{% url 'home' %}">Home</a></li>
<li><a href="{% url 'menu' %}">Menu</a></li>
<li><a href="{% url 'administration' %}">Administration</a></li>
<li><a href="{% url 'contact' %}">Contact Us</a></li>
</ul>
</nav>

<h1 style="text-align:center;">Administration Team</h1>
<p style="text-align:center;">Meet the people who make Aryabhavan feel like home</p>
</header>

<!-- TEAM MEMBERS UNCHANGED -->

<footer>
<div class="footer-bottom">
Made with ♥ by Aryabhavan © 2025. All Rights Reserved.
</div>
</footer>
</body>
</html>
~~~
contact.html
~~~
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>CONTACT US | ARYABHAVAN</title>
<style>
body{background:#fdf1dc;}
h1{text-align:center;font-size:60px;color:maroon;}
nav{height:65px;width:70%;margin:auto;margin-top:100px;
background:maroon;border-radius:50px;text-align:center;}
ul{display:flex;justify-content:space-between;}
a{color:#f4d03f;text-decoration:none;}
.footer-bottom{text-align:center;padding:15px;background:#333;color:white;}
</style>
</head>

<body>
<header>
<div style="text-align:center;margin:40px;">
<img src="{% static 'ashna.png' %}" style="width:300px;height:300px;">
</div>

<nav>
<ul>
<li><a href="{% url 'home' %}">Home</a></li>
<li><a href="{% url 'menu' %}">Menu</a></li>
<li><a href="{% url 'administration' %}">Administration</a></li>
<li><a href="{% url 'contact' %}">Contact Us</a></li>
</ul>
</nav>
</header>

<h1>Contact Us</h1>

<center>
<p style="font-size:x-large;">
<strong>
Aryabhavan<br><br>
📍 Address: Vadasery Bus Stand, Nagercoil<br>
📞 Phone: +91 97913 62222<br>
✉️ Email: aryabhavan@info.com<br><br>
We look forward to welcoming you.
</strong>
</p>
</center>

<footer>
<div class="footer-bottom">
Made with ♥ by Aryabhavan © 2025. All Rights Reserved.
</div>
</footer>
</body>
</html>
~~~
# OUTPUT:
![alt text](<Screenshot 2025-12-23 123744.png>)
![alt text](<Screenshot 2025-12-23 123800.png>)
![alt text](<Screenshot 2025-12-23 123813.png>)
![alt text](<Screenshot 2025-12-23 122705.png>)
![alt text](<Screenshot 2025-12-23 121848.png>)
![alt text](<Screenshot 2025-12-23 122901.png>)
![alt text](<Screenshot 2025-12-23 122913.png>)
![alt text](<Screenshot 2025-12-23 122925.png>)
# RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
