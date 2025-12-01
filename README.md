# CRM & İş Yönetim Sistemi

Bu proje, Smarthr Bootstrap Admin Panel Template'ini Laravel framework'üne dönüştürülmüş kapsamlı bir CRM & İş Yönetim Sistemidir.

## Özellikler

### 1. Müşteri Yönetimi (CRM)
- ✅ Bireysel Müşteri Bilgileri (Ad-Soyad, Telefon, E-posta, İl/İlçe, Adres, T.C. Kimlik No, Not Alanı)
- ✅ Kurumsal Müşteri Bilgileri (Firma Adı, Yetkili Ad-Soyad, Telefon, E-posta, İl/İlçe, Vergi Dairesi, Vergi No, Adres, Not Alanı)
- ✅ Müşteri geçmişi görüntüleme
- ✅ Diğer modüllerle otomatik entegrasyon
- ✅ Hatırlatıcı oluşturma
- ✅ Müşteriye özel dosya yükleme alanı
- ✅ Müşteriye abonelik ekleme
- ✅ Müşteriye araç takip bakım onarımları ekleme
- ✅ Raporlar

### 2. Mail & SMS Yönetimi
- 🔄 Şablonlar (Hazır mail ve SMS şablonları)
- 🔄 Mail Gönderimi (Tekli/Toplu, Dosya ekleme, Zamanlama, Log kayıtları)
- 🔄 SMS Gönderimi (Tekli/Toplu, Otomatik hatırlatma, Gönderim raporları)
- 🔄 Hatırlatıcılar

### 3. Dosya & Evrak Yönetimi
- 🔄 Dosya Ekle (Müşteri veya proje bazlı)
- 🔄 Evrak listesi ve kategorilere ayırma
- 🔄 Evrak versiyon takibi

### 4. Kargo Yönetimi
- 🔄 Kargo Ekle (Kargo firması seçimi, Gönderi bilgileri, Müşteri bağlantısı)
- 🔄 Kargo Takip (Takip numarası ile anlık durum, Kargo geçmişi)
- 🔄 Kargo İade (İade süreç takibi, İade nedeni ve raporlaması)

### 5. Şube Yönetimi
- 🔄 Şube Ekle
- 🔄 Şubeler listesi

### 6. Stok & Depo Yönetimi
- 🔄 Stok Ekle (Ürün adı, Barkod, Kategori, Alış/Satış fiyatı, Minimum stok limiti)
- 🔄 Stoklar listesi ve hareketleri
- 🔄 Depo Ekle ve Yönetimi
- 🔄 Depolar arası transfer

### 7. Fatura Yönetimi
- ✅ Fatura Ekle (Müşteri seçimi, Ürün/hizmet ekleme, KDV hesaplama, Fatura PDF çıktısı)
- ✅ Fatura listesi
- ✅ Ödenen/Ödenmeyen takip

### 8. Abonelik Yönetimi
- ✅ Abonelik Ekle (Paket seçimi, Başlangıç/Bitiş tarihleri, Otomatik ödeme takibi)
- ✅ Abonelikler listesi (Aktif/Pasif)
- ✅ Hatırlatıcılar

### 9. Paket Yönetimi
- ✅ Paket Ekle (Paket adı, Fiyat, Süre, Açıklama)
- ✅ Paket Kategorileri

### 10. Teklif Yönetimi
- ✅ Teklif Oluştur (Müşteri seçimi, Ürün/hizmet ekleme, Teklif PDF oluşturma)
- ✅ Teklifler listesi (Durum takibi: beklemede, onaylandı, reddedildi)
- ✅ Teklif geçmişi

### 11. Proje Yönetimi
- ✅ Proje Ekle (Proje adı, Açıklama, Başlangıç-Bitiş tarihleri, Sorumlu ekip üyeleri)
- ✅ Proje Kategorileri

### 12. Cari Yönetimi
- 🔄 Gelir Ekle
- 🔄 Gider Ekle
- 🔄 Raporlar (Aylık gelir-gider, Kâr-zarar, Bakiye durumu)

### 13. Ödeme Kanalları
- 🔄 Ödeme Kanalı Ekle
- 🔄 Ödeme Kanalları listesi
- 🔄 Komisyon oranı takibi

### 14. Araç Yönetimi
- 🔄 Araç Ekle
- 🔄 Araçlar listesi

### 15. Araç Bakım Yönetimi
- 🔄 Bakım Ekle
- 🔄 Bakımlar listesi
- 🔄 Randevular

### 16. Servis & Yedek Parça
- 🔄 Servis Ekle
- 🔄 Servis Planı
- 🔄 Yedek Parça Ekle
- 🔄 Yedek Parçalar listesi
- 🔄 Stok Takibi

