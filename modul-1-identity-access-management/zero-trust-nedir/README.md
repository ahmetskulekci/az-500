# Zero Trust Nedir?

Zero Trust modeli “güven” kelimesine göre hareket etmemiz gerektiğini, bunun yerine güveni sürekli olarak kontrol ve denetim altında tutmamızı belirtir. Siber güvenlikteki çoğu modelin askeri kökenli olduğu bir kez daha karşımıza çıkıyor. Almanların bir tabiri “ vertrauen ist gut kontrolle ist besser” veya bizdeki karşılığı olan “itimat kontrole mani değildir” bu modeli desteklemektedir.

Model, güvenlik duvarının (firewall) arkasındaki her şeyin güvenli olduğunu varsaymak yerine, ihlali varsayar ve her istek açık bir ağdan geliyormuş gibi doğrular. İsteğin nereden kaynaklandığına veya hangi kaynağa eriştiğine bakılmaksızın bize asla güvenmemeyi, her zaman doğrulamayı söyler. Her erişim isteği, erişim verilmeden önce tamamen doğrulanır, yetkilendirilir ve şifrelenir. Yanal hareketi (Lateral Movement Attacks) en aza indirmek için en az ayrıcalıklı erişim ilkeleri uygulanır.

<figure><img src="https://miro.medium.com/v2/resize:fit:1400/0*vpzw8zk8So7SK0to.png" alt=""><figcaption><p>Zero Trust Doğrulama Yöntemleri</p></figcaption></figure>

Modelde doğrulama için 4 ana bileşen bulunmaktadır.

* **Identity provider**. Bir kullanıcının kimliğini ve ilgili bilgileri belirler.
* **Device directory:** Bir cihazı ve cihaz bütünlüğünü doğrular.
* **Policy evaluation service:** Kullanıcının ve cihazın güvenlik politikalarına uygun olup olmadığını belirler.
* **Access proxy:** Erişilebilir kuruluş kaynakları belirler.

Zero Trust Politikaları

**Doğrulama:** Kullanıcı kimliği, konum, cihaz durumu, veri sınıflandırması ve anormallikler dahil olmak üzere her zaman mevcut tüm alanlara göre kimlik doğrulaması yapılması ve yetkilendirilmesidir.

**Kısıtlı Erişim:** Hem verileri hem de sürdürülebilirliği korumak için Tam Zamanında ve Tam Yeterli Erişim (JIT/JEA), risk tabanlı uyarlanabilir politikalar ve veri koruması ile kullanıcı erişiminin kısıtlanmasıdır.

**İhlale göre Aksiyon Planı:** Erişimi ağ, kullanıcı, cihazlar ve uygulama farkındalığına göre bölümlere ayırarak ihlaller için patlama yarıçapını en aza indirilmesi ve yanal hareketi önlenmesi için tatbikatlar ve planlar yapılmasıdır.
