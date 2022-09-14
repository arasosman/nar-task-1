# Narbulut Organization Import Task

Bu küçük `Laravel` projesinde sizden gerçekleştirmenizi beklediğimiz görev, organizations.csv dosyasındaki organization listesini laravel projesine import etmeniz (Gerekli dosya repoda bulunmaktadır) ve import edilen modelleri rest api yazılması. Projedeki tüm endpoint ve diğer componentlerin testlerinin yazılması.

Basitçe projede `Organization`, `User` Modellerinin olması beklenmektedir. Bu modeller arasında ilişkileri yapmanız beklenmektedir. 

Oluşturulan her kullanıcı için rasgele bir şifre oluşturulması ve bu şifrenin kullanıcıya hoşgeldiniz maili ile birlikte atılması beklenmektedir. (şifre db'de açık olarak tutulmamalıdır.)

organizations.csv dosyası sadece organization bilgisini tutmaktadır. Bu bilgilerden user bilgilerini üretmelisiniz. Örn: organizations.csv dosyasındaki email adresini USER modeli içinde kullanabilirsiniz. 

Organization ve User modelinde uuid alanı olması beklenmektedir. uuid observer yada listener ile eklenmesi önerilmektedir.

User ve Organization arasında ilişki olması beklenmektedir. User birden çok organizationa atanmış olabilir. Bunu aynı email birden çok organizationda kullandıysa anlanabilir.

Projede Cache, Ve Request limit (throttle) kullanılması önerilmektedir (dakikada 50 istekten fazlası gönderilmemeli).

Modeller

 - id
 - uuid
 - name
 - email
 - phone
 - address

User
 - id
 - uuid
 - name
 - email
 - password


## Beklentiler.
- Model, Factory, Migration dosyalarının oluşturulması.
- Import edilen Modelleri görüntüleyebileceğimiz Rest Api endpointleri.
- Organizations.csv dosyanını import eden bir command eklenmesı (Optional)
- Csv dosyası okurken her organization için işleri sırayla yapmak yerine kuyruklanarak (Job vb) Async ele alınması
- Tüm testlerin yazılması (Optional)
- Proje Docker üzerinde çalışmalıdır (Optional)
- Hoşgeldin maili farklı bir servisten (Microservice) gönderilmelidir. (Optional)
- İki servis arasındaki iletişim Service Bus(Rabbitmq or kafka) üzerinden olmalıdır. (Optional)
- Yazılan kodların psr 2 standardında olması ve solid prensiplerine uygun olması beklenmektedir (Optional)
- kodların static kod analizi tollarında geçmesi beklenmektedir (exp: phpcs or phpmd) (Optional)
- analiz için composer komutları yazılabilir. (Optional)


Proje github reposu olarak gönderilmelidir. commitler aşama aşama atılmalıdır akışa dikkat edilecektir.

Şimdiden başarılar. Anlamadığınız yada aklınıza takılan bir yer olması durumunda benimle iletişime geçebilirsiniz.

osman.aras@narbulut.com.tr