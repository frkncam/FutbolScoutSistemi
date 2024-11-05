# FutbolScoutSistemi
•2.Öğretim Çift 16.grup

•Furkan ÇAM-225260044

•Yunus Emre İNEL-225260040

•Davut KARAGÖL-225260136

Futbol scout sistemi veritabanı projesi, futbol kulüplerinin ve scout (gözlemci) ekiplerinin oyuncu takibi, analiz ve transfer süreçlerini daha etkin bir şekilde yönetmelerine yardımcı olmayı amaçlamaktadır. Bu sistem, oyuncu performans verilerinin, sakatlık geçmişlerinin, transfer kayıtlarının ve maç istatistiklerinin merkezi bir veritabanında depolanmasını ve analiz edilmesini sağlar.

# Varlık-Özellik Tablosu:

| **Varlıklar**           | **Özellikler**                                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------------------------------|
| **Oyuncu**              | Oyuncu ID, Ad, Soyad, Uyruk, Doğum Tarihi                                                                          |
| **Takım**               | Takım ID, Takım Adı, Ülke, Lig Adı, Menajer ID                                                                      |
| **Lig**                 | Lig ID, Lig Adı, Ülke                                                                                               |
| **Pozisyon**            | Pozisyon ID, Pozisyon Adı                                                                                           |
| **Rol**                 | Rol ID, Rol Adı                                                                                                     |
| **Transfer Kaydı**      | Transfer ID, Transfer Tarihi, Eski Takım ID, Yeni Takım ID, Transfer Ücreti                                        |
| **Menajer**             | Menajer ID, Ad, Soyad, Telefon                                                                                      |
| **Sakatlık**            | Sakatlık ID, Oyuncu ID, Yaralanma Tipi, Başlangıç Tarihi, Bitiş Tarihi                                             |
| **Rapor**               | Rapor ID, Rapor Tarihi, İçerik, Scout ID, Oyuncu ID                                                                 |
| **Maç İstatistikleri**  | İstatistik ID, Maç ID, Şut Sayısı, Faul Sayısı, Kırmızı Kart, Sarı Kart                                           |
| **Stadyum**             | Stadyum ID, Stadyum Ad, Şehir, Kapasite                                                                            |
| **Maç**                 | Maç ID, Tarih, Stadyum ID, Takım1 ID, Takım2 ID, Sonuç                                                             |
| **Performans Kaydı**    | Performans ID, Tarih, Maç ID, Dakika, Gol Sayısı, Asist Sayısı, Pozisyon, Scout Yorum                              |
| **Scout**               | Scout ID, Ad, Soyad, Uzmanlık Alanı, Çalışma Bölgesi, Rol ID                                                       |

# Varlık İlişki Tablosu

Bu tablo, veritabanındaki varlıklar arasındaki ilişkileri göstermektedir:

| **Varlık 1** | **Varlık 2**           | **İlişki** |
|--------------|------------------------|------------|
| Oyuncu       | Performans Kaydı       | 1-N        |
| Oyuncu       | Rapor                  | 1-N        |
| Oyuncu       | Takım                  | 1-N        |
| Oyuncu       | Transfer Kaydı         | 1-N        |
| Oyuncu       | Sakatlık               | 1-N        |
| Scout        | Performans Kaydı       | 1-N        |
| Scout        | Rapor                  | 1-N        |
| Scout        | Rol                    | N-1        |
| Takım        | Transfer Kaydı         | 1-N        |
| Takım        | Lig                    | N-1        |
| Takım        | Menajer                | N-1        |
| Maç          | Performans Kaydı       | N-1        |
| Maç          | Stadyum                | N-1        |
| Maç          | Maç İstatistikleri     | 1-1        |
| Oyuncu       | Pozisyon               | N-M        |

# Projenin E-R diyagraımı aşağıda gösterilmiştir:

![image]()

