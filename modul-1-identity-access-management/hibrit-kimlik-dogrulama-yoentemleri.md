# Hibrit Kimlik Doğrulama Yöntemleri

Azure AD Connect, On-Prem AD ve Azure Active Directory’ nizi birbirine bağlayabilir. Böylelikle Microsoft 365, Azure ve SaaS uygulamaları için kullanıcılarınız için ortak bir kimlik sağlamanıza olanak sağlar.

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*Ayl6xA3mc-HqUgXk.png" alt=""><figcaption><p>Azure AD Connect</p></figcaption></figure>

Azure AD Connect

Azure AD Connect’ in öne çıkan özelliklerine bakalım.

* **Password Hash Synchronization:** Azure AD Connect, on-prem de bulunan kullanıcının parolasını Azure AD’ ye senkron ederek eşitler. Bu yöntemde parola, Azure AD’ de tutulur.
* **Pass-Through Authentication:** Kullanıcıların parolası on-prem de bulunan AD’ de doğrulanır. Parola doğrulması cloud ortamında yapılmaz.
* **Federation**: Azure AD, kullanıcının parolasını doğrulamak için kimlik doğrulamasını on-prem de bulunan AD FS gibi ayrı bir kimlik doğrulama sistemine üzerinde yapar.
* **Synchronization:** Kullanıcıları, grupları ve diğer nesneleri oluşturmaktan sorumludur. Ayrıca şirket içi kullanıcıların ve grupların kimlik bilgilerinin cloud ortamında eşleştirmekten sorumludur.
* **Health Monitoring:** Azure AD Connect Health, On-Prem AD ve Azure AD arasındaki bağlantıyı sürekli olarak izlenmesi ve olası sorunda görünürlük için kullanılır. Performansı takip etme ve kritik uyarılar için e-posta bildirimi ayarlayabiliriz.

Peki hangi metodu şirkette kullanmam gerekiyor sorusunun cevabını da aşağıda bulunan karar ağacında bulabiliriz.

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*ovp4EZFc36ZN16fc.png" alt=""><figcaption><p>PHS, PTA ve Federation Authentication Karar Ağacı</p></figcaption></figure>

On-prem Active Directory entegrasyonuna mı ihtiyacınız yoksa yalnızca cloud kimlik doğrulamasını kullanırsınız.

On-Prem Active Directory entegrasyonuna ihtiyacınız varsa cloud kimlik doğrulaması, parola koruması kullanmanız gerekiyor mu ve kimlik doğrulama gereksinimleriniz Azure AD tarafından destekleniyorsa PHS+ Seamless SSO’ yu kullanırsınız.

On-Prem Active Directory entegrasyonuna ihtiyacınız varsa ancak cloud kimlik doğrulaması, parola koruması kullanmanız gerekmiyorsa ve kimlik doğrulama gereksinimleriniz Azure AD tarafından destekleniyorsa PTA + Seamless SSO’ yu kullanırsınız.

On-Prem Active Directory entegrasyonuna ihtiyacınız varsa, mevcut bir federasyon sağlayıcınız varsa ve kimlik doğrulama gereksinimleriniz Azure AD tarafından desteklenmiyorsa Federasyon kimlik doğrulamasını kullanırsınız.

Azure AD tarafından desteklenmeyen kimlik doğrulama yöntemleri

* Akıllı kartlar veya sertifika kullanımı
* On-prem MFA sunucusu üzerinden kimlik doğrulanması
* 3rd party kimlik doğrulama çözümü kullanılması

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*qdfK0Fg0yg_WtMA9.jpeg" alt=""><figcaption></figcaption></figure>

Gün sonunda hangi yöntem kullanılırsa kullanılsın “Password Writeback” özelliğinin aktif edilmesi tavsiye edilmektedir. Böylelikle cloud ortamında değiştirilen parola On-Prem AD’ ye de yazılmış oluyor. Bu özellik Azure Service Bus üzerinden iletişim kurduğu için güvenlik duvarı (firewall) tarafında inbound bir kurala ihtiyaç duymaz.
