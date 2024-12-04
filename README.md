# python-virtualenv

```bash
$ pip install virtualenv
$ virtualenv -python=python3.7 env_name
$ source ./env_name/bin/activate # windows: env_name/bin/activate
```


```
env_name
├── bin
└── lib
    └── python3.12
        └── site-packages
            ├── pip
            │   ├── _internal
            │   │   ├── cli
            │   │   ├── commands
            │   │   ├── distributions
            │   │   ├── index
            │   │   ├── locations
            │   │   ├── metadata
            │   │   │   └── importlib
            │   │   ├── models
            │   │   ├── network
            │   │   ├── operations
            │   │   │   ├── build
            │   │   │   └── install
            │   │   ├── req
            │   │   ├── resolution
            │   │   │   ├── legacy
            │   │   │   └── resolvelib
            │   │   ├── utils
            │   │   └── vcs
            │   └── _vendor
            │       ├── cachecontrol
            │       │   └── caches
            │       ├── certifi
            │       ├── distlib
            │       ├── distro
            │       ├── idna
            │       ├── msgpack
            │       ├── packaging
            │       ├── pkg_resources
            │       ├── platformdirs
            │       ├── pygments
            │       │   ├── filters
            │       │   ├── formatters
            │       │   ├── lexers
            │       │   └── styles
            │       ├── pyproject_hooks
            │       │   └── _in_process
            │       ├── requests
            │       ├── resolvelib
            │       │   └── compat
            │       ├── rich
            │       ├── tomli
            │       ├── truststore
            │       └── urllib3
            │           ├── contrib
            │           │   └── _securetransport
            │           ├── packages
            │           │   └── backports
            │           └── util
            └── pip-24.3.1.dist-info
```




## pythonanywhere
- https://www.pythonanywhere.com/

`hosting server file system`
```
/home/user/
├── virtual_environment
└── sourcecode
    └── main.py
/var/www/
└── user_pythonanywhere_com_wsgi.py
```

`/home/user/main.py`
```python
import dash
from dash import dcc, html

app = dash.Dash(__name__)
app.layout = html.Div([
    html.H1("Hello Dash"),
    dcc.Graph(
        id='example-graph',
        figure={
            'data': [{
                'x': [1, 2, 3],
                'y': [10, 11, 12],
                'type': 'line',
                'name': 'Sample Data'
            }],
            'layout': {
                'title': 'Sample Graph'
            }
        }
    )
])

if __name__ == "__main__":
    app.run_server(debug=True)
```

`/var/www/user_pythonanywhere_com_wsgi.py: dash`
```python
import sys

path = '/home/user/sourcecode'
if path not in sys.path:
    sys.path.append(path)

from main import app
application = app.server
```




