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
Developed by: pvabishek
Reference.No.: 22009411
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
</head>
</head>
<body>
<h1>WELCOME</h1>
<h2>NAME:pvabishek</h2>
<h2>REF.NO.:22009411</h2>
<h3>LIST OF FRAMEWORKS</h3>
<h4>-Django</h4>
<h4>-Ruby on Rails</h4>
<h4>-Angular</h4>
<h4>-Meteor</h4>
<h4>-jQuery</h4>
</body>
</html>
"""

class Hellohandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',80)
httpd = HTTPServer(server_address, Hellohandler)
httpd.serve_forever()
```
## OUTPUT:

![Screenshot_20230128_124555](https://user-images.githubusercontent.com/119405626/215252775-d8bfe037-25cf-41e4-b7e5-3dffe94175a5.png)


## RESULT:
The program is executed succesfully
