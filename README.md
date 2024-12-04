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

