---
title: "PythonBackendInternals: Cooked_hard"
date: "2025-03-12"
tags:
  - "Cooked_hard"
  - "PythonBackendInternals"
---

Okiesss lesgo real quickly on how backend looks 🤩
As we might all know the three main components of backend side of python web applications are
- A Web Server :: such as Apache / Nginx
	-  Guyss !! To receive a HTTP request and back the response we need a web server 
- A WSGI Layer :: such as Gunicorn / uWSGI
	- A Traditional web server might not understand or wouldn't be capable of running a python application, which lead to the evolution of WSGI as a standard interface.
	- There are 2 main benefits from a WSGI server
		- **Flexibility ::** `Jeez, This provides flexi for devs ?? 👨🏻‍💻 yesss!! We know Backend has three layers, making WSGI as the middle layer , which now de-couples the need for choosing a framework for web application even though that doesn't support the web server ...  Yeahhhhh it is 💪🏻`
		- **Scaling ::** `Lesgoo!!! Consider we are having a flow where WSGI doesn't exist , where our application server will work as application layer along with managing requests... Intro of WSGI seperates this... And WSGI is meant  for hanlding multiple concurrent requests efficiently 💥`
- A Web Application Framework :: Such as Cherrypy / Django / Flask
	- Here, this layer handles the application level logic.

