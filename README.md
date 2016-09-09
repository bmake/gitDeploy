# gitDeploy

Php Script for deployment of an github repository when a commit is made. Upload via (s)ftp to a remote server is handeled by [PHPloy](https://github.com/banago/PHPloy). 

## Requirments

- [PHPloy](https://github.com/banago/PHPloy)


## Example phploy.ini
	
```ini
	[production]
    scheme = sftp
    user = "username"
    pass = "password"
    host = "server.local"
    path = "/path/to/folder/"
    port = 22
    permissions = 0777

    include[] = 'bower_components'

    pre-deploy[] = "composer update"
    pre-deploy[] = "bower update"

    logger = "on"
```
