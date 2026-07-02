# Ticket 003 - Outlook Açılmıyor veya Mail Senkronize Olmuyor

## Kategori

Microsoft Office / Mail Desteği

## Öncelik

Orta

## Problem

Kullanıcı Outlook uygulamasının açılmadığını veya yeni e-postaların gelmediğini bildirdi.

## Kullanıcıdan Alınan Bilgiler

* Outlook tamamen açılmıyor mu, yoksa mail mi gelmiyor?
* Web üzerinden e-postaya erişebiliyor mu?
* İnternet bağlantısı var mı?
* Hata mesajı alıyor mu?
* Sorun ne zaman başladı?

## Kontrol Adımları

1. İnternet bağlantısı kontrol edildi.
2. Kullanıcının webmail erişimi test edildi.
3. Outlook güvenli modda açılmaya çalışıldı.
4. Outlook profil durumu kontrol edildi.
5. Mail hesabı ayarları kontrol edildi.
6. Outlook veri dosyası ve senkronizasyon durumu incelendi.
7. Gerekirse yeni Outlook profili oluşturuldu.

## Kullanılan Komutlar

```cmd
outlook.exe /safe
```

## Tespit

Outlook güvenli modda açıldı. Sorunun bir eklenti kaynaklı olabileceği değerlendirildi.

## Çözüm

Outlook eklentileri devre dışı bırakıldı. Uygulama normal şekilde tekrar açıldı. Mail gönderme ve alma testi yapıldı.

## Sonuç

Kullanıcı Outlook üzerinden tekrar mail gönderip alabildi. Ticket kapatıldı.

## Öğrenilen Ders

Outlook sorunlarında önce webmail erişimi test edilmeli, ardından uygulama tarafı incelenmelidir. Güvenli mod, eklenti kaynaklı sorunları ayırmak için hızlı bir yöntemdir.
