WSGI (Web Server Gateway Interface) layer is a specification that provides a standardised interface between web servers and python web applications / frameworks.
Check out [[💥💀Python Backend Internals]] to grind basics 

***purpose of WSGI layer***
> WSGI has been designed to facilitate communication between web servers and python application.
> This ensures the compatibility across various servers and frameworks. 😎


***WSGI application structure*** 👨🏻‍💻
- WSGI application is a callable object, which accepts two arguments:
	- `environ :`  A dict containing CGI-style environment variables. this includes info about the request, such as headers, method, URL, etc...
	- `start_response :`  This is a callback function that takes the status and header of the response.
	- *NOTE ::  The above start response should be called before the application returns the response body !!!*
```
def learning_app(environ, start_response):
    status = '200 OK'
    headers = [('Content-type', 'text/plain')]
    start_response(status, headers)
    return [b'Hello, World!']	
```

***WSGI Server***
- The WSGI server acts as an intermediary between the web server and the WSGI application handling the details to manage multiple requests
- Popular WSGI servers include Gunicorn, uWSGI, and Waitress. 👨🏻‍🔧

*Also WSGI supports middleware, which are components that can be placed between the web server and the web application to process req and resp. Middleware can handle tasks such as session management, authentication, etc....* ⎨·⎬

