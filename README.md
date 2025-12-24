<img width="315" height="118" alt="image" src="https://github.com/user-attachments/assets/fbabeb10-b258-4e25-b205-f785551db8db" />

# Reference Console

## 📚 Table of Contents

- [ℹ️ About the Project](#ℹ️-about-the-project) 
- [🧱 Built With](#🧱-built-with) 
- [🏗️ Architecture](#🏗️-architecture)
- [⚡ Quick Start](#⚡-quick-start) 
- [🧩 Usage](#🧩-usage) 
- [🔧 More Options](#🔧-more-options) 
- [🐞 Known Issues & Limitations](#🐞-known-issues--limitations) 
- [🆘 Getting Help](#🆘-getting-help) 
- [📜 License](#📜-license)   


## ℹ️ About the Project
Bu proje, kurum içi sorumluların kitlelere yönelik dağıtım organizasyonlarını planlayabildiği, gruplandırabildiği ve şablonlanabildiği bir web uygulamasıdır.
Yetkili kullanıcılar dağıtım etkinlikleri oluşturur, birden fazla Excel dosyasından gelen katılımcı listelerini sisteme aktarır, tanımlanmış kurallara göre gruplar ve her kişi için sahada kullanılabilecek çıktı dokümanları üretir.

Sistem, mevcut kaynak sayısı ile hak sahibi kişi sayısı birebir uyuşmadığında bile adil paylaşım kurallarını uygulayarak, kimin hangi şablon altında ne aldığının izlenebilir olmasını amaçlar.​

## 🧱 Built With
Bu projede kullanılan başlıca teknolojiler:

### Backend

[Laravel 12](https://laravel.com/)  (laravel/framework)
​

[Laravel Fortify](https://laravel.com/docs/12.x/fortify)  (authentication)
​

[Laravel Sanctum](https://laravel.com/docs/12.x/sanctum)  (API / token auth)
​

[Laravel Telescope](https://laravel.com/docs/12.x/telescope)  (debugging & monitoring)
​

[Laravel Queue](https://laravel.com/docs/12.x/queues)  (Background Jobs)


[Laravel Reverb](https://laravel.com/docs/12.x/reverb#main-content)  (WebSocket Server)
​

[Spatie Activitylog](https://spatie.be/docs/laravel-activitylog/v4/introduction)  (kullanıcı aksiyon loglama)
​

[Spatie Query Builder](https://github.com/spatie/laravel-query-builder)  (filtreleme / sıralama / include)
​

[Maatwebsite Excel](https://packagist.org/packages/maatwebsite/excel)  (Excel içe/dışa aktarma)
​

[TCPDF & FPDI]()  (PDF oluşturma / birleştirme)
​

[Tighten Ziggy](https://github.com/tighten/ziggy)  (Laravel route’larını JS tarafında kullanma)
​

### Frontend
[TailAdmin](https://tailadmin.com/)  (Theme)


[Laravel Echo](https://laravel.com/docs/12.x/broadcasting)  (JS Listener)


[Vite](https://vite.dev/)  (build tool)
​

[Tailwind](https://tailwindcss.com/)  CSS 4
​

[Alpine.js](https://alpinejs.dev/)  (+ collapse, focus, persist eklentileri)
​

[Flatpickr](https://flatpickr.js.org/) (tarih/saat picker)


[Tabulator](https://tabulator.info/)  (tablo & grid)
​

[Konva](https://konvajs.org/)  (canvas tabanlı görselleştirme)
​​​

### Veritabanı & Ortam

[MySQL](https://www.mysql.com/)  (DB_CONNECTION=mysql, DB_PORT=3306)
​

[Laravel Herd](https://herd.laravel.com/windows)  (local PHP/Laravel runtime, development environment)
​

[DBngin](https://dbngin.com/)  (lokal veritabanı yönetimi)
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

### JavaScript asset'lerini derlemek için, proje dizininde
```bash
npm run dev
```
komutunu çalıştırmanız yeterlidir; geliştirme ortamında asset'ler derlenir ve güncellenir.

## 🏗️ Architecture
CQRS + Vertical Slice Architecture
```bash
Controller → Request → Action(Command/Query) → Model
```

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
npm run build
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


## 🐞 Known Issues & Limitations
Şu anda bu projeyle ilgili bilinen bir hata veya kısıtlama bulunmamaktadır.
Herhangi bir sorunla karşılaşırsanız, lütfen bir issue açarak veya katkıda bulunarak geri bildirim sağlamaktan çekinmeyin.


## 🆘 Getting Help
Projeyi kullanırken yardıma ihtiyaç duyarsanız aşağıdaki kişilerle iletişime geçebilirsiniz:

👨‍💻 Ali Kemal Özdemir – 
@akozdem
​

👨‍💻 Mahmut Coşkun – 
@mahmutcskn
​

👨‍💻 Tunahan Öztürk – 
@tnhnOzturk-0


## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.


Geri bildirim, hata raporu veya katkı önerileriniz için GitHub üzerinden issue açabilir veya doğrudan bu profiller üzerinden ulaşabilirsiniz.


