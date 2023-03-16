# Azure AD Nedir?

Azure Active Directory (Azure AD), Microsoft’un multi-tenant bulut tabanlı dizin ve kimlik yönetimi hizmetidir. BT Yöneticileri için de Azure AD, şirket çalışanlarına, iş ortaklarına Office365, Salesforce ve Dropbox gibi binlerce bulut SaaS uygulamaları için çoklu oturum açma (SSO) erişimi sağlamaktadır.

> _Henüz suyun yüzeyindeyken şunu da belirtelim._
>
> _Azure AD ≠ Active Directory Domain Servis (AD DS)_

Peki aralarındaki farklar nelerdir?

* **Kimlik Doğrulama Çözümü:** Azure AD, öncelikle bir kimlik doğrulama çözümüdür. HTTP/ HTTPS protokolleri üzerinden haberleşen uygulamalar için tasarlanmıştır.
* **REST API:** Azure AD, HTTP/HTTPS tabanlı olduğundan LDAP üzerinden sorgulama yapamaz. Bunun yerine HTTP/ HTTPS üzerinden REST API’ sini kullanır.
* **Protokol:** AD DS kimlik doğrulamasını Kerberos üzerinden yaparken Azure AD, kimlik doğrulama ve yetkilendirme için (OAuth) SAML, WS-Federation ve OpenID protokollerini kullanır.
* **Kimlik Doğrulama Yöntemleri:** Azure AD; SAML, WS-Federation veya OpenID kullanmaktadır.
* **Yetkilendirme Yöntemleri:** AD DS; OU’ lar üzerinden yetkilendirme yaparken Azure AD, OAuth kullanmaktadır.
* **Düz Hiyerarşi (Flat structure):** Azure AD üzerinde kullanıcılar ve gruplar düz bir yapıda oluşturularak arada katman bulunmaz. AD DS’ de ki OU ve GPO kavramı da yoktur.

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*-QivrxFVA43TnzkC.png" alt=""><figcaption><p>Azure AD ve AD DS Farkları</p></figcaption></figure>



Azure AD ve AD DS Farkları

> _Azure AD’ de bulunan global admin rolündeki kullanıcılar içerdeki tüm ayarlara okuma ve değişiklik yapma yetkisine sahiptir. Riski azaltmak için bu rolü içerde **en fazla 5 kullanıcıya verilmesi önerilir.**_
