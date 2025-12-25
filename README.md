<img width="315" height="118" alt="image" src="https://github.com/user-attachments/assets/fbabeb10-b258-4e25-b205-f785551db8db" />

# Reference Console (English)

## 📚 Table of Contents

- [ℹ️ About the Project](#about-the-project) 
- [🧱 Built With](#built-with) 
- [🏗️ Architecture](#architecture)
- [⚡ Quick Start](#quick-start) 
- [🧩 Usage](#usage) 
- [🔧 More Options](#more-options) 
- [🐞 Known Issues & Limitations](#known-issues--limitations) 
- [🆘 Getting Help](#getting-help) 
- [📜 License](#license)   



## ℹ️ About the Project
This project is a web application that allows internal managers to plan, group, and template distribution organizations for the masses. Authorized users create distribution events, import participant lists from multiple Excel files into the system, group them according to defined rules, and generate output documents for each person that can be used in the field. The system aims to ensure that it is traceable who received what under which template, by applying fair sharing rules even when the number of available resources does not exactly match the number of eligible individuals.​

## 🧱 Built With
The main technologies used in this project are:

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

[Spatie Activitylog](https://spatie.be/docs/laravel-activitylog/v4/introduction)  (user action logging)
​

[Spatie Query Builder](https://github.com/spatie/laravel-query-builder)  (Filtering / Sorting/ include)
​

[Maatwebsite Excel](https://packagist.org/packages/maatwebsite/excel)  (Import/export from Excel)
​

[TCPDF & FPDI]()  (Creating/merging PDFs)
​

[Tighten Ziggy](https://github.com/tighten/ziggy)  (Using Laravel routes on the JavaScript side)
​

### Frontend
[TailAdmin](https://tailadmin.com/)  (Theme)


[Laravel Echo](https://laravel.com/docs/12.x/broadcasting)  (JS Listener)


[Vite](https://vite.dev/)  (build tool)
​

[Tailwind](https://tailwindcss.com/)  (CSS 4)
​

[Alpine.js](https://alpinejs.dev/)  (+ collapse, focus, persist plugins)
​

[Flatpickr](https://flatpickr.js.org/) (date/time picker)


[Tabulator](https://tabulator.info/)  (table & grid)
​

[Konva](https://konvajs.org/)  (canvas-based visualization)
​​​

### Database & Environment

[MySQL](https://www.mysql.com/)  (DB_CONNECTION=mysql, DB_PORT=3306)
​

[Laravel Herd](https://herd.laravel.com/windows)  (local PHP/Laravel runtime, development environment)
​

[DBngin](https://dbngin.com/)  (local database management)
​​
### To install PHP & Laravel dependencies, simply run the following command in the project directory:

```bash
composer install
```


### To install all JavaScript dependencies, simply run the following command in the project directory:

```bash
npm install
```

The required packages are listed in the dependencies and devDependencies sections of package.json.

### To compile JavaScript assets, simply run the following command in the project directory:
```bash
npm run dev
```
The assets will be compiled and updated in the development environment.

## 🏗️ Architecture
CQRS + Vertical Slice Architecture
```bash
Controller → Request → Action(Command/Query) → Model
```

## ⚡ Quick Start
1- Clone the repository and enter the directory:
```bash
git clone https://github.com/username/cr-none.git
cd cr-none
```
2- Install PHP & Laravel dependencies:
```bash
composer install
```
3- Install JavaScript dependencies:
```bash
npm install
```
4- Create the environment file and generate the application key:
```bash
cp .env.example .env
php artisan key:generate
```
5- Configure database settings in .env:
```bash
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=crnone_db
DB_USERNAME=root
DB_PASSWORD=
```
6- Test data (Optional)
Since the project includes ready-made factories and seeders, you can create test data to quickly test the application:
```bash
php artisan migrate --seed
```
#### (This step is not mandatory, but for those setting up the project for the first time, it makes it easier to quickly test the screens and flow.)
7- Start the development server and asset compiler:
```bash
php artisan serve
npm run build
```

## 🧩 Usage
After the installation is complete, authorized users log into the web interface and work with four basic concepts: organizations, participant files, filing, and templates.

* First, a new deployment activity is created and basic parameters such as type, location, and date range are defined.

* Then, multiple Excel files containing the rights holders are uploaded; the system combines these files, performs basic checks, and prepares them for group processing.

* Sharing rules are implemented using defined templates, and A4-sized outputs are generated for each rights holder, showing both the individual and the responsible organization.

The generated outputs can be downloaded or printed in bulk; they can be used for verification purposes in the field and then saved for reporting to relevant stakeholders.

## 🔧 More Options
In addition to the basic workflow, advanced options are also offered on an organization basis.

#### Custom Templates:

Multiple templates can be defined for different supporting organizations, capacities, or distribution models, and these templates can be reused in different events.

#### Flexible Grouping Rules:

Group sizes and sharing logic can be configured; thus, the same infrastructure can be adapted to different scenarios without requiring code changes.

## 🐞 Known Issues & Limitations
Currently, there are no known bugs or limitations related to this project. If you encounter any issues, please feel free to provide feedback by opening an issue or contributing.

## 🆘 Getting Help
If you need help while using the project, you can contact the following people:


👨‍💻 Ali Kemal Özdemir – 
@akozdem
​

👨‍💻 Mahmut Coşkun – 
@mahmutcskn
​

👨‍💻 Tunahan Öztürk – 
@tnhnOzturk-0

For feedback, bug reports, or suggestions, you can address the issue via GitHub or directly through these profiles.

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.


# Reference Console (Türkçe)

## 📚 İçindekiler

- [ℹ️ Proje Hakkında](#proje-hakkında)
- [🧱 Kullanılan Araçlar](#kullanılan-araçlar)
- [🏗️ Mimari](#mimari)
- [⚡ Hızlı Başlangıç](#hızlı-başlangıç)
- [🧩 Kullanım](#kullanım)
- [🔧 Daha Fazla Seçenek](#daha-fazla-seçenek)
- [🐞 Bilinen Sorunlar ve Sınırlamalar](#bilinen-sorunlar-ve-sınırlamalar)
- [🆘 Yardım Alma](#yardım-alma)
- [📜 Lisans](#lisans)



## ℹ️ Proje Hakkında
Bu proje, kurum içi sorumluların kitlelere yönelik dağıtım organizasyonlarını planlayabildiği, gruplandırabildiği ve şablonlanabildiği bir web uygulamasıdır.
Yetkili kullanıcılar dağıtım etkinlikleri oluşturur, birden fazla Excel dosyasından gelen katılımcı listelerini sisteme aktarır, tanımlanmış kurallara göre gruplar ve her kişi için sahada kullanılabilecek çıktı dokümanları üretir.

Sistem, mevcut kaynak sayısı ile hak sahibi kişi sayısı birebir uyuşmadığında bile adil paylaşım kurallarını uygulayarak, kimin hangi şablon altında ne aldığının izlenebilir olmasını amaçlar.​

## 🧱 Kullanılan Araçlar
Bu projede kullanılan başlıca teknolojiler:

### Backend

[Laravel 12](https://laravel.com/)  (laravel/framework)
​

[Laravel Fortify](https://laravel.com/docs/12.x/fortify)  (Kimlik doğrulama)
​

[Laravel Sanctum](https://laravel.com/docs/12.x/sanctum)  (API / token doğrulama)
​

[Laravel Telescope](https://laravel.com/docs/12.x/telescope)  (Hata ayıklama ve izleme)
​

[Laravel Queue](https://laravel.com/docs/12.x/queues)  (Arka Plan İşleri)


[Laravel Reverb](https://laravel.com/docs/12.x/reverb#main-content)  (WebSocket Sunucusu)
​

[Spatie Activitylog](https://spatie.be/docs/laravel-activitylog/v4/introduction)  (Kullanıcı Aksiyon Loglama)
​

[Spatie Query Builder](https://github.com/spatie/laravel-query-builder)  (filtreleme / sıralama / dahil etme)
​

[Maatwebsite Excel](https://packagist.org/packages/maatwebsite/excel)  (Excel içe/dışa aktarma)
​

[TCPDF & FPDI]()  (PDF oluşturma / birleştirme)
​

[Tighten Ziggy](https://github.com/tighten/ziggy)  (Laravel route’larını JS tarafında kullanma)
​

### Frontend
[TailAdmin](https://tailadmin.com/)  (Tema)


[Laravel Echo](https://laravel.com/docs/12.x/broadcasting)  (JS Listener)


[Vite](https://vite.dev/)  (build tool)
​

[Tailwind](https://tailwindcss.com/)  (CSS 4)
​

[Alpine.js](https://alpinejs.dev/)  (+ collapse, focus, persist eklentileri)
​

[Flatpickr](https://flatpickr.js.org/) (tarih/saat seçici)


[Tabulator](https://tabulator.info/)  (tablo & grid)
​

[Konva](https://konvajs.org/)  (canvas tabanlı görselleştirme)
​​​

### Veritabanı & Ortam

[MySQL](https://www.mysql.com/)  (DB_CONNECTION=mysql, DB_PORT=3306)
​

[Laravel Herd](https://herd.laravel.com/windows)  (yerel PHP/Laravel çalışma ortamı, geliştirme ortamı)
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

## 🏗️ Mimari
CQRS + Vertical Slice Mimarisi
```bash
Controller → Request → Action(Command/Query) → Model
```

## ⚡ Hızlı Başlangıç
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

## 🧩 Kullanım
Kurulum tamamlandıktan sonra yetkili kullanıcılar web arayüzüne giriş yaparak dört temel kavram üzerinden çalışır: organizasyonlar, katılımcı dosyaları, dosyalama ve şablonlar.

* Önce yeni bir dağıtım etkinliği oluşturulur ve tür, yerve tarih aralığı gibi temel parametreler tanımlanır.

* Ardından, hak sahibi kişilerin bulunduğu birden fazla Excel dosyası yüklenir; sistem bu dosyaları birleştirir, temel kontrolleri yapar ve grupla işlemeye hazır hale getirir.

* Tanımlı şablonlar kullanılarak paylaşım kuralları uygulanır ve her hak sahibi için, hem kişiyi hem de sorumlu kuruluşu gösteren A4 boyutunda çıktılar üretilir.

Oluşturulan çıktılar toplu olarak indirilebilir veya yazdırılabilir; sahada doğrulama amacıyla kullanılabilir ve sonrasında ilgili paydaşlara raporlama için saklanabilir.

## 🔧 Daha Fazla Seçenek
Temel akışın yanı sıra, kurum bazinda gelişmiş seçenekler de sunulur.

#### Özel şablonlar: 
Farklı destekçi kuruluşlar, kapasiteler veya dağıtım modelleri için birden fazla şablon tanımlanabilir ve bu şablonlar farklı etkinliklerde tekrar kullanılabilir.

#### Esnek gruplama kuralları: 
Grup boyutları ve paylaşım mantığı yapılandırılabilir; böylece aynı altyapı, farklı senaryolara uyarlanabilir ve kod değişikliği gerektirmez.


## 🐞 Bilinen Sorunlar ve Sınırlamalar
Şu anda bu projeyle ilgili bilinen bir hata veya kısıtlama bulunmamaktadır.
Herhangi bir sorunla karşılaşırsanız, lütfen bir issue açarak veya katkıda bulunarak geri bildirim sağlamaktan çekinmeyin.


## 🆘 Yardım Almak
Projeyi kullanırken yardıma ihtiyaç duyarsanız aşağıdaki kişilerle iletişime geçebilirsiniz:

👨‍💻 Ali Kemal Özdemir – 
@akozdem
​

👨‍💻 Mahmut Coşkun – 
@mahmutcskn
​

👨‍💻 Tunahan Öztürk – 
@tnhnOzturk-0

Geri bildirim, hata raporu veya katkı önerileriniz için GitHub üzerinden issue açabilir veya doğrudan bu profiller üzerinden ulaşabilirsiniz.

## 📜 Lisans
Bu proje MIT Lisansı altında lisanslanmıştır - ayrıntılar için [LICENSE](LICENSE.md) dosyasına bakın.









