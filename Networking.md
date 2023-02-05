## Default networks
> Uer-defined network   
> - create internal network
> ```python
> docker network create \
>   -- driver bridge \
>   -- subnet 182.18.0.0.0/16
>   -- custom-isolated-network
> ```
> - list all networkds
> ```
> docker network list    
> ```    
>. 

## Inspect Network

```
docker inspect network_name
```


## Enbedded DNS
```javascript
// name of the container
mysql.connect(mysql) 
```

## Docker stirage
where and how docker stores data

> - folder /var/lib/docker
>> - aufs
>> - ...
>> - ...

```javascript
// create a docker volume
docker volume create data_volume
```

```javascript
// mount the volume to the app
docker run -v data_vloume:/var/lib/mysql mysql
```

## storage drivers
- AUFS
- ZFS
- BRTFS
- Device Mapper
- Overlay
- Overlay2


