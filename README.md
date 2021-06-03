# openrc-zram
Openrc sistemlerde zram yapılandırmalarına ait birkaç Türkçe rehber

## Yöntem 1

[zram-init](https://github.com/vaeth/zram-init) paketini kurduktan sonra repoda verdiğim zram-init dizini içerisinde yer alan dosyaları, bulundukları dizine ait adı kendi sisteminizde bularak (ikisi de /etc altında bulunmakta) oraya kopyalamanız gerekmektedir. Örneğin /init.d/zram-init dosyasını kendi sisteminizde /etc/init.d/ altına kopyalamalısınız. Her iki dosya içerisinde yer alan talimatları uyguladıktan sonra;

`rc-update add zram-init boot` komutu aracılığıyla servisi boot esnasında aktifleştirebilirsiniz. 

`rc-service zram-init start` komutuyla sistemi yeniden başlatmadan zram'i çalıştırabilirsiniz.

Zaten biliyorsunuzdur ama servisi durdurmak için;

`rc-service zram-init stop`, 

devre dışı bırakmak için;

`rc-update delete zram-init boot` komutunu kullanabilirsiniz.
