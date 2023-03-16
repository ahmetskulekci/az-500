# Azure Identity Protection

Ne olduğuna anlatmadan önce ufak bir detaya değinmek isterim. Bu modül _**Azure AD Premium P2**_ lisansı gerektiriyor :)

Identity Protection, şirketlerin üç ana görevi gerçekleştirmesi olanak sağlamaktadır.

* Kimliğe dayalı risklerin tespiti ve düzeltilmesine kadar uzanan süreci otomatize eder.
* Portal üzerinden verileri analiz ederek çözüm konusunda görünürlük sağlar.
* Daha fazla analiz için verileri 3rd party uygulamalara (SIEM) aktarma olanağı sunar.

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*GakwcpqbSl0pBFUp.png" alt=""><figcaption><p>Identity Protection Poliy Ekranı</p></figcaption></figure>

Azure AD Identity Protection, yöneticilerin etkinleştirmeyi seçebileceği üç varsayılan kural içerir. Bu politikalar limitli özelleştirme içerir, ancak çoğu şirket için geçerlidir. Tüm kurallar, acil durum veya break-glass yönetici hesaplarınız gibi kullanıcıların hariç tutulmasına izin verir.

* **Azure MFA Policy:** Oturum açma esnasında MFA kullanılması zorunlu hale getiren kuraldır.
* **Sign-in risk Policy:** Identity Protection, hem gerçek zamanlı hem de çevrimdışı olarak her oturum açma işleminden gelen logları analiz eder ve oturum açmanın kullanıcı tarafından yapılmamış olma olasılığına göre bir risk puanı hesaplar. Yöneticiler, kurumsal gereklilikleri uygulamak için bu risk puanı loguna dayalı olarak karar verebilir. Yöneticiler erişimi engellemeyi, erişime izin vermeyi veya erişime izin vermeyi seçebilir ancak yöneticinin bu işlemi yapabilmesi MFA doğrulaması gerekir.
* **Custom Access Policy:** Yönetici hesapları şirketin gereksinimlere göre kendi belirledikleri parametrelere göre kural yazabilir.

Riskli oturum işlemine dair tespitleri ve raporları iki farklı ortamda inceleyebiliriz.

* Azure AD Reporting
* Azure Identity Protection

Hali hazırda Azure AD üzerinde altı farklı risk türü bulunmaktadır.

* **Leak credentials:** Hacker forumlarında yayınlanmış bir kullanıcı bilgisiyle oturum açma işlemlerini tanımlar
* **Sign-ins from anonymous IP addresses:** Anonim bir proxy IP adresi olarak tanımlanmış bir IP adresinden oturum açan kullanıcıları tanımlar.
* **Impossible travel to atypical locations:** Coğrafi olarak uzak konumlardan yapılmış iki oturum açmayı tanımlar; burada konumlardan en az biri, geçmişteki davranışları göz önüne alındığında kullanıcı için alışılmadık olabilir.
* **Sign-ins from infected devices:** Bir C2 (Command and Control Server) sunucusuyla aktif olarak iletişim kurduğu bilinen, zararlı yazılım bulaşmış cihazlardan yapılan oturum açma işlemlerini tanımlar.
* **Sign-in from unfamiliar locations:** Yeni/bilinmeyen konumları belirlemek için geçmiş oturum açma konumlarını (IP, Enlem/Boylam ve ASN) dikkate alır.
* **Sign-ins from IP addresses with suspicious activity:** Kısa bir zaman diliminde birden çok kullanıcı hesabında çok sayıda başarısız oturum açma girişiminin görüldüğü IP adreslerini tanımlar.

_Azure AD Premium P2 lisansıyla, tüm temel ve gelişmiş algılamalar hakkında en ayrıntılı bilgileri alırsınız._

_Azure AD Premium P1 lisansıyla, gelişmiş algılamalar (Sign-in from unfamiliar locations) lisansınızın kapsamına girmez ve riskli oturum açma alanı altında görünür. Ayrıca, risk düzeyi ve risk ayrıntısı alanları da gizlenir._

Riskli oturum açma işlemleri olan kullanıcılar “User risk policy” altında görülüp kullanıcıların hangi sebeple ve hangi seviyede riskli olduğuna dair bilgiler bulunmaktadır. Yöneticiler şifre resetlemeye zorlama, riski reddetme, oturum açmayı engelleme ve Azure ATP ile daha fazla araştırma yapılması gibi aksiyonları alabilir ve bu işlemler 1 aylık raporlar halinde incelenebilir. Raporda bulunan bazı bilgilere bakalım.

* Hangi oturum açma işlemleri hangi risk altında olarak sınıflandırılır? Güvenlik ihlali doğrulandı mı? Doğrulanmadıysa reddedildi veya düzeltildi mi?
* Oturum açma girişimleriyle ilişkili gerçek zamanlı ve toplu risk seviyeleri.
* Tetiklenen algılama türleri
* MFA detayları
* Cihaz Bilgisi
* Konum bilgisi

Yöneticiler bu raporlar üzerinden yukarda belirtilen aksiyonları alabilir. Şirkete özel kurallar oluşturarak ve bilgilendirici eğitimlerle riskli kullanıcı sayısını düşürebilir.