### 17. Yapılacaklar & Notlar
- 🔄 Etkinlik Ekle
- 🔄 Etkinlikler listesi
- 🔄 Not Ekle
- 🔄 Notlar listesi

### 18. Ekip Yönetimi
- 🔄 Ekip Üyeleri listesi
- 🔄 Yeni Üye Oluştur
- 🔄 Yetkilendirme

### 19. Google Takvim Entegrasyonu
- 🔄 Google Takvim entegrasyonu
- 🔄 Otomatik senkronizasyon
- 🔄 Randevuların takvimde görünmesi

## Kurulum

1. Projeyi klonlayın:
```bash
cd crm-system
```

2. Bağımlılıkları yükleyin:
```bash
composer install
```

3. `.env` dosyasını oluşturun ve veritabanı ayarlarını yapın:
```bash
cp .env.example .env
php artisan key:generate
```

4. Veritabanı migration'larını çalıştırın:
```bash
php artisan migrate
```

5. Geliştirme sunucusunu başlatın:
```bash
php artisan serve
```

## Proje Yapısı

### Migration Dosyaları
- `customers` - Müşteri bilgileri (Bireysel ve Kurumsal)
- `invoices` - Fatura bilgileri
- `invoice_items` - Fatura kalemleri
- `quotes` - Teklif bilgileri
- `quote_items` - Teklif kalemleri
- `projects` - Proje bilgileri
- `packages` - Paket bilgileri
- `subscriptions` - Abonelik bilgileri
- `shipments` - Kargo bilgileri
- Ve diğerleri...

### Model Dosyaları
- `Customer` - Müşteri modeli
- `Invoice` - Fatura modeli
- `InvoiceItem` - Fatura kalemi modeli
- `Quote` - Teklif modeli
- `QuoteItem` - Teklif kalemi modeli
- `Project` - Proje modeli
- Ve diğerleri...

### Controller Dosyaları
- `DashboardController` - Dashboard işlemleri
- `CustomerController` - Müşteri işlemleri
- `InvoiceController` - Fatura işlemleri
- `ProjectController` - Proje işlemleri
- Ve diğerleri...

### View Dosyaları
- `layouts/app.blade.php` - Ana layout
- `layouts/sidebar.blade.php` - Sidebar menü
- `layouts/topbar.blade.php` - Üst bar
- `layouts/footer.blade.php` - Footer
- `dashboard/index.blade.php` - Dashboard sayfası
- Ve diğerleri...

### Template Entegrasyonu
- Smarthr template'inin `partials` klasörü Laravel'de `resources/views/layouts` altında Blade include'larına dönüştürüldü (`app`, `sidebar`, `topbar`, `footer`, `partials/head.blade.php`, `partials/scripts.blade.php`).
- Yeni bir sayfa oluştururken `@extends('layouts.app')` kullanın ve gerekirse `@section('page-header')`, `@section('content')`, `@push('styles')`, `@push('vendor-scripts')` bloklarıyla template bileşenlerini genişletin.
- Modül bazlı view dosyalarını `resources/views/{modul}` klasörlerinde tutun (ör: `customers/index.blade.php`, `invoices/index.blade.php`, `projects/index.blade.php`).
- Template'ten gelen tüm CSS/JS dosyaları `public/assets` altına kopyalandığı için `asset('assets/...')` ile doğrudan kullanılabilir.
- Sidebar menüsü Laravel rotalarına bağlandı; yeni modüller için ilgili rotayı tanımladıktan sonra `layouts/sidebar.blade.php` içinde menü kaydını ekleyin.

## Devam Eden İşler

✅ Tamamlandı:
- Laravel projesi yapısı
- Temel migration dosyaları
- Temel model dosyaları
- Temel controller dosyaları
- Temel view dosyaları
- Asset dosyalarının entegrasyonu
- Dashboard yapısı

🔄 Devam Ediyor:
- Tüm modüllerin controller ve view dosyalarının tamamlanması
- Mail & SMS entegrasyonu
- Google Takvim entegrasyonu
- Yetkilendirme sistemi
- Raporlar

## Notlar

- Proje Laravel 12 ile geliştirilmiştir
- Template asset dosyaları `public/assets` klasöründe bulunmaktadır
- Template'e bağımlı olmayan bir yapı kurulmuştur
- Tüm modüller MVC yapısına uygun şekilde organize edilmiştir

## Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Commit edin (`git commit -m 'Add some amazing feature'`)
4. Push edin (`git push origin feature/amazing-feature`)
5. Pull Request oluşturun

## Lisans

Bu proje özel bir projedir.