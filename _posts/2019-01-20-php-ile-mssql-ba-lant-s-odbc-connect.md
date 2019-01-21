---
layout: post
published: true
title: PHP ile MSSQL Bağlantısı - ODBC Connect
---
Eğer PHP'yi sadece web sitesi yapmak için kullanmıyorsanız. Çalıştığınız iş yerinde MSSQL ile ilgili web tabanlı projeler geliştiriyorsanız veya geliştirecekseniz. Olmazsa olmaz olan bağlantılardan bir tanesi ODBC_Connect bağlantısıdır. Başka alternatifler yok mu var tabiki ama hepsi bir uğraş ve zaman gerektiriyor. İnternette yaptığım araştırmalar da hep eski ve yabancı kaynaklı bilgiler olduğu için bu yazıyı yazmaya karar verdim.

İlk olarak belirtmek istediğim şey ise web tabanlı bir proje geliştiriyorsanız ve ilk defa kullanacağınız diziler, bağlantılar var ise muhakkak projenizi sunucuda test ederek ilerleyin. Böylece hem zamandan tasarruf ediyorsunuz hem de sunucuda dönecek olan hataları canlı olarak görme fırsatınız oluyor. Ben böyle yapmadığım için direk localhost'umda çalışıp daha sonra sunucuya aktardığım için bazı sıkıntılar yaşadım. Bu sıkıntıları geçte olsa hallettim ve projemi şuan bitirdim. 

### Microsoft® ODBC Driver 11 for SQL Server® - Windows

Bu indirme paketinde MSSQL Server'ımızı yerel ağ ve Windows Azure gibi servislere açıyoruz. Bir nevi MSSQL Server'ımıza dışarı veri aktarma işlemini yapıyoruz. Aşağıdaki vermiş olduğum linkten bunu indirip kolayca kurabilirsiniz.

[ODBC_Connect - Windows](https://www.microsoft.com/en-us/download/details.aspx?id=36434 "Php ile ODBC Bağlantısı")

### ODBC Kütüphanesini PHP'ye İnclude Etme

Yukarıdaki işlemi yaptıktan sonra asıl bizim için önemli olan noktaya geliyoruz. Bizim burada PHP sürümümüzü bilmemiz gerekiyor çünkü buna göre gerekli olan paketi indirip install edeceğiz. Gelelim bu işi nasıl yapacağımza ilk olarak localhost'unuzun çalıştığı dizine girerek aşağıdaki kodu surum.php uzantılı bir sayfa açıp içine yapıştırıyoruz.

__ <?php
__ phpinfo();
__ ?>

Sürümüzü öğrendikten sonra bizim için gerekli olan install paketini yükledikten sonra indirdiğimiz dll'leri nasıl include edeceğimize geçebiliriz. İlk olarak yapmamız gereken dosyaları bir klasöre çıkartmak daha sonra klasör içindeki .dll uzantılı dosyaları alıp gerekli yere kopyalamak. Bunun için localhost dizinimize gidip örneğin XAMPP kullandığımızı varsayalım PHP -> EXT -> DLL'lerimizi buraya kopyalıyoruz.

Bu işlemi yaptıktan sonra tekrar PHP klasörüne geliyoruz ve PHP.INI dosyasını açıyoruz. Ctrl+F ile 'extension' araması yaparak extension'lara hızlı bir şekilde ulaşabiliriz. Başında ';' olan satırlar geçersiz olarak geçiyor. Bizim yapacağımız iş ise indirdiğimiz .dll uzantılı kütüphanemizi buraya ekleyip başında ';' varsa kaldırmak. Örnek olması açısından aşağıdaki resmi örnek alabilirsiniz. 

[![image](https://i.hizliresim.com/LlnYYJ.png)](https://hizliresim.com/LlnYYJ)

Bu işlemide yaptıktan sonra artık localhost php sürümümüz odbc destekli bir sürüm haline gelmiş oldu tekrar surum.php sayfamızı çalıştırdığınızda başıklarda Odbc paketinin yüklendiğini göreceksiniz. Artık PHP ile MSSQL Server'ımız arasında bir bağlantı kurabiliriz. Bağlantımızı test etmek için tekrar connect.php uzantılı bir sayfa açıp içine aşağıdaki php kodumuzu yapıştırıyoruz.

> <?php  $baglanti = odbc_connect('DRIVER={SQL Server};SERVER=.\OZGUN;DATABASE=Deneme;',"Kullanıcıadi","Sifre"); ?> 



Bağlantımızı da test ettikten sonra artık projelerimize başlayabiliriz. 


> Yukarıda anlatmış olduğum işlemler Windows İşletim Sistemi için geçerlidir. MacOs işletim sistemlerinde bu işlemin nasıl olacağını da yapmış olduğum araştırmalar ve denemelerim sonucunda paylaşacağım. 



