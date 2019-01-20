---
layout: post
published: true
title: PHP ile MSSQL Bağlantısı - ODBC Connect
---
Eğer PHP'yi sadece web sitesi yapmak için kullanmıyorsanız. Çalıştığınız iş yerinde MSSQL ile ilgili web tabanlı projeler geliştiriyorsanız veya geliştirecekseniz. Olmazsa olmaz olan bağlantılardan bir tanesi ODBC_Connect bağlantısıdır. Başka alternatifler yok mu var tabiki ama hepsi bir uğraş ve zaman gerektiriyor. İnternette yaptığım araştırmalar da hep eski ve yabancı kaynaklı bilgiler olduğu için bu yazıyı yazmaya karar verdim.

İlk olarak belirtmek istediğim şey ise web tabanlı bir proje geliştiriyorsanız ve ilk defa kullanacağınız diziler, bağlantılar var ise muhakkak projenizi sunucuda test ederek ilerleyin. Böylece hem zamandan tasarruf ediyorsunuz hem de sunucuda dönecek olan hataları canlı olarak görme fırsatınız oluyor. Ben böyle yapmadığım için direk localhost'umda çalışıp daha sonra sunucuya aktardığım için bazı sıkıntılar yaşadım. Bu sıkıntıları geçte olsa hallettim ve projemi şuan bitirdim. 

### ODBC Kütüphanesini PHP'ye İnclude Etme

ODBC kütüphanesini PHP'ye aktarmak için öncelikle Microsoft'un sitesinden bizim için gerekli olan dosyaları indirmemiz gerekiyor. Aşağıda vereceğim linkten siz kendi işletim sisteminize ve kullandığınız PHP sürümüne göre gerekli olan dosyaları indirebilirsiniz.

[System Requirements ODBC Driver - Microsoft](https://docs.microsoft.com/en-us/sql/connect/php/system-requirements-for-the-php-sql-driver?view=sql-server-2017 "Microsoft ODBC Connect")






