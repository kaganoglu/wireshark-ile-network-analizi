# Wireshark ile Network Analizi

![1](https://user-images.githubusercontent.com/65306271/169202087-7278253c-5fa6-4929-853e-ec1a1a741566.png)

## Wireshark Nedir ?
Wireshark ağ trafiğini analiz etmek için, ağda hareket eden veri paketlerini yakalayan bir araçtır.

Özellikleri: 
- Ücretsiz ve açık kaynak kodludur.
- Windows, Linux, MacOS işletim sistemleri için uygundur. 
- Yerel ağ arayüzünden paketleri tutar, ayrıntılı bir şekilde protokol bilgileriyle görüntüler.
- Tutulan paketleri kaydetme özelliği vardır.
- Çeşitli kriterlerde paket arar ve filtreler.
- Paketleri filtrelemeye göre kategorize eder.
- Çeşitli istatistikleri kullanıcıya sunar.

(İndirme Linki : https://www.wireshark.org/#download)

**Açılış Arayüzü :**
![4](https://user-images.githubusercontent.com/65306271/169202100-c36d13dc-3dfb-4f71-ba3f-1f8c3a59980f.png)

1. Alan: Daha önce açılmış dosyalar görüntülenir.
2. Alan: "Capture Filter" için filtreleme komut alanı mevcuttur.
3. Alan: Cihazdaki newtork adaptörlerinin listesi yer alır ve bu adaptörler kullanıma göre seçilebilir.
4. Alan: Wireshark ile ilgili bazı linkler mevcuttur.
ve en yukarıda kısayol tuşları ile menü bulunmaktadır.

**Araç Çubuğu :**

![ws-main-toolbar](https://user-images.githubusercontent.com/65306271/170108609-5bf8ef40-557b-4771-826f-2a720ecb288f.png)

1. Başlat
2. Durdur
3. Yeniden Başlat
4. Ayarlar
5. Dosya Aç
6. Kaydet
7. Kapat
8. Yükle
9. Ara
10. Geri Dön
11. İleri Git
12. Pakete Git
13. İlk Pakete Git
14. Son Pakete Git
15. Otomatik kaydırma
16. Renklendir
17. Büyüt
18. Küçült
19. %100 Boyutlandır
20. Sütunları Boyutlandır

## Filtreleme
Wireshark, hem paket yakalama öncesi (Capture Filter) hem de sonrasında (Display Filter) filtreleme imkanı sunar. Bunun için bazı operatörler ve komutlar kullanılmaktadır.

### Mantıksal Operatörler

- `AND - &&` : Her iki filtreleme komutunun geçerli olduğu alanlar
- `OR - ||` : Filtreleme komutlarından en az birisinin ortak olduğu alanlar
- `NOT - !` : Belirtilen değeri içermeyen alanlar

### Karşılaştırma Operatörleri
- `==` Eşit olan
- `!=` Eşit olmayan
- `>` Büyüktür
- `<` Küçüktür
- `>=` Büyük Eşit
- `<=` Küçük Eşit

### Filtreleme Komutları

#### Host Filtreleme Komutları
- `host 192.168.53.41` IPv4
- `host 2001:98:A11:10:11:1:0:106` IPv6
- `ether host 68-7F-74-12-34-56` Mac Adres
- `src host 192.168.53.41` host Kaynak IP Adresi
- `dst host 192.168.53.41` host Hedef IP Adresi

#### Port Filtreleme Komutları
- `port 80` Tüm 80 portlu paketler
- `dst port 25` Kaynak Port
- `src port 5000` Hedef Port

#### Protokol Filtreleme Komutları
- `icmp` 
- `tcp`
- `ip`
- `http`
- `ftp`
- `broadcast`
- `...`

## Display Filter Kullanımı
Bu bölüm yakalanan paketler üzerinde filtreleme yapmak için kullanılır.

![2](https://user-images.githubusercontent.com/65306271/169202117-ba8dfa11-be3a-43a3-b404-e2d855c0bc09.png)

**Not:** Komutlar doğru yazıldığında alan yeşil, yanlış yazıldığında kırmızı olur. Ayrıca Display Filter komutlarında nokta operatörü kullanılarak alt komutlara ulaşılabilir.

Paket görüntüleme arayüzü:

![5](https://user-images.githubusercontent.com/65306271/169202860-9da591b2-0450-4cfa-9866-abe59877d6e4.png)

### Display Filter Yapısı:

![6](https://user-images.githubusercontent.com/65306271/169205905-d70ba587-b1b3-4d60-9a07-49bd526d4fa0.png)

Örnek : `http.request.method == "GET" && arp`
- `http` : Protokol
- `request` : Protokol değeri
- `method` : Protokol alt değeri
- `==` : Karşılaştırma operatörü 
- `GET` : Değer
- `&&` : Mantıksal Operatör
- `arp` : Diğer değer

En çok kullanılan filtrelere repo içerisinden erişebilirsiniz.
