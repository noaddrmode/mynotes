# pixi 
```python
pixi global install awscli --with python
pixi global list
pixi global expose add -e awscli python

pixi init myenv
pixi add python=3.12
pixi add numpy
pixi remove numpy
pixi shell
pixi list
pixi update
```


# simple http server that solves CORS problem
To use it as alternative to `python3 -m http.server`
```
#!/usr/bin/env python3
from http.server import HTTPServer, SimpleHTTPRequestHandler, test
import sys

class CORSRequestHandler (SimpleHTTPRequestHandler):
    def end_headers (self):
        self.send_header('Access-Control-Allow-Origin', '*')
        SimpleHTTPRequestHandler.end_headers(self)

if __name__ == '__main__':
    test(CORSRequestHandler, HTTPServer, port=int(sys.argv[1]) if len(sys.argv) > 1 else 8000)
```
