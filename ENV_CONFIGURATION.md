# Mail ve SMS Entegrasyonu - .env Yapılandırması

Bu dosya, müşteri panelinde mail ve SMS gönderimi için gerekli .env ayarlarını içerir.

## Mail Ayarları

Aşağıdaki ayarları `.env` dosyanıza ekleyin:

```env
# Mail Ayarları
MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-app-password
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=your-email@gmail.com
MAIL_FROM_NAME="${APP_NAME}"
```

### Mail Ayarları Açıklamaları:

- **MAIL_MAILER**: Mail gönderim yöntemi (smtp, sendmail, mailgun, ses, postmark, resend, log, array, failover, roundrobin)
- **MAIL_HOST**: SMTP sunucu adresi (Gmail için: smtp.gmail.com)
- **MAIL_PORT**: SMTP port numarası (587 TLS, 465 SSL)
- **MAIL_USERNAME**: SMTP kullanıcı adı (genellikle e-posta adresiniz)
- **MAIL_PASSWORD**: SMTP şifresi (Gmail için App Password kullanın)
- **MAIL_ENCRYPTION**: Şifreleme türü (tls veya ssl)
- **MAIL_FROM_ADDRESS**: Gönderen e-posta adresi
- **MAIL_FROM_NAME**: Gönderen adı (varsayılan: APP_NAME)

## SMS Ayarları

Aşağıdaki ayarları `.env` dosyanıza ekleyin. Birden fazla SMS sağlayıcısı kullanabilirsiniz, sistem otomatik olarak yapılandırılmış olanı seçer.

### NetGSM (Türkiye için önerilen)

```env
# NetGSM Ayarları
NETGSM_USERNAME=your-netgsm-username
NETGSM_PASSWORD=your-netgsm-password
NETGSM_SENDER_ID=PANELCRM
```

### Nexmo/Vonage

```env
# Nexmo/Vonage Ayarları
NEXMO_KEY=your-nexmo-api-key
NEXMO_SECRET=your-nexmo-api-secret
NEXMO_FROM=PANELCRM
```

### Twilio

```env
# Twilio Ayarları
TWILIO_SID=your-twilio-account-sid
TWILIO_TOKEN=your-twilio-auth-token
TWILIO_FROM=+1234567890
```

### Turkcell

```env
# Turkcell Ayarları
TURKCELL_API_KEY=your-turkcell-api-key
TURKCELL_API_SECRET=your-turkcell-api-secret
TURKCELL_SENDER_ID=PANELCRM
TURKCELL_API_URL=https://api.turkcell.com
```

### SMS Provider Seçimi

```env
# Aktif SMS sağlayıcısını belirle (opsiyonel)
# Boş bırakılırsa, yapılandırılmış ilk sağlayıcı kullanılır
SMS_PROVIDER=netgsm
```

## SMS Ayarları Açıklamaları:

- **NETGSM_USERNAME**: NetGSM kullanıcı adı
- **NETGSM_PASSWORD**: NetGSM şifresi
- **NETGSM_SENDER_ID**: NetGSM gönderen başlığı (onaylı başlık)
- **NEXMO_KEY**: Nexmo API anahtarı
- **NEXMO_SECRET**: Nexmo API secret
- **NEXMO_FROM**: Nexmo gönderen adı
- **TWILIO_SID**: Twilio Account SID
- **TWILIO_TOKEN**: Twilio Auth Token
- **TWILIO_FROM**: Twilio telefon numarası (+ ile başlamalı)
- **TURKCELL_API_KEY**: Turkcell API anahtarı
- **TURKCELL_API_SECRET**: Turkcell API secret
- **TURKCELL_SENDER_ID**: Turkcell gönderen başlığı
- **TURKCELL_API_URL**: Turkcell API URL'i (varsayılan: https://api.turkcell.com)
- **SMS_PROVIDER**: Tercih edilen SMS sağlayıcısı (netgsm, nexmo, twilio, turkcell)

## Örnek .env Yapılandırması

```env
# Mail Ayarları
MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587
MAIL_USERNAME=info@example.com
MAIL_PASSWORD=your-app-password-here
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=info@example.com
MAIL_FROM_NAME="CRM Panel"

# SMS Ayarları - NetGSM (Türkiye için önerilen)
NETGSM_USERNAME=your-username
NETGSM_PASSWORD=your-password
NETGSM_SENDER_ID=PANELCRM
SMS_PROVIDER=netgsm
```

## Notlar

1. **Gmail Kullanımı**: Gmail için 2FA aktif olmalı ve App Password kullanılmalıdır.
2. **NetGSM**: Türkiye'de en yaygın kullanılan SMS sağlayıcısıdır. Başlık (sender_id) onaylanmış olmalıdır.
3. **SMS Sağlayıcı Önceliği**: Sistem şu sırayla kontrol eder: netgsm → nexmo → twilio → turkcell
4. **Güvenlik**: .env dosyasını asla versiyon kontrolüne eklemeyin. Hassas bilgiler içerir.

