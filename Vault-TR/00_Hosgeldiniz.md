---
type: welcome
tags:
  - welcome
  - start
created: 2026-07-03
modified: 2026-07-03
---

# Obsidian Gelistirici Calisma Alanina Hos Geldiniz

Bu calisma alani, yazilim gelistiriciler icin ozel olarak tasarlanmis kisisel bir bilgi ve proje yonetim sablonudur. Notlarinizi organize etmek, projelerinizi takip etmek ve kod parcaciklarinizi saklamak icin her sey onceden yapilandirilmistir.

---

## Klasor Yapisi

Sol paneldeki klasor yapisi su sekildedir:
* **00_Dashboard/**: Gorev takviminizi ve gunluk ilerlemenizi gosteren ana panel.
* **01_Daily/**: Gunluk notlariniz. Takvimden veya kisayoldan otomatik olusturulur.
* **02_Projects/**: Aktif projeleriniz ve Kanban is tahtalariniz.
* **03_Knowledge/**: Ogrenilen teknolojiler ve kavramlarin hiyerarsik agaci.
* **04_Snippets/**: Aciklamali kod parcaciklari deposu.
* **05_Resources/**: Makaleler, kitaplar, PDF'ler ve diger varliklar.

---

## Temel Kullanim Ipuclari

1. **Hizli Gorev Ekleme (Ctrl+X):**
   * Herhangi bir notun icindeyken Ctrl+X tuslarina basin. Acilan kutuya gorev tanimini yazip Enter'a basin, ardindan takvimden tarihi secin.
   * Goreviniz otomatik olarak #task etiketi ve bitis tarihiyle satira eklenecektir.

2. **Otomatik Tarih Guncelleme:**
   * Notlarinizdaki modified (guncellenme tarihi) alani, siz dosyayi duzenledikçe arka planda otomatik olarak guncel tarihe (YYYY-MM-DD) cekilir.

3. **Gelistirici Etiket Vurgulamalari:**
   * #task ve #bug etiketleri, Obsidian editorunde otomatik olarak orman yesili ve koyu kirmizi kapsuller seklinde renkli gorunur.

---

## Eklentileri Yapilandirma
* **Git Yedekleme:** obsidian-git eklentisi varsayilan olarak kapali gelmektedir. Notlarinizi GitHub'a yedeklemek isterseniz, Ayarlar -> Topluluk Eklentileri menusunden aktif edip kendi reposunuza baglayabilirsiniz. Detayli yonergeler projenin ana GitHub README'sinde yer almaktadýr.
