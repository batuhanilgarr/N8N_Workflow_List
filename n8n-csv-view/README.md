# VCF Rehber Kartları - N8N Workflow & Frontend

Bu proje, VCF (vCard) rehber yedeklerinden kişi bilgilerini çıkarmak ve güzel kartlar halinde görüntülemek için tasarlanmıştır.

## 🚀 Özellikler

- **N8N Workflow**: VCF verilerini işleyen otomatik workflow
- **Modern Frontend**: Responsive ve kullanıcı dostu arayüz
- **Drag & Drop**: VCF dosyalarını kolayca yükleme
- **Akıllı Parsing**: İsim, telefon, email ve diğer bilgileri otomatik tespit
- **Güzel Kartlar**: Her kişi için modern tasarım
- **Çoklu Alan Desteği**: Birden fazla telefon, email desteği

## 📋 Gereksinimler

- N8N kurulumu (self-hosted veya cloud)
- Modern web tarayıcısı
- VCF (vCard) formatında rehber yedeği

## 🛠️ Kurulum

### 1. N8N Workflow Kurulumu

1. N8N instance'ınızda yeni bir workflow oluşturun
2. `n8n-workflow.json` dosyasını import edin
3. Workflow'u aktif hale getirin
4. Webhook URL'ini kopyalayın

### 2. Frontend Kullanımı

1. `index.html` dosyasını herhangi bir web sunucusunda barındırın
2. Tarayıcıda açın
3. N8N webhook URL'ini girin
4. VCF rehber yedeğinizi yükleyin

## 📊 VCF Formatı

VCF dosyanız aşağıdaki formatları destekler:

```vcf
BEGIN:VCARD
VERSION:3.0
FN:Ahmet Yılmaz
TEL:+90 555 123 4567
EMAIL:ahmet@email.com
ORG:ABC Teknoloji
TITLE:Yazılım Geliştirici
ADR:;;İstanbul;İstanbul;34000;Türkiye
NOTE:Senior Developer
BDAY:1985-03-15
URL:https://ahmetyilmaz.com
END:VCARD
```

### Desteklenen Alanlar:

- **FN**: Tam İsim
- **TEL**: Telefon numarası (birden fazla olabilir)
- **EMAIL**: Email adresi (birden fazla olabilir)
- **ORG**: Organizasyon/Şirket
- **TITLE**: Ünvan/Pozisyon
- **ADR**: Adres
- **NOTE**: Not
- **BDAY**: Doğum tarihi
- **URL**: Web sitesi

## 🔧 N8N Workflow Detayları

### Node'lar:

1. **Webhook Node**: POST isteklerini alır
2. **Code Node**: VCF verilerini parse eder ve kişi bilgilerini çıkarır
3. **Respond Node**: Sonuçları JSON formatında döner

### Özellikler:

- Otomatik VCF parsing
- Çoklu telefon ve email desteği
- Tüm standart vCard alanlarını destekler
- Hata yönetimi
- Esnek veri işleme

## 🎨 Frontend Özellikleri

- **Responsive Design**: Mobil ve masaüstü uyumlu
- **Modern UI**: Gradient arka planlar ve gölgeler
- **Drag & Drop**: Dosya yükleme için modern arayüz
- **Real-time Feedback**: Yükleme durumu ve hata mesajları
- **Contact Cards**: Her kişi için detaylı kart tasarımı
- **İkon Desteği**: Her bilgi türü için uygun ikonlar

## 📱 Kullanım

1. **Webhook URL Girin**: N8N'den aldığınız webhook URL'ini girin
2. **VCF Dosyası Seçin**: Rehber yedeğinizi sürükleyin veya tıklayarak seçin
3. **Yükleyin**: "Yükle ve İşle" butonuna tıklayın
4. **Sonuçları Görün**: Kişi kartları otomatik olarak görüntülenir

## 🔒 Güvenlik

- Sadece VCF dosyaları kabul edilir
- Dosya boyutu sınırı yoktur (N8N limitlerine tabi)
- Veriler sadece işlenir, saklanmaz

## 🐛 Sorun Giderme

### Yaygın Hatalar:

1. **"Webhook URL gerekli"**: N8N webhook URL'ini girmeyi unutmayın
2. **"Geçersiz dosya formatı"**: Sadece .vcf ve .vcard dosyaları desteklenir
3. **"HTTP error"**: Webhook URL'inin doğru olduğundan emin olun

### N8N Workflow Kontrolü:

1. Workflow'un aktif olduğundan emin olun
2. Webhook node'unun çalıştığını kontrol edin
3. N8N loglarını inceleyin

## 📈 Geliştirme

### Özelleştirme:

- CSS'de renkleri değiştirin
- Yeni alan türleri ekleyin
- Farklı kart tasarımları oluşturun

### Genişletme:

- Veritabanı entegrasyonu
- Export özellikleri (VCF, CSV, Excel)
- Filtreleme ve arama
- Çoklu dosya desteği
- QR kod oluşturma

## 📄 Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

## 🤝 Katkıda Bulunma

1. Fork yapın
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Commit yapın (`git commit -m 'Add some AmazingFeature'`)
4. Push yapın (`git push origin feature/AmazingFeature`)
5. Pull Request oluşturun

## 📞 Destek

Herhangi bir sorun yaşarsanız:
- GitHub Issues kullanın
- N8N community forumlarını ziyaret edin
- Proje dokümantasyonunu inceleyin

---

**Not**: Bu proje eğitim amaçlıdır ve production kullanımı için ek güvenlik önlemleri alınması önerilir.
