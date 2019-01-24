---
layout: post
published: true
title: WOL ile Ağ Üzerinden Bilgisayarı Açmak
---

Wake On Line Nedir?

Wake On Line, bilgisayarın ağ üzerinden açıldığı bir BIOS ve Ethernet Kartı özelliğidir. Bu özellik size zamandan, enerjiden ve aynı zamanda mekan gözetmeksizin istediğiniz yerden kapalı olan bilgisayarınızı açmanızı sağlar. Bu özelliği kullanmak için ise gerekli olan bazı şartlar şunlardır;

1. BIOS'unuzda Wake On Line özelliğini destekliyor mu?
2. Ethernet Kartınız Wake On Line özelliğini destekliyor mu?
3. Sabit IP kullanıyor musunuz? "Uzaktan Erişim İçin Gerekli"

Anakartınız ATX uyumlu bir güç kaynağına bağlı ise artık yapacağımız işlemlere geçebiliriz. İlk olarak yukarıda da belirttiğim gibi BIOS içine girip ayarlarımızı "Enabled" yapmamız gerekiyor. Bunun için BIOS ekranına gelip "Power" veya "Advanced" sekmesinden gerekli WOL ayarlarını düzeltiyoruz.

> Denediğim bazı bilgisayarlar da BIOS ekranında "Network Configuration" ayarları mevcut eğer bu ayar var ise bunu da "Enabled" yapmanız gerekiyor.

Daha sonra "Exit" sekmesine gelip "Save and Exit" diyerek BIOS ekranımızdan çıkış yapıyoruz ve bilgisayarın yeniden açılmasını bekliyoruz. Bilgisayarımız açıldığında ise bu sefer Ethernet Kartımıza bakıyoruz. Burada dikkat etmeniz gereken nokta bu işlem "Wi-Fi" üzerinden olmuyor. Bunun için modeminizden bilgisayarınıza bir RJ-45 kablo gelmesi gerekiyor. Kablolu bağlantımız var sayarsak yapacağımız işlemler aşağıdaki gibi olacaktır.

1. İlk olarak Bilgisayarım'a sağ tıklayıp Yönet sekmesine tıklıyoruz.
2. Açılan pencerede "Aygıt Yöneticisi" sekmesine tıklıyoruz.
3. Yan pencereden "Ağ Bağdaştırıcıları" sekmesine tıklıyoruz.
4. Alt başlıklardan kablolu bağlantımızın olduğu bağdaştırıcıya sağ tıklayıp "Özellikler" diyoruz.
5. "Güç Yönetimi" sekmesinden "Bu aygıt, bilgisarı başlatsın" seçeneğini işaretliyoruz.
6. "Gelişmiş" sekmesinden "Sihirli Paket Eşleştirme Uyanmasını" "Etkinleştir" diyoruz.
7. "Tamam" butonuna basıp ayarlarımızı kaydediyoruz.

> Eğer Kablolu Ağ Bağdaştırıcınızda WOL özelliği yok ise sürücünüzü güncelleştirebilirsiniz. Bilgisayarınızı yeniden başlattığınız da eğer güncel sürücü kurulduysa büyük olasılıkla WOL özelliği de geliyor. Eğer hala gelmediyse Ethernet Kartınız çok eski olabilir.

### Yerel Ağdan Açmak İçin

Artık yapmamız gereken WOL özelliği olan IP Scanner programlarıyla bilgisayarımıza WOL değerini göndermek. Eğer Ağ üzerinden bilgisayar açacak iseniz benim de kullanıyor olduğum program Advanced IP Scanner. Programı kurduktan sonra Ağınızı taratıp kablo ile bağlı olan bilgisayarlarınızı sağ tıklayıp "Wake On Line" foksiyonunu gönderip çalıştırabilirsiniz.

### Uzaktan veya Mobilden Açmak İçin

Uzaktan bilgisayarınızı açmak için gerekli siteler ve mobil uygulamalar mevcut. İnternette Wake On Line aramasını yaparsanız karşınıza onlarca mobil uygulama gelecektir. Eğer bilgisayardan açmak istiyorsanız şuan benim kullanmış olduğum site [Depicus - Wake On Line](https://www.depicus.com/wake-on-lan/woli "WOL") 

Bu sayfadan bilgisayarınıza ait bilgileri girerek uzaktan bilgisayarınızı açabilirsiniz. Sabit IP olmasında fayda var çünkü bu işlemler daha kolay ve hızlı oluyor. Her seferinde IP değişmesini istemiyorsak.


