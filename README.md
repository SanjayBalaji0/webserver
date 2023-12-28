# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```

from http.server import HTTPServer, BaseHTTPRequestHandler
content ="""
<html>
<head>
</head>
<body>
<h1>JOHN PAUL J</h1>
<h1>AIDS<h1>
</body>
</html>
"""

class HelloHandler (BaseHTTPRequestHandler):
   def do_GET (self):
     self.send_response(200)
     self.send_header('Content-type', 'text/html; charset=utf-8')
     self.end.headers ()
     self.wfile.write(content.encode())

server_address = ('', 80)
httpd = HTTPServer (server_address, HelloHandler)
httpd.serve_forever()
```
## OUTPUT:
![image](https://github.com/SanjayBalaji0/webserver/assets/145533553/299f24fd-6207-4835-a380-78fdc6e74083)


## RESULT:
The program is executed succesfully
