# Sonaric Puan Artmama Sorunu

> Sonaric'de puanlarınız hiç artmıyorsa bu yöntemi deneyebilirsiniz

# Başlangıç
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
![image](https://github.com/user-attachments/assets/8078ae7e-949f-43f1-9bfa-b5d80f5d8c30)

> Böyle ise devam edelim

> Puanlarım artıyormu kontrol edelim
```console
sonaric points
````

# Artmaya Başladıysa Tamamdır
> Anlamadığınız yerleri RC de sorabilirsiniz
