# Ticket 002 - Yazıcıdan Çıktı Alınamıyor

## Kategori

Printer / Donanım Desteği

## Öncelik

Orta

## Problem

Kullanıcı yazıcıya belge gönderdiğini ancak çıktı alamadığını bildirdi.

## Kullanıcıdan Alınan Bilgiler

* Hangi yazıcıyı kullanıyor?
* Sorun sadece kendi bilgisayarında mı var?
* Diğer kullanıcılar çıktı alabiliyor mu?
* Yazıcıda hata ışığı veya ekran mesajı var mı?
* Belge yazdırma kuyruğunda bekliyor mu?

## Kontrol Adımları

1. Yazıcının açık ve ağa bağlı olduğu kontrol edildi.
2. Kağıt ve toner durumu kontrol edildi.
3. Yazıcı kuyruğu incelendi.
4. Yazıcı varsayılan yazıcı olarak ayarlandı.
5. Print Spooler servisi kontrol edildi.
6. Yazıcı sürücüsü kontrol edildi.
7. Test sayfası gönderildi.

## Kullanılan Komutlar

```powershell
Get-Service -Name Spooler
Restart-Service -Name Spooler
Get-Printer
```

## Tespit

Yazdırma kuyruğunda eski belgeler takılı kalmıştı. Print Spooler servisi çalışıyordu fakat kuyruk temizlenmeden yeni belgeler yazdırılamıyordu.

## Çözüm

Yazdırma kuyruğu temizlendi. Print Spooler servisi yeniden başlatıldı. Test sayfası gönderildi ve çıktı başarıyla alındı.

## Sonuç

Kullanıcı tekrar çıktı alabildi. Ticket kapatıldı.

## Öğrenilen Ders

Yazıcı sorunlarında önce fiziksel durum, sonra yazdırma kuyruğu, ardından servis ve sürücü kontrol edilmelidir.
