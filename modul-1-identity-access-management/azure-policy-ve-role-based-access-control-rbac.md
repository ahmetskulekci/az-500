# Azure Policy ve Role-Based Access Control (RBAC)

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*GbC032v6NBdqBNEx.png" alt=""><figcaption></figcaption></figure>

Azure Policy ve RBAC Akışı

Azure Policy ile RBAC arasında birkaç önemli fark vardır. Azure Policy, bazı Kaynak Sağlayıcılarının Resource Manager ve özelliklerinde temsil edilen kaynaklardaki özellikleri inceleyerek durumu değerlendirir. Azure Policy, kaynak durumunun, değişikliği kimin yaptığı veya değişiklik yapma iznine sahip olduğu endişesi olmadan iş kurallarınızla uyumlu olmasını sağlar. DenyAction etkisi aracılığıyla Azure Policy, kaynaklardaki belirli eylemleri de engelleyebilir.

Azure RBAC, farklı kapsamlarda kullanıcı [eylemlerini](https://learn.microsoft.com/tr-tr/azure/role-based-access-control/resource-provider-operations) yönetmeye odaklanır. Kullanıcı bilgilerine bağlı olarak bir eylemin denetimi gerekiyorsa, Azure RBAC kullanılacak doğru araçtır. Bir kişinin eylem gerçekleştirme erişimi olsa bile, sonuç uyumlu olmayan bir kaynaksa Azure İlkesi yine de oluşturma veya güncelleştirme işlemini engellemektedir.

Azure RBAC ve Azure Policy birleşimi, Azure’da tam kapsamlı denetim sağlar. (Alıntı: [https://learn.microsoft.com/tr-tr/azure/governance/policy/overview](https://learn.microsoft.com/tr-tr/azure/governance/policy/overview))
