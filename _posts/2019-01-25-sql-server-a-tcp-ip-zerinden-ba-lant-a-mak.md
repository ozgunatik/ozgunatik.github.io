---
layout: post
published: true
title: SQL Server'a TCP/IP Üzerinden Bağlantı Açmak
bigimg: ../img/sql.png
---
İşyerinizde Microsoft SQL Server veritabanını kullanarak proje geliştiriyorsunuz ve bu veritabanına diğer arkadaşlarınızın erişmesini istiyorsunuz. Yerel ağ veya geniş ağ farketmez bu veritabanını eğer arkadaşlarınıza açmak istiyorsanız ilk olarak yapmanız gereken adım Microsoft SQL Server'a PORT açmaktır.

Bu portu açtıktan sonra MSSQL ile yazılmış bir websiteniz varsa bile kendi bilgisayarınızı Server olarak kullanıp websitenizi dışarı açabilirsiniz. Çok fazla kafanızı bulandırmadan bu işlemlerin nasıl yapılacağını anlatıyorum.

* Başlat menüsüne tıklayıp "SQL Server Configuration Manager" programımızı açıyoruz.

![port1.png]({{site.baseurl}}/img/port1.png)

* Resimdeki gibi sırasıyla alanlara girip gerekli olan pencereyi açıyoruz.

![port2.png]({{site.baseurl}}/img/port2.png)

* IP Adresses butonuna tıkladıktan sonra en aşağıdaki "TCP Port" kutucuğunu istediğimiz herhangi bir Port numarasını yazıyoruz. Bu port numarasına daha sonra Güvenlik Duvarından izin vereceğiz. Geniş ağa açmak istiyorsak modem arayüzümüzden sanal sunucu olarak belirtilen portu açmamız gerekiyor.

![port3.png]({{site.baseurl}}/img/port3.png)

* Bu ayarları uyguladıktan sonra artık "SQL Server" restart atmamız gerekiyor. Bunun için resimdeki belirtilen alana gelir "Restart" sekmesine tıklıyoruz ve işlemin bitmesini bekliyoruz.

![port4.png]({{site.baseurl}}/img/port4.png)

* Sunucumuzu "Restart" ettikten sonra artık güvenlik duvarımızdan gerekli izinleri verebiliriz. Başlat çubuğuna "Gelişmiş Güvenlik Duvarı" yazarak aşağıdaki pencereyi açabiliriz. "Gelen Kurallar" sekmesine tıklayarak "Yeni Kural" oluşturmakla başlıyoruz.

![port5.png]({{site.baseurl}}/img/port5.png)

* Açılan pencereden "Bağlantı Noktası" seçeneğini işaretliyoruz.

![port6.png]({{site.baseurl}}/img/port6.png)

* Bir sonraki sekmede "TCP" seçip Microsoft SQL Server'daki açtığımız ağa açtığımız "TCP Portu"nu buraya yazarak portumuza izin veriyoruz.

![port7.png]({{site.baseurl}}/img/port7.png)

* Bağlantıya izin ver seçenğini işaretliyoruz ve devam ediyoruz.

![port8.png]({{site.baseurl}}/img/port8.png)

* İleride "PORT" değiştirmek istersek bize açıklayacı olması açısından bir isim ve açıklama belirtiyoruz.

![port9.png]({{site.baseurl}}/img/port9.png)



![port10.png]({{site.baseurl}}/img/port10.png)



