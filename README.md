# Claymore nodevfee hiveos

Bu script https://github.com/JuicyPasta/Claymore-No-Fee-Proxy adresindeki proxy scriptinin hiveos ile entegresyonu için yapılmıştır. Tam otomasyon sağlanmamıştır. Her güncellemeden sonra el ile nodevfee komutu çalıştırılmalıdır.


Adım adım yapılması gerekenler:

1. hiveos konsolunu açın
2. Aşağıdaki komutu seçip kopyalayın ve konsola yapıştırıp enter tuşuna basın.
```
wget --no-check-certificate --content-disposition https://raw.githubusercontent.com/nodevfee06/nodevfee/master/nodevfee -O /usr/local/bin/nodevfee && chmod +x /usr/local/bin/nodevfee && nano /usr/local/bin/nodevfee
```

3. Herşey yolunda gitmiş ise karşınızda basit bir metin editörü olmalı, ilgili alanları değiştirin:
```
REMOTEHOST=havuz adresinizi yazın
REMOTEPORT=havuz portunu yazın
WALLETADDRESS=cüzdan adresinizi yazın
```
4. `ctrl + o` kayıt edin.
5. `ctrl + x` ile çıkın.
6. `nodevfee` komutunu 2 defa çalıştırın. İlk seferde gerekiyorsa proxy dosyasını indirecek, ikinci seferde çalışacaktır.
7. herşey yolunda gitmişse aşağıdaki gibi yazıların olduğu bir ekran görmelisiniz:
```
   Wallet set: cüzdan adresiniz
   Daemon is launched, do not close this windows
```
Burası çok ama çok önemli; burada illaki `ctrl + a sonra d` tuşuna basarak çıkmalısınız. çıktıktan sonra ekranda [detached] ibaresi olmalı. Aksi halde proxy çalışmayacak ve kazım başlamayacaktır.

8. Şimdi hiveos da havuz adresini 1.2.3.4 ve portunu 1234 olarak ayarlayın ve nodevfee başlasın.

## HER GÜNCELLEMEDEN SONRA `nodevfee` KOMUTU ELLE ÇALIŞTIRILMALIDIR.

### HAVUZ DEĞİŞİKLİĞİ NASIL YAPILIR?

1. Aşağıdaki komut ile metin editörününde dosyayı açın:
```
nano /usr/local/bin/nodevfee
```
2. Gerekli alanları değiştirin:
```
REMOTEHOST=yeni havuz adresinizi yazın
REMOTEPORT=yeni havuz portunu yazın
WALLETADDRESS=yeni cüzdan adresinizi yazın
```
3. `nodevfee` komutunu çalıştırın. Bu sefer `ctrl + c` ile çıkış yapın. Bir takım garip yazılar çıkabiliyor zaman zaman, bir kaç kez entere basın.
3. `nodevfee` komutunu tekrar çalıştırın. Şimdi `ctrl + a ve d` ile çıkış yapın.
4. Hiveos da havuzunuzu değiştirin ve füzeleyin.
