---
layout: post
published: true
title: SQL Server'a TCP/IP Üzerinden Bağlantı Açmak
bigimg: ../img/sql.png
---
İşyerinizde Microsoft SQL Server veritabanını kullanarak proje geliştiriyorsunuz ve bu veritabanına diğer arkadaşlarınızın erişmesini istiyorsunuz. Yerel ağ veya geniş ağ farketmez bu veritabanını eğer arkadaşlarınıza açmak istiyorsanız ilk olarak yapmanız gereken adım Microsoft SQL Server'a PORT açmaktır.

Bu portu açtıktan sonra MSSQL ile yazılmış bir websiteniz varsa bile kendi bilgisayarınızı Server olarak kullanıp websitenizi dışarı açabilirsiniz. Çok fazla kafanızı bulandırmadan bu işlemlerin nasıl yapılacağını anlatıyorum.

1. Başlat menüsüne tıklayıp "SQL Server Configuration Manager" programımızı açıyoruz.

![port1.png]({{site.baseurl}}/img/port1.png)

2. Resimdeki gibi sırasıyla alanlara girip gerekli olan pencereyi açıyoruz.

![port2.png]({{site.baseurl}}/img/port2.png)

3. IP Adresses butonuna tıkladıktan sonra en aşağıdaki "TCP Port" kutucuğunu istediğimiz herhangi bir Port numarasını yazıyoruz. Bu port numarasına daha sonra Güvenlik Duvarından izin vereceğiz. Geniş ağa açmak istiyorsak modem arayüzümüzden sanal sunucu olarak belirtilen portu açmamız gerekiyor.

![port3.png]({{site.baseurl}}/img/port3.png)

4. Bu ayarları uyguladıktan sonra artık "SQL Server" restart atmamız gerekiyor. Bunun için resimdeki belirtilen alana gelir "Restart" sekmesine tıklıyoruz ve işlemin bitmesini bekliyoruz.

![port4.png]({{site.baseurl}}/img/port4.png)


![port5.png]({{site.baseurl}}/img/port5.png)


![port6.png]({{site.baseurl}}/img/port6.png)


![port7.png]({{site.baseurl}}/img/port7.png)


![port8.png]({{site.baseurl}}/img/port8.png)


![port9.png]({{site.baseurl}}/img/port9.png)


![port10.png]({{site.baseurl}}/img/port10.png)



