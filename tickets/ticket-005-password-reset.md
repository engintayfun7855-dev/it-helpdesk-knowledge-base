# Ticket 005 - Kullanıcı Şifresini Unuttu

## Kategori

Account / Active Directory Desteği

## Öncelik

Orta

## Problem

Kullanıcı bilgisayarına veya kurumsal hesabına giriş yapamadığını, şifresini unuttuğunu bildirdi.

## Kullanıcıdan Alınan Bilgiler

* Hangi hesaba giriş yapamıyor?
* Hata mesajı nedir?
* Hesap kilitlendi mi?
* Son başarılı giriş zamanı biliniyor mu?
* Kullanıcı kimlik doğrulaması yapıldı mı?

## Kontrol Adımları

1. Kullanıcının kimliği doğrulandı.
2. Hesap adı kontrol edildi.
3. Hesabın kilitli olup olmadığı incelendi.
4. Şifre resetleme işlemi yapıldı.
5. Kullanıcıdan ilk girişte şifre değiştirmesi istendi.
6. Giriş testi yapıldı.
7. Gerekirse hesap kilidi kaldırıldı.

## Kullanılan İşlemler

* Active Directory Users and Computers üzerinden kullanıcı hesabı bulundu.
* Hesap durumu kontrol edildi.
* Password reset işlemi yapıldı.
* “User must change password at next logon” seçeneği aktif edildi.

## PowerShell Örnek Komutları

```powershell
Get-ADUser username -Properties LockedOut
Unlock-ADAccount -Identity username
Set-ADAccountPassword -Identity username -Reset
```

## Tespit

Kullanıcı hesabı kilitlenmişti. Yanlış şifre denemeleri nedeniyle oturum açılamıyordu.

## Çözüm

Kullanıcı kimliği doğrulandıktan sonra hesap kilidi kaldırıldı ve geçici şifre tanımlandı. Kullanıcıdan ilk girişte yeni şifre belirlemesi istendi.

## Sonuç

Kullanıcı hesabına başarıyla giriş yaptı. Ticket kapatıldı.

## Öğrenilen Ders

Şifre resetleme işlemlerinde güvenlik nedeniyle kullanıcı kimliği doğrulanmadan işlem yapılmamalıdır.
