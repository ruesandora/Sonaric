# Sonaric

> Node'u kurduktan sonra sonaric puanlarımız anlık olarak gelecek.

> Hala bir incentive programı üstünde çalıştıklarını söylemişler.

> Puanlarımız ödül olacak diye bir şey yok - sadece RC olarak içerdeyiz.

> Sunucu maliyetimiz yok, mevcut bir sunucumuzu kullanacağız.

#

# Donanım.

> Ubuntu 22 ve üzerine ihtiyacımız var.

> Ben aktif node kurduğum cihazlardan birini kullandım.

> Yinede yeni sunucu alacaksanız 2 vCPU 2 RAM yeterlidir.

#

# Kurulum

```console
# sunucu güncelleme
sudo apt-get update && sudo apt-get upgrade -y

# nvm kullanarak nodejs yükleyelim 
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
nvm install 20
nvm use 20
npm install -g npm@latest

# sonaric kurulumu
sh -c "$(curl -fsSL https://raw.githubusercontent.com/monk-io/sonaric-install/main/linux-install-sonaric.sh)"
````

> `sonaric node-info` komutu ile node bilgileri çıktısı alıyorsak okeydir.

<img width="661" alt="Ekran Resmi 2024-07-03 12 29 31" src="https://github.com/ruesandora/Sonaric/assets/101149671/a61730fe-2fd7-4e34-a802-41158e24f6ee">

#

```console
# güncelleme
sudo apt update
sudo apt upgrade sonaric
sonaric node-info
```

```console
# komutun sonunu düzenleyelim.
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
# user olarak root kullanıyorsanız root yazalım.
```

> Yukarıdaki komutun çalıştığını anlamak için: `curl http://localhost:44004`

<img width="874" alt="Ekran Resmi 2024-07-03 12 37 19" src="https://github.com/ruesandora/Sonaric/assets/101149671/d23fa136-1889-4f1c-b90d-930ce53c67ce">

```console
sonaric identity-export -o node-ismi.identity
# node-ismi kısmını silip bir isim belirleyelim.
# şifremizi girelim.
````

> Yedekleme dosyası sunucumuzda SFTP ( Dosya ) bağlantı uygulamaları ile yada Termius ( Mac - Windows - Telefon ) , Mobaxterm üzerinden indirebilirsiniz.

Termius ise SFTP Girdiniz - Sunucunuzu seçtiniz sunucuzda bulunan xxxx.identy dosyasını sürükleyerek kendi bilgisayarınızda istediğiniz dosyaya kopyaladınız - indirdiniz.

![image](https://github.com/ruesandora/Sonaric/assets/141464235/27431eba-c1a0-4dad-8dff-edf0ec429a70)


> Yedekleme İçin  ( Site Üzerinden Ayarlarken Pub ID - Priv Key - Key - Key PW )

Node ile pc'miz arasında tünel açacağız. 

```console
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
```

User - Ve İp Adresini sunucunuza göre ayarlayıp CMD'ye yapıştırın ve sunucunuza girin. CMD Açık Kaldığı sürece tunel aktif olacaktır. 

Tarayıcınızdan : http://localhost:44004/ - Adresine Gidin - Nodenizin puanını - sıralamanızı göreceksiniz. 

Orta sağ üst ayarlar butonu olacak Tıklayın - Export Butonuna tıklayın - Şifrenizi ayarlayın ve onaylayın artık size keylerinizi verecektir. Kaydedin ardından save to json file dosyasını basarakta json halini bilgisayarına kaydedin.

![image](https://github.com/ruesandora/Sonaric/assets/141464235/2a2c9b7b-e75c-4c8f-ada4-1559c13af1c0)


#

> Puanlarımızı `sonaric points` ile görebiliriz.

<img width="276" alt="Ekran Resmi 2024-07-03 12 39 26" src="https://github.com/ruesandora/Sonaric/assets/101149671/fe2aea28-99ea-45ae-948f-5b6a23a9e116">

> Tebrikler, vaktim olduğunda 2 node daha gelecek reposu bile hazır - we love rc.








