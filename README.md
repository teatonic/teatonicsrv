# Teatonic Services

A full sample of services used as a demo for Tango generator : https://github.com/StudioEtrange/tango

## Installation


### Install or update tango dependencies


```
cd $HOME
git clone https://github.com/StudioEtrange/tango
cd tango
./tango install
```


### Install teatonicsrv

```
cd $HOME
git clone https://github.com/StudioEtrange/teatonicsrv
```

## Configuration


### Configuration file


* modify `$HOME/teatonicsrv/teatonicsrv.env` file according to your needs

### Minimal configuration

* set these variables

    |variable name|description|default value|sample value|
    |-|-|-|-|
    |TANGO_DOMAIN|your widcard domain|`.*`|`domain.org`|
    |TANGO_SERVICES_MODULES|list of active modules, add or remove them||`whoami codeserver`|
    |NETWORK_PORT_MAIN|exposed HTTP port for `main` area network||`80`|
    |NETWORK_PORT_MAIN_SECURE|exposed HTTPS port for `main` area network||`443`|
    |NETWORK_PORT_ADMIN|exposed HTTP port for `admin` area network||`58000`|
    |NETWORK_PORT_ADMIN_SECURE|exposed HTTPS port for `admin` area network||`58343`|
    |CTX_DATA_PATH|root path where all traefik and modules data will be stored. Can be absolute or relative to `teatonicsrv/workspace` folder|`data`|`data`|

* NOTE :
    * default value is the tango default variable value if not setted in configuration file or with shell environnment variable

* NOTE : there is two logical networks area and each module is attached to one of them
    * `main` area network is dedicated for generic modules, and may be acessible from outside of your network. Modules are attached to it by default.
    * `admin` area network is dedicated for admin kind modules like traefik or portainer, and should not be acessible from outside of your network

### Certificate generation with lets encrypt

* To activate lets encrypt support set these variable

    |variable name|description|default value|sample value|
    |-|-|-|-|
    |LETS_ENCRYPT|`enable`/`disable` certificate generation. `debug` allow to test certificate generation without beeing ban for spam by letsencrypt|`disable`|`debug`|
    |LETS_ENCRYPT_MAIL|mail used to request certificate to lets encryot||`no@no.com`|


## Available commands

```
cd $HOME
cd teatonicsrv
```



* launch all services
```
./teatonicsrv up
```

* stop all services
```
./teatonicsrv down
```

* get info
```
./teatonicsrv info
```

* get status on services
```
./teatonicsrv status
```

* generate full traefik and compose configuration files
```
./teatonicsrv gen
```

* get help
```
./teatonicsrv -h
```