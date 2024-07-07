arkadaşlar tmpfs (Yetersiz Alan Sorunu) hatası alanlar için çözüm buldum deneyebilirsiniz 

```s -ld /run
sudo mount -t tmpfs tmpfs /run  
mount -o remount,size=99M /run/
```

kontrol edelim 

```
df -h /run
```

Used kısmı azaldıysa tamamdır
![image](https://github.com/Emir236070/Sonaric/assets/94224701/a7fcbf3d-2219-4153-922c-043ec09585c8)
