# docker-php-apache-xdebug
Run xDebug on apache with php

## Install image

Run this command:

```bash
docker pull greep/php-apache-xdebug
```

This will install php:apache and add xDebug config on it

## Run it on your VSCode

- Install `PHP Debug` extension on your Code

- Create `.vscode/launch.json` on your workspace

- Paste this configuration:
```json
{
    "name": "Listen for XDebug on Docker App",
    "type": "php",
    "request": "launch",
    "port": 9000,
    "pathMappings": {
        "/var/www/html": "${workspaceFolder}"
    },
    "xdebugSettings": {
        "max_data": 65535,
        "show_hidden": 1,
        "max_children": 100,
        "max_depth": 5
    }
}
```

Then run it with F5
