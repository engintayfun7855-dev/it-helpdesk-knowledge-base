# Ticket 004 - Bilgisayar Yavaş Çalışıyor

## Kategori

Windows / Performans Desteği

## Öncelik

Düşük-Orta

## Problem

Kullanıcı bilgisayarının yavaş açıldığını, programların geç tepki verdiğini ve genel performansın düşük olduğunu bildirdi.

## Kullanıcıdan Alınan Bilgiler

* Sorun ne zamandır var?
* Hangi programlarda yavaşlık yaşanıyor?
* Bilgisayar açılışta mı, kullanım sırasında mı yavaşlıyor?
* Son dönemde yeni program kuruldu mu?
* Disk doluluk oranı yüksek mi?

## Kontrol Adımları

1. Görev Yöneticisi üzerinden CPU, RAM ve disk kullanımı kontrol edildi.
2. Başlangıçta çalışan uygulamalar incelendi.
3. Disk doluluk oranı kontrol edildi.
4. Gereksiz geçici dosyalar temizlendi.
5. Windows Update durumu kontrol edildi.
6. Antivirüs taraması önerildi.
7. Donanım yükseltme ihtiyacı değerlendirildi.

## Kullanılan Komutlar

```cmd
taskmgr
cleanmgr
msconfig
```

```powershell
Get-Process | Sort-Object CPU -Descending | Select-Object -First 10
Get-PSDrive C
```

## Tespit

C diski yüksek oranda doluydu ve başlangıçta gereksiz uygulamalar çalışıyordu. RAM kullanımı da normalden yüksekti.

## Çözüm

Geçici dosyalar temizlendi. Gereksiz başlangıç uygulamaları devre dışı bırakıldı. Kullanıcıya disk alanı yönetimi konusunda bilgi verildi. Sistem yeniden başlatılıp performans tekrar kontrol edildi.

## Sonuç

Bilgisayarın açılış süresi ve genel tepkisi iyileşti. Ticket kapatıldı.

## Öğrenilen Ders

Performans sorunlarında CPU, RAM, disk kullanımı ve başlangıç uygulamaları birlikte değerlendirilmelidir.
