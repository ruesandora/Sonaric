# Sonaric Puan Artmama Sorunu

# İŞLEMLERDEN ÖNCE İDENTİTY DOSYANIZI YEDEKLEYİN!

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

# BU KISIM YUKARIDAKİ İŞLEMİ YAPTIKTAN SORNA PUANLARI SIFIRLANAN KULLANICILAR İÇİNDİR

> identity dosyanız sunucuda bu şekilde olması gerek
> 
![image](https://github.com/user-attachments/assets/100cfef5-0c43-4afd-a07c-05c94879f49e)

> Dosyanımızı içeri aktaralım

```console
sonaric identity-import -i <DOSYA YOLUNUZ>
````
> Şifremizi girelim
> 
![image](https://github.com/user-attachments/assets/5fd88b3d-c07b-4790-9490-4f78e5871061)

> Bu çıktıyı aldıysak devam

```console
sonaric run sonaric-gui/latest
````
![image](https://github.com/user-attachments/assets/daba3408-29b7-4491-8942-4464264172cd)

# TEBRİKLER! ARTIK PUANLARINIZ ARTIYOR
> Anlamadığınız Yerleri RC de sorabilirsiniz
