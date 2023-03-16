# Azure Komponentleri

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*Up4hP-5svZNFWfCU.png" alt=""><figcaption><p>Azure Hiyerarşisi</p></figcaption></figure>

Azure Resource Manager (ARM), Azure dağıtım ve yönetim hizmetidir. Azure aboneliğinizde kaynak oluşturmanıza, güncellemenize ve silmenize olanak tanıyan bir yönetim katmanıdır. Dağıtımdan sonra kaynaklarınızı korumaya ve düzenlemeye yardımcı olması için erişim kontrolü, denetleme ve etiketleme özelliklerini kullanabilirsiniz.

Portal, Azure PowerShell, Azure CLI, REST API’ler veya SDK’ lar aracılığıyla işlem gerçekleştirdiğinizde, Resource Manager API isteğinizi işler. Aynı API tüm istekleri işlediğinden, tüm farklı araçlardan tutarlı sonuçlar ve yetenekler alırsınız. Başlangıçta API’ler aracılığıyla yayınlanan işlevsellik, ilk sürümden sonraki 180 gün içinde portalda temsil edilmelidir.

Kapsam

Azure totalde dört ana bileşen aracılığıyla yönetilir.

* Management groups
* Subscriptions
* Resource groups
* Resources

Management Groups

Management Groups, ortamınızın yapısında esnek ve sürdürülebilir hiyerarşiler oluşturmayı sağlayan Azure kaynağıdır. Management Groups, subscriptions seviyesinin üzerinde bulunur ve böylece subscription ları birlikte gruplandırılmasına olanak tanır.

Bu gruplama, management groups ların kurallarını ve RBAC yetkilerinin uygulanmasını kolaylaştırır. Kurallar ve RBAC yetkileri, management group daki tüm kaynaklara devralınır.

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*lpiTbURuzvlqyd3t.png" alt=""><figcaption><p>Management Groups Örneği</p></figcaption></figure>

Management Groups lar altı seviyeye kadar dallanma olabilir. Bu bize, şirket ihtiyaçlarını karşılamak için bu stratejilerin birkaçını birleştiren bir hiyerarşi oluşturma esnekliği sağlar.

Resource Groups

Azure Resource Manager (ARM) de kendi içerisinde iki kısımdan oluşur.

1. Resource Group
2. Resource Group Template

Resource Manager Mimarisi ile Azure’da açılan her nesne bir kaynak (resource) olarak işlenir ve resource group’lar tamamen ücretsizdir. ARM Kaynak grupları ve içerisindeki kaynakların oluşturulması, yapılandırılması, yönetilmesi ve silinmesine sağlayan yönetim katmanıdır.

Resource Group, Azure Resource Manager mimarisi içerisinde kaynakları gruplandırmak için kullanılan kapsayıcılara verilen isimdir. Grupları kullanım şekline göre (development, staging, live, prod) projeye ya da departman adına göre kaynak gruplarının ayırıp yönetimini sağlayabiliriz.

> _Her kaynak bir kaynak grubuna bağlı olmak zorundadır. Kaynak grubu içerisinde farklı veri merkezlerindende ki kaynakları içerebilir ve bir kaynak grubunun sildiğiniz taktirde o kaynak grubunun içerisindeki tüm kaynaklarda silinecektir._

Kaynak grubu sayesinde kullanabileceğiniz özellikler ise aşağıdaki gibidir.

* **Role Based Access Control**: Tanımladığınız role bazında Azure Resource Group’lara yetki verebiliyorsunuz. Örnek vermek gerekirse, bilgi işlem adına oluşturduğunuz bir kaynak grubunun içerisinde yer alan kaynaklara yetkisi olmayan bir kimse ulaşamıyor.
* **Kaynakların etiketlenmesi (Tag)**: Tanımlanan kaynak grubuna etiketlendirme yapıp yönetimsel olarak hatırlatıcı etiketler tanımlayabilirsiniz.
* **Azure Tüketim ve Faturalandırma Yönetimi :** Hangi kaynak grubundan ötürü ne kadar bir bedel ödediğinizi görebilmenizi ve yönetmenizi sağlayabilirsiniz.
* **Resource Locks:** Kaynakların yanlışlıkla silinmesininin önüne geçebilirsiniz.
* **Audit Logs:** Kaynak gruplarına uyguladığınız yetkilendirmelerin erişim loglarını görebilirsiniz.

\
\
