# MithraByte Learning Intelligence

## 1. Proje nedir?

Dershanelerin öğrencileri daha iyi takip etmesini ve her öğrencinin neye çalışması gerektiğini anlamasını sağlayan bir eğitim platformu.

**Temel fikir:** Sistem yalnızca sınav sonucunu göstermez. Öğrencinin zorlandığı konuları takip eder, eski notlarını bulur ve uygun zamanda kısa tekrar önerir.

**Ana ilke:** Öğrencinin çalışma akışını bozma.

## 2. Ürün özellikleri

### Öğrenci
- Günlük çalışma planını görür.
- Görev başlatır, tamamlar veya erteler.
- Sınav sonuçlarını ve konu eksiklerini takip eder.
- Kendi notlarını kaydeder ve daha sonra arar.
- Yanlış yaptığı soruyla ilgili eski notlarını bulur.
- Kısa tekrar ve yeni soru önerileri alır.

### Öğretmen
- Sınıfını ve öğrencilerini takip eder.
- Deneme sınavı sonuçlarını yükler.
- Öğrencilerin zorlandığı konuları görür.
- Öğrenciye uygun çalışma önerileri hazırlar.

### Dershane yöneticisi
- Öğrenci, sınıf ve öğretmenleri yönetir.
- Sınav ve gelişim raporlarını görüntüler.
- Kurumun verilerine yalnızca yetkili kişilerin erişmesini sağlar.

### Yapay zekâ
- Öğrencinin notlarıyla ilgili kısa tekrar hazırlar.
- Yanlış soruları açıklamaya yardımcı olur.
- Öğretmene anlaşılır raporlar sunar.
- Gereksiz kişisel verileri almadan çalışır.
- Uygun kurulumlarda yerel veya bulut tabanlı çalışabilir.

## 3. Projeyi yapma yol haritası

### Aşama 1 — Temeli planla
- İlk sürümde hangi özelliklerin olacağını kesinleştir.
- Öğrenci, öğretmen ve yönetici yetkilerini belirle.
- Verilerin nerede ve ne kadar süre saklanacağını planla.
- Basit ekran taslaklarını hazırla.

**Çıktı:** Net kapsam, temel veri modeli ve ekran taslakları.

### Aşama 2 — Güvenli temel sistemi kur
- Next.js, TypeScript, PostgreSQL ve Prisma altyapısını kur.
- Giriş ve oturum sistemini ekle.
- Kurumları, sınıfları, öğrencileri ve öğretmenleri tanımla.
- Her kullanıcının yalnızca yetkili olduğu verilere erişmesini sağla.
- Güvenlik testleri ekle.

**Çıktı:** Kullanıcıların güvenli şekilde giriş yaptığı çalışan temel uygulama.

### Aşama 3 — Sınav analizini geliştir
- Deneme sonuçlarını elle girme ve CSV/Excel ile yükleme özelliği ekle.
- Doğru, yanlış ve boş cevapları konu bazında göster.
- Öğrencinin tekrar tekrar zorlandığı konuları belirle.
- Öğretmen ve dershane raporlarını hazırla.

**Çıktı:** Gerçek verilerle kullanılabilen sınav analiz modülü.

### Aşama 4 — Not sistemini geliştir
- Öğrencinin metin notu eklemesini sağla.
- Notları konu ve etiketlerle ilişkilendir.
- Notlarda arama yap.
- Yanlış yapılan soruyla ilgili eski notları bul.

**Çıktı:** Sınav sonucunu öğrencinin kendi notlarıyla ilişkilendiren sistem.

### Aşama 5 — Çalışma planını ekle
- Günlük görev ve çalışma oturumlarını oluştur.
- Konu eksiklerine ve sınav tarihine göre öncelik belirle.
- Öğrenci çalışırken planı durmadan değiştirme.
- Öğrenciye önerinin nedenini açıkla.

**Çıktı:** Öğrenciye neye çalışacağını öneren, akışı koruyan planlayıcı.

### Aşama 6 — Yapay zekâyı bağla
- Yerel ve bulut modelleri için ortak bir bağlantı katmanı oluştur.
- Notlardan kısa tekrarlar üret.
- Yanlış sorular için açıklamalar hazırla.
- Yapay zekânın yalnızca gerekli verilere erişmesini sağla.
- Sonuçları gerçek örneklerle test et.

**Çıktı:** Öğrencinin verilerine dayanan, kontrollü AI özellikleri.

### Aşama 7 — Pilot kullanım yap
- Bir dershane veya küçük bir öğrenci grubuyla dene.
- Hataları ve anlaşılmayan ekranları düzelt.
- Öğrenci ve öğretmenlerden geri bildirim al.
- Güvenlik, hız ve kullanım kolaylığını ölç.

**Çıktı:** Gerçek kullanıcılarla test edilmiş ilk sürüm.

## 4. İlk sürümde neler olmalı?

Önce şu akışı baştan sona çalıştır:

1. Öğrenci sisteme giriş yapar.
2. Deneme sınavı sonucu sisteme eklenir.
3. Sistem öğrencinin eksik olduğu konuyu bulur.
4. İlgili eski notu gösterir.
5. Kısa tekrar önerir.
6. Öğrencinin tekrar sonrası durumunu kaydeder.

Bu akış sorunsuz çalışmadan büyük bir soru bankası, canlı ders, mobil uygulama veya karmaşık AI özellikleri geliştirmeye başlama.

## 5. Teknik yapı

- **Arayüz ve API:** Next.js + TypeScript
- **Veritabanı:** PostgreSQL
- **Veri erişimi:** Prisma
- **İlk sürüm:** Mobil uyumlu web uygulaması / PWA
- **AI:** Yerel veya bulut modeline geçişi destekleyen ortak katman
- **Güvenlik:** Rol ve kurum bazlı erişim kontrolü, şifreli bağlantılar, güvenli oturumlar, yedekleme ve denetim kayıtları

Başlangıçta çok sayıda ayrı servis kurmak yerine, sınırları iyi belirlenmiş tek bir uygulama geliştir. İhtiyaç ortaya çıkarsa servisleri daha sonra ayır.

## 6. Şimdilik ertele

- Native iOS ve Android uygulamaları
- Büyük soru bankası
- Canlı ders ve sohbet
- El yazısı tanıma
- Kendi AI modelini eğitme
- Öğrenciyi sürekli izleyen özellikler

## 7. İlk iş listesi

- [ ] MVP kapsamını kesinleştir.
- [ ] Ekran taslaklarını çiz.
- [ ] Veritabanı modelini hazırla.
- [ ] Kurum ve rol bazlı erişim kurallarını yaz.
- [ ] Güvenli giriş sistemini geliştir.
- [ ] Sınav sonucu ekleme ve analizini yap.
- [ ] Not ekleme ve aramayı geliştir.
- [ ] Yanlış soru ile ilgili notu eşleştir.
- [ ] Kısa tekrar önerisini ekle.
- [ ] Küçük bir grupla pilot test yap.

**Başarı ölçütü:** Sistem, bir öğrencinin eksik konusunu bulup kendi notuyla ilişkilendirebilmeli ve doğru zamanda işe yarar bir tekrar önerebilmeli.
