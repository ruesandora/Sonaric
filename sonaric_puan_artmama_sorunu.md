# Sonaric Puan Artmama Sorunu

> Sonaric'de puanlarınız hiç artmıyorsa bu yöntemi deneyebilirsiniz
> 
> Ağı silelim
```console
podman network rm monk-core-network -f
````

> Tekrar başlatalım
```console
systemctl start sonaricd
````

> Durum kontrol
```console
systemctl status sonaricd
````
