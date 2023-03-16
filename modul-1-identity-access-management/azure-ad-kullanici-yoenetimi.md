# Azure AD Kullanıcı Yönetimi

Azure AD’ de kullanıcılar 3 şekilde tanımlanır.

* **Cloud Identities:** Kullanıcılar yalnızca Azure AD’de bulunur.
* **Directory-synchronized Identities:** Kullanıcılar On-Prem deki Active Directory’de bulunur. Azure AD Connect aracılığıyla kullanıcılar Azure’a gelir.
* **Guest Users:** Azure’ un dışında bulunan diğer bulut sağlayıcı hesapları veya Microsoft hesaplarıdır.

Kullanıcı şekillerinden grup türlerine geçiş yapalım. Azure bu seferde 2 farklı türde grup tanımlaması yapmamızı istiyor.

* **Security Groups:** En yaygın kullanılan grup türüdür ve bir grup kullanıcı için paylaşılan kaynaklara üye ve bilgisayar erişimini yönetmek için kullanılır. Her kullanıcıya ayrı ayrı yetki vermek yerine tüm üyelere aynı anda yetki verebiliriz. Security group oluşturmak için Azure AD Administrator yetkisi gerekmektedir.
* **Microsoft 365 Groups:** Bu gruplar, kullanıcılarla paylaşılan bir posta kutusuna, takvime, dosyalara, SharePoint vb. sitelere erişim sağlayarak işbirliği fırsatları sunar. Bu seçenek, şirket dışındaki kullanıcılara da erişim izni vermenize de olanak tanır. Bu seçenek hem kullanıcılar hem de yöneticiler tarafından kullanılabilir.

Grup türlerini de bitirdik şimdi geldi kullanıcıları bu gruplara nasıl atayacağımıza. Azure burda 3 farklı seçenek sunuyor.

* **Assigned:** Grubun üyesi olmak için ekleme yapmak yeterlidir.
* **Dynamic User:** Kullanıcıları ekleme/ çıkarma işlemlerini otomatize hale getirmek için gruplara özel kurallar yazılır. Kullanıcının özellikleri kuralla eşleşirse gruba dahil edilir veya çıkartılır.
* **Dynamic Device (Only Security Gropus):** Kullanıcılar için uygulanan yöntemin aynısı cihazlar için olan versiyonudur. Şirket dışındaki cihazlar yönetilemeyeceği için sadece Security Group tarafında kullanılmaktadır.

Bu aşamaya kadar kullanıcıları nasıl oluşturacağımızdan gruplara atama işlemine kadar olan süreci öğrendik. Artık kullanıcı yönetimi kısmının son ve en önemli kısmı olan administrative unitlere gelelim.
