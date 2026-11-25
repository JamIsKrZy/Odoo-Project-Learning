# Practice Odoo Project


## Run Server Locally


```
uv run python odoo/odoo-bin -c .odoorc -d dev20 -i base --dev=reload,xml,qweb --save
```


after  running the command, the odoo config will save due to `--save`. You dont have to run with
specifying the config file. [Refer to this document](https://www.odoo.com/documentation/master/developer/reference/cli.html#configuration-file)    



## How to setup configuration
The Docker compose only set ups a basic local hosted posgresql. 
just create a config  file `.odoorc` with the following contents


*Contents*
```
[options]
admin_passwd = admin

db_host = localhost
db_port = 5432
db_user = odoo
db_password = odoo

addons_path = odoo/addons,custom_addons
data_dir = .odoo_data
```

Note: This setup is still in practice use yet. Do not use it for production use project
