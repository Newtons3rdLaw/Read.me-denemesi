# CR-None

## 📚 Table of Contents

- [ℹ️ About the Project](#about-the-project) ---
- [🧱 Built With](#built-with) ---
- [🚀 Introduction](#introduction)
- [⚡ Quick Start](#quick-start) ---
- [🧩 Usage](#usage) ---
- [🔧 More Options](#more-options) ---
- [🐞 Known Issues & Limitations](#known-issues--limitations) ---
- [🆘 Getting Help](#getting-help) ---
- [🤝 Contributing](#contributing)   ---contributing.md olacak
- [📜 License](#license)   ---licence.md olacak
- [🙏 Acknowledgments](#acknowledgments)   --- silsek mi?


## ℹ️ About the Project
Bu proje, kurum içi sorumluların kitlelere yönelik dağıtım organizasyonlarını planlayabildiği, gruplandırabildiği ve şablonlanabildiği bir web uygulamasıdır.
Yetkili kullanıcılar dağıtım etkinlikleri oluşturur, birden fazla Excel dosyasından gelen katılımcı listelerini sisteme aktarır, tanımlanmış kurallara göre gruplar ve her kişi için sahada kullanılabilecek çıktı dokümanları üretir.

Sistem, mevcut kaynak sayısı ile hak sahibi kişi sayısı birebir uyuşmadığında bile adil paylaşım kurallarını uygulayarak, kimin hangi şablon altında ne aldığının izlenebilir olmasını amaçlar.​

## 🧱 Built With
Bu projede kullanılan başlıca teknolojiler:

### Backend

[Laravel 12](https://pip.pypa.io/en/stable/)  (laravel/framework)
​

[Laravel Fortify](https://pip.pypa.io/en/stable/)  (authentication)
​

[Laravel Sanctum](https://pip.pypa.io/en/stable/)  (API / token auth)
​

[Laravel Telescope](https://pip.pypa.io/en/stable/)  (debugging & monitoring)
​

[Laravel Tinker](https://pip.pypa.io/en/stable/)  (artisan REPL)
​

[Spatie Activitylog](https://pip.pypa.io/en/stable/)  (kullanıcı aksiyon loglama)
​

[Spatie Query Builder](https://pip.pypa.io/en/stable/)  (filtreleme / sıralama / include)
​

[Maatwebsite Excel](https://pip.pypa.io/en/stable/)  (Excel içe/dışa aktarma)
​

[TCPDF & FPDI](https://pip.pypa.io/en/stable/)  (PDF oluşturma / birleştirme)
​

[Tighten Ziggy](https://pip.pypa.io/en/stable/)  (Laravel route’larını JS tarafında kullanma)
​

### Frontend

[Vite](https://pip.pypa.io/en/stable/)  (build tool)
​

[Tailwind](https://pip.pypa.io/en/stable/)  CSS 4
​

[Alpine.js](https://pip.pypa.io/en/stable/)  (+ collapse, focus, persist eklentileri)
​

[FullCalendar](https://pip.pypa.io/en/stable/)  (takvim & event görselleştirme)
​

[ApexCharts](https://pip.pypa.io/en/stable/)  (grafikler)
​

[Dropzone](https://pip.pypa.io/en/stable/)  (dosya yükleme)
​

[Flatpickr](https://pip.pypa.io/en/stable/) (tarih/saat picker)


[Tabulator](https://pip.pypa.io/en/stable/)  (tablo & grid)
​

[Konva](https://pip.pypa.io/en/stable/)  (canvas tabanlı görselleştirme)
​

[xlsx](https://pip.pypa.io/en/stable/)  (Excel okuma/yazma)
​

[Ziggy JS](https://pip.pypa.io/en/stable/)  (route helper)
​

### Veritabanı & Ortam

[MySQL](https://pip.pypa.io/en/stable/)  (DB_CONNECTION=mysql, DB_PORT=3306)
​

[Laravel Herd](https://pip.pypa.io/en/stable/)  (local PHP/Laravel runtime, development environment)
​

[DBngin](https://pip.pypa.io/en/stable/)  (lokal veritabanı yönetimi)
​​
### PHP & Laravel bağımlılıklarını yüklemek için, proje dizininde yalnızca 
```bash
composer install
```
komutunu çalıştırmanız yeterlidir; gerekli paketler require ve require-dev bölümlerinde tanımlanmıştır.

### Tüm JavaScript bağımlılıklarını yüklemek için, proje dizininde yalnızca 
```bash
npm install 
```
komutunu çalıştırmanız yeterlidir; gerekli paketler package.json içindeki dependencies ve devDependencies bölümlerinde listelenmiştir.


## 🚀 Introduction
Bu proje, dağıtım organizasyonlarını Excel tabanlı kişi listeleri üzerinden uçtan uca yönetebilmek için geliştirilmiş, kurum içi kullanıma yönelik bir yönetim panelidir.
​
Amaç; farklı kaynak ve kapasite kısıtları altında, çok sayıda hak sahibini adil ve izlenebilir şekilde gruplandırmak, her bir kişi için standart bir çıktı üretmek ve tüm süreci daha az manuel iş yüküyle yürütmektir.
​

Genel olarak dağınık Excel dosyaları ve manuel hesaplamalarla yapılan planlama süreci; bu uygulama sayesinde tek bir arayüzde toplanır, tekrar kullanılabilir şablonlar ve otomatik gruplama kurallarıyla daha tutarlı ve denetlenebilir hale gelir.

## ⚡ Quick Start
1- Depoyu klonla ve dizine gir:
```bash
git clone https://github.com/username/cr-none.git
cd cr-none
```
2- PHP & Laravel bağımlılıklarını yükle:
```bash
composer install
```
3- JavaScript bağımlılıklarını yükle:
```bash
npm install 
```
4- Ortam dosyasını oluştur ve uygulama anahtarını üret:
```bash
cp .env.example .env
php artisan key:generate
```
5- Veritabanı ayarlarını .env içinde yapılandır:
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=crnone_db
DB_USERNAME=root
DB_PASSWORD=
```
6- Test verisi (isteğe bağlı)
Projede hazır factory ve seeder’lar bulunduğu için, uygulamayı hızlıca denemek amacıyla test verisi oluşturabilirsiniz:
```bash
php artisan migrate --seed
```
#### (Bu adım zorunlu değildir ancak projeyi ilk kez kuranlar için, ekranları ve akışı hızlıca test etmeyi kolaylaştırır.)
7- Geliştirme sunucusunu ve asset derleyicisini başlat:
```bash
php artisan serve
npm run dev
```

## 🧩 Usage
Kurulum tamamlandıktan sonra yetkili kullanıcılar web arayüzüne giriş yaparak dört temel kavram üzerinden çalışır: organ'zasyonlar, katılımcı dosyaları, dosyalama ve şablonlar.

* Önce yeni bir dağıtım etkinliği oluşturulur ve tür, yerve tarih aralığı gibi temel parametreler tanımlanır.

* Ardından, hak sahibi kişilerin bulunduğu birden fazla Excel dosyası yüklenir; sistem bu dosyaları birleştirir, temel kontrolleri yapar ve grupla işlemeye hazır hale getirir.

* Tanımlı şablonlar kullanılarak paylaşım kuralları uygulanır ve her hak sahibi için, hem kişiyi hem de sorumlu kuruluşu gösteren A4 boyutunda çıktılar üretilir.

Oluşturulan çıktılar toplu olarak indirilebilir veya yazdırılabilir; sahada doğrulama amacıyla kullanılabilir ve sonrasında ilgili paydaşlara raporlama için saklanabilir.

## 🔧 More Options
Temel akışın yanı sıra, kurum bazinda gelişmiş seçenekler de sunulur.

#### Özel şablonlar: 
Farklı destekçi kuruluşlar, kapasiteler veya dağıtım modelleri için birden fazla şablon tanımlanabilir ve bu şablonlar farklı etkinliklerde tekrar kullanılabilir.

#### Esnek gruplama kuralları: 
Grup boyutları ve paylaşım mantığı yapılandırılabilir; böylece aynı altyapı, farklı senaryolara uyarlanabilir ve kod değişikliği gerektirmez.

📝 Tunahan’ın eksik gördüğü veya daha ayrıntılı anlatılmasını önerdiği her şeyi burada topla.

## 🐞 Known Issues & Limitations
Şu anda bu projeyle ilgili bilinen bir hata veya kısıtlama bulunmamaktadır.
Herhangi bir sorunla karşılaşırsanız, lütfen bir issue açarak veya katkıda bulunarak geri bildirim sağlamaktan çekinmeyin.
(Max yuklenebilen excel var mi? Belli bir noktadan sonra kasma yada calismama oluyor mu arastir.)

## 🆘 Getting Help
Projeyi kullanırken yardıma ihtiyaç duyarsanız aşağıdaki kişilerle iletişime geçebilirsiniz:

👨‍💻 Ali Kemal Özdemir – 
@akozdem
​

👨‍💻 Mahmut Coşkun – 
@mahmutcskn
​

👨‍💻 Tunahan Öztürk – 
@


Geri bildirim, hata raporu veya katkı önerileriniz için GitHub üzerinden issue açabilir veya doğrudan bu profiller üzerinden ulaşabilirsiniz.

## 🤝 Contributing
Katkıda bulunmak istersen adımlar genelde şöyledir:
​

Depoyu fork et.

Yeni bir branch oluştur: feature/my-feature.

Değişikliklerini commit et.

Pull Request aç.

Eğer bir CONTRIBUTING.md dosyan varsa, detaylı rehber için buraya link ekle:

📄 Detaylı katkı rehberi için bkz: CONTRIBUTING.md

Örnek bir katkı rehberi için:
https://github.com/mhucka/readmine/blob/main/CONTRIBUTING.md
​

## 📜 License
Bu projede hangi lisansın kullanıldığını burada belirt:
​

Örneğin: “Bu proje MIT lisansı ile lisanslanmıştır. Ayrıntılar için LICENSE dosyasına bakınız.”

Lisans metnini repo köküne LICENSE dosyası olarak eklemeyi unutma.

## 🙏 Acknowledgments
Bu bölümde projeye doğrudan veya dolaylı katkısı olan kişi ve projelere teşekkür edebilirsin:
​

İlham alınan projeler.

Kullandığın önemli açık kaynak kütüphaneler.

AfroTech ekibi veya bireysel katkı sağlayan arkadaşların.

💐 Örnek: “Bu proje, X projesinden ilham alınarak geliştirilmiştir.” veya “Y kütüphanesinin geliştiricilerine teşekkürler.”
