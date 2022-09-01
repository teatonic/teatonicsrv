# Teatonic Services

A full sample of services.
Based on Tango generator : https://github.com/StudioEtrange/tango

## Installation


### Install and update tango dependencies


```
cd $HOME
git clone https://github.com/StudioEtrange/tango
cd tango
./tango install
```


### install teatonicsrv

```
cd $HOME
git clone https://github.com/StudioEtrange/teatonicsrv
```

## Configuration

* modify `$HOME/teatonicsrv/teatonicsrv.env` file according to your needs

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