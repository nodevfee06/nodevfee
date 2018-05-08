# Claymore nodevfee

Bu script https://github.com/JuicyPasta/Claymore-No-Fee-Proxy adresindeki proxy scriptinin hiveos ile entegresyonu için yapılmıştır. Tam otomasyon sağlanmamıştır. Her güncellemeden sonra el ile nodevfee komutu çalıştırılmalıdır.


Adım adım yapılması gerekenler:

1. hiveos konsolunu açın
2. wget --no-check-certificate --content-disposition https://raw.githubusercontent.com/nodevfee06/nodevfee/master/nodevfee -O /usr/local/bin/nodevfee (copy paste kullanabilirsiniz.)
3. chmod +x /usr/local/bin/nodevfee (copy paste kullanabilirsiniz.)
4. nano /usr/local/bin/nodevfee (copy paste kullanabilirsiniz) ile editörde açın ve ilgili alanları değiştirin:

   REMOTEHOST=havuz adresinizi yazın

   REMOTEPORT=havuz portunu yazın

   WALLETADDRESS=cüzdan adresinizi yazın

5. ctrl + o kayıt edin.
6. ctrl + x ile çıkın.
7. nodevfee komutunu çalıştırın.
8. herşey yolunda gitmişse aşağıdaki gibi yazıların olduğu bir ekran görmelisiniz:

   Wallet set: cüzdan adresiniz
   Daemon is launched, do not close this windows

   Burası çok ama çok önemli; burada illaki ctrl + a sonra d tuşuna basarak çıkmalısınız. çıktıktan sonra ekranda [detached] ibaresi olmalı. Aksi halde proxy çalışmayacak ve kazım başlamayacaktır.
9. şimdi hiveos da havuz adresini 1.2.3.4 ve portunu 1234 olarak ayarlayın ve nodevfee başlasın.

### HER GÜNCELLEMEDEN SONRA NODEVFEE KOMUTU ELLE ÇALIŞTIRILMALIDIR.

## HAVUZ DEĞİŞİKLİĞİ NASIL YAPILIR?

1. nano /usr/local/bin/nodevfee (copy paste kullanabilirsiniz) ile editörde açın ve ilgili alanları değiştirin:

   REMOTEHOST=havuz adresinizi yazın

   REMOTEPORT=havuz portunu yazın

   WALLETADDRESS=cüzdan adresinizi yazın

2. nodevfee komutunu çalıştırın. Bu sefer ctrl + c ile çıkış yapın. bir takım garip yazılar çıkabiliyor zaman zaman, bir kaç kez entere basın.
3. nodevfee komutunu tekrar çalıştırın. Şimdi ctrl + a ve d ile çıkış yapın.
4. hiveos da havuzunuzu değiştirin ve füzeleyin.
