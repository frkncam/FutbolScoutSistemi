# Futbol Scout Sistemi
•2.Öğretim Çift 16.grup

•Furkan ÇAM-225260044

•Yunus Emre İNEL-225260040

•Davut KARAGÖL-225260136

Futbol scout sistemi veritabanı projesi, futbol kulüplerinin ve scout (gözlemci) ekiplerinin oyuncu takibi, analiz ve transfer süreçlerini daha etkin bir şekilde yönetmelerine yardımcı olmayı amaçlamaktadır. Bu sistem, oyuncu performans verilerinin, sakatlık geçmişlerinin, transfer kayıtlarının ve maç istatistiklerinin merkezi bir veritabanında depolanmasını ve analiz edilmesini sağlar.

# Varlık-Özellik Tablosu:

| **Varlıklar**           | **Özellikler**                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Oyuncu**              | Oyuncu ID, Ad, Soyad, Uyruk, Doğum Tarihi                                                                          |
| **Takım**               | Takım ID, Takım Adı, Ülke, Lig ID, Menajer ID                                                                      |
| **Lig**                 | Lig ID, Lig Adı, Ülke                                                                                               |
| **Pozisyon**            | Pozisyon ID, Pozisyon Adı                                                                                           |
| **Rol**                 | Rol ID, Rol Adı                                                                                                     |
| **Transfer Kaydı**      | Transfer ID, Transfer Tarihi, Eski Takım ID, Yeni Takım ID, Oyuncu ID, Transfer Ücreti                               |
| **Menajer**             | Menajer ID, Ad, Soyad, Telefon                                                                                      |
| **Sakatlık**            | Sakatlık ID, Oyuncu ID, Yaralanma Tipi, Başlangıç Tarihi, Bitiş Tarihi                                             |
| **Rapor**               | Rapor ID, Rapor Tarihi, İçerik, Scout ID, Oyuncu ID                                                                 |
| **Maç İstatistikleri**  | İstatistik ID, Maç ID, Şut Sayısı, Faul Sayısı, Kırmızı Kart, Sarı Kart                                           |
| **Stadyum**             | Stadyum ID, Stadyum Ad, Şehir, Kapasite                                                                            |
| **Maç**                 | Maç ID, Tarih, Stadyum ID, Takım1 ID, Takım2 ID, Sonuç                                                             |
| **Performans Kaydı**    | Performans ID, Tarih, Oyuncu ID, Maç ID, Dakika, Gol Sayısı, Asist Sayısı, Pozisyon, Scout Yorum                   |
| **Scout**               | Scout ID, Ad, Soyad, Uzmanlık Alanı, Çalışma Bölgesi, Rol ID                                                       |

# Varlık İlişki Tablosu

Bu tablo, veritabanındaki varlıklar arasındaki ilişkileri göstermektedir:

| İlişki                 | Açıklama                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Oyuncu - Performans Kaydı** (1-N) | Bir oyuncu, birden fazla performans kaydına sahip olabilir. Ancak her performans kaydı yalnızca bir oyuncuya aittir. |
| **Oyuncu - Rapor** (1-N)           | Bir oyuncu hakkında birden fazla rapor oluşturulabilir. Ancak her rapor yalnızca bir oyuncuya aittir.       |
| **Oyuncu - Takım** (N-1)           | Bir oyuncu aynı anda sadece bir takımda olabilir. Fakat bir takımda birden fazla oyuncu bulunabilir.       |
| **Oyuncu - Transfer Kaydı** (1-N)  | Bir oyuncunun birden fazla transfer kaydı olabilir. Ancak her transfer kaydı yalnızca bir oyuncuya aittir. |
| **Oyuncu - Sakatlık** (1-N)        | Bir oyuncunun birden fazla sakatlık kaydı olabilir. Her sakatlık kaydı yalnızca bir oyuncuya aittir.       |
| **Oyuncu - Pozisyon** (N-M)        | Bir oyuncu birden fazla pozisyonda oynayabilir. Aynı zamanda bir pozisyonda birden fazla oyuncu bulunabilir. Bu ilişki çift yönlü çoktan-çoka (N-M) bir ilişkidir. |
| **Scout - Performans Kaydı** (1-N) | Bir scout birden fazla performans kaydı oluşturabilir. Ancak her performans kaydı yalnızca bir scout tarafından oluşturulabilir. |
| **Scout - Rapor** (1-N)            | Bir scout, birden fazla rapor oluşturabilir. Ancak her rapor yalnızca bir scout'a aittir.                |
| **Scout - Rol** (N-1)              | Birden fazla scout aynı role sahip olabilir. Ancak her scout yalnızca bir role sahip olabilir.            |
| **Takım - Transfer Kaydı** (1-N)   | Bir takımın birden fazla transfer kaydı olabilir. Ancak her transfer kaydı yalnızca bir takıma aittir.   |
| **Takım - Lig** (N-1)              | Birden fazla takım aynı ligde olabilir. Ancak her takım yalnızca bir ligde yer alır.                     |
| **Takım - Menajer** (N-1)          | Birden fazla takım aynı menajer tarafından yönetilebilir. Ancak her takım yalnızca bir menajer tarafından yönetilir. |
| **Maç - Performans Kaydı** (N-1)   | Bir maçta birden fazla performans kaydı olabilir. Ancak her performans kaydı yalnızca bir maç için geçerlidir. |
| **Maç - Stadyum** (N-1)            | Birden fazla maç aynı stadyumda oynanabilir. Ancak her maç yalnızca bir stadyumda yapılır.                |
| **Maç - Maç İstatistikleri** (1-1) | Her maçın yalnızca bir istatistik kaydı vardır ve her istatistik kaydı yalnızca bir maça aittir. Bu, bire bir (1-1) bir ilişki türüdür. |


# Projenin E-R diyagramı aşağıda gösterilmiştir:

![futbolScout](https://github.com/user-attachments/assets/914d655e-53b1-47dd-bc85-37760b1a11ae)
