# WhatsApp TXT Analizi Web Sitesi

Bu proje, n8n workflow'unuz ile entegre çalışan basit bir web arayüzü sağlar. Kullanıcılar TXT dosyalarını yükleyebilir ve bunları n8n webhook'unuza gönderebilir.

## Özellikler

- 🎨 Modern ve responsive tasarım
- 📁 Drag & drop dosya yükleme
- 📱 Mobil uyumlu arayüz
- ⚡ Gerçek zamanlı analiz
- 🔒 Sadece .txt dosyaları kabul eder
- 📊 Dosya boyutu ve ad bilgisi gösterimi

## Kurulum

1. `index.html` dosyasını web sunucunuza yükleyin
2. Dosyayı bir web tarayıcısında açın
3. TXT dosyanızı seçin ve "Analiz Et" butonuna tıklayın

## Kullanım

1. **Dosya Seçimi**: TXT dosyanızı sürükleyip bırakın veya tıklayarak seçin
2. **Analiz**: "Analiz Et" butonuna tıklayın
3. **Sonuç**: n8n workflow'unuzdan gelen analiz sonucunu görüntüleyin

## n8n Entegrasyonu

Webhook URL: `https://n8n.8bitiz.com/webhook/whatsapp-analysis`

Gönderilen veri formatı:
```json
{
  "text": "dosya_icerigi",
  "filename": "dosya_adi.txt",
  "timestamp": "2024-01-01T00:00:00.000Z"
}
```

## Teknik Detaylar

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Dosya İşleme**: FileReader API
- **HTTP İstekleri**: Fetch API
- **Responsive Design**: CSS Flexbox ve Grid
- **Animasyonlar**: CSS Transitions ve Keyframes

## Tarayıcı Desteği

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır.

## Destek

Herhangi bir sorun yaşarsanız, lütfen GitHub issues bölümünde bildirin.
