# Azure Privileged Identity Management (PIM)

_PIM’i kullanmak için ücretli veya deneme lisanslarından birine ihtiyacınız vardır: **Azure AD Premium P2, Enterprise Mobility + Security (EMS) E5 veya Microsoft 365 M5.**_

Azure AD ve Azure kaynaklarına zamana dayalı erişim sağlamaya olanak tanır.

* Yöneticiler, bir rolün maksimum süresi (en fazla 24 saat) olacak şekilde bir aktivasyon süresi seçebilir. Yalnızca o süre için ayrıcalığı alacaklardır. Aktivasyon süresinden sona erdikten sonra, yöneticilerin tekrar aktivasyon süreci onyalması gerekmektedir.
* Başlangıç ve bitiş tarihlerini kullanarak kaynaklara zamana bağlı erişim atama. PIM, rol için bir bitiş zamanı belirlemenizi sağlar. Bu, özellikle bir misafir hesabı için kullanışlıdır. Şirketin belirli bir süre çalışan müşteri hesapları varsa, rol ayrıcalığı otomatik olarak sona erecektir.

Ayrıcalıklı rolleri etkinleştirmek için onay gereklidir. Bir veya daha fazla onaylayıcı atayabilirsiniz. Bu onaylayıcılar, istek yapıldığında bir e-posta alacaklardır. Ayrıcalığın etkinleştirilmesi için onay gereklidir.

Herhangi bir rolü etkinleştirmek için Azure Multi-Factor Authentication’ı (MFA) zorunlu kılınır. Şirket içerisinde hali hazırda MFA etkinleştirilmişse, PIM kullanıcıdan tekrar oturum açmasını istemeyecektir.

Kullanıcıların neden etkinleştirdiğini anlamak için yetki istedikleri talep için açıklama istenir. Hem iç hem de dış denetçilerin rolün neden etkinleştirildiğini anlamalarına yarar.

Bir kullanıcıya bir ayrıcalık atandığında ve bu ayrıcalık etkinleştirildiğinde bildirim alınır.

Kuruluşta hangi kullanıcıların ayrıcalıklı rollere sahip olduğunu ve bunlara hâlâ ihtiyaç duyup duymadıklarını öğrenmek için erişim incelemeleri hem panel üzerinden hem de rapor olarak incelenebilir.

Dahili veya harici bir denetim için loglar geriye dönük saklanır ve talep halinde indirilebilir. Bu, tüm PIM olaylarının kaydını tutar.

Kullanıcılar, Azure AD’de farklı yönetici rollerine atanabilir. Bu rol atamaları, kullanıcıların Azure AD, Microsoft 365 ve diğer Microsoft Çevrimiçi Hizmetleri ve bağlı uygulamalarda gerçekleştirebileceği kullanıcı ekleme veya kaldırma ya da hizmet ayarlarını değiştirme gibi görevleri yapmasını sağlar.

Global Administrator **Add-MsolRoleMember** ve **Remove-MsolRoleMember**gibi PowerShell cmdlet’lerini kullanarak veya portal aracılığıyla Azure AD’deki rollere kalıcı olarak atanan kullanıcıları düzenleyebilir.

Azure AD Privileged Identity Management (PIM), Azure AD’deki kullanıcılar için ayrıcalıklı erişim kurallarını yönetir. PIM, kullanıcıları Azure AD’de bir veya daha fazla role atar ve birini kalıcı olarak rolde olacak veya role uygun olacak şekilde atayabilirsiniz. Bir kullanıcı kalıcı olarak bir role atandığında veya uygun bir rol atamasını etkinleştirdiğinde, rollerine atanan izinlerle Azure Active Directory, Microsoft 365 ve diğer uygulamaları yönetebilir.

Kalıcı ve uygun bir rol ataması olan birine verilen erişim arasında hiçbir fark yoktur. Tek fark, bazı kişilerin bu erişime her zaman ihtiyaç duymamasıdır. Rol için uygun hale getirilirler ve ihtiyaç duyduklarında rolü açıp kapatabilirler. PIM üzerinde yönetici rolü olarak aşağıdaki roller bulunmaktadır.

* **Global Administrator: (**Company Administrator) tüm yönetim özelliklerine erişebilir. Şirkette birden fazla global administrator olabilir. Microsoft 365'i satın almak için kaydolan kişi otomatik olarak global adminisrator olur.
* **Privileged role Administrator:** Azure AD PIM’i yönetir ve diğer kullanıcılar için rol atamalarını güncelleştirir.
* **Billing Administrator:** Satın alma işlemlerini gerçekleştirir, abonelikleri yönetir, destek taleplerini yönetir ve hizmet durumunu izler.
* **Password Administrator:** Parolaları sıfırlar, hizmet taleplerini yönetir ve hizmet durumunu izler. Parola yöneticileri, kullanıcılar için parolaları sıfırlamakla sınırlıdır.
* **Service Administrator:** Hizmet yöneticisi, hizmet isteklerini yönetir ve hizmet durumunu izler.
* Not: Microsoft 365 kullanıyorsanız, bir kullanıcıya hizmet yöneticisi rolünü atamadan önce Exchange Online gibi bir hizmete kullanıcı yönetim izinlerini atayın.
* **User Management Administrator:** Parolaları sıfırlar, hizmet durumunu izler ve kullanıcı hesaplarını, kullanıcı gruplarını ve hizmet isteklerini yönetir. User Management Administrator, Global admin hesabını silemez, başka yönetici rolleri oluşturamaz veya faturalandırma, genel ve hizmet yöneticileri için parolaları sıfırlayamaz.
* **Exchange Administrator:** Exchange yönetim merkezi (EAC) aracılığıyla Exchange Online’a yönetici erişimine sahiptir ve Exchange Online’da hemen hemen her görevi gerçekleştirebilir.
* **SharePoint Administrator:** SharePoint Online yönetici merkezi aracılığıyla SharePoint Online’a yönetim erişimine sahiptir ve SharePoint Online’da neredeyse tüm görevleri gerçekleştirebilir.
* **Skype for Business Administrator:** Skype Kurumsal yönetim merkezi aracılığıyla Skype Kurumsal’a yönetici erişimine sahiptir ve Skype Kurumsal Çevrimiçi Sürüm’deki hemen hemen her görevi gerçekleştirebilir.

\
\
