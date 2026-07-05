# Kurulum ve Kullanım Rehberi (Türkçe)

Bu rehber, Obsidian Geliştirici Çalışma Alanı şablonunu bilgisayarınıza nasıl kuracağınızı ve günlük iş akışınıza nasıl entegre edeceğinizi ayrıntılı olarak açıklamaktadır.

---

## Neler Var?

Kasa (vault) klasörü içerisinde aşağıdaki klasör yapılandırması hazır gelir:

| Klasör | Amaç |
|--------|------|
| `00_Dashboard/` | Görev takvimi görünümüyle ana pano |
| `01_Daily/` | Günlük notlar (şablondan otomatik oluşturulur) |
| `02_Projects/` | Proje notları + Kanban tabloları |
| `03_Knowledge/` | Konu ağaçlarıyla yapılandırılmış bilgi tabanı |
| `04_Snippets/` | Açıklamalı kod parçacıkları deposu |
| `05_Resources/` | Referanslar, PDF'ler ve varlıklar |
| `_Templates/` | Tüm not şablonları (Templater tabanlı) |
| `tasksCalendar/` | Özel DataviewJS takvim görünümü bileşeni |

---

## Gerekli Eklentiler

Vault'un tüm bileşenleriyle çalışması için Obsidian içerisinden **Settings -> Community Plugins -> Browse** adımlarını izleyerek aşağıdaki eklentileri yükleyin:

| Eklenti | Amaç | Zorunlu mu? |
|---------|------|---------|
| **Templater** | Dosya oluşturulurken otomatik şablon uygulama | Evet |
| **Tasks** | `#task` etiketi ile gelişmiş görev takibi | Evet |
| **Dataview** | Dashboard takvimi için DataviewJS desteği | Evet |
| **QuickAdd** | `Ctrl+X` ile hızlı görev yakalama | Evet |
| **Kanban** | Kanban proje iş tahtaları | Evet |
| **Calendar** | Günlük not takvim paneli (yan bar) | Evet |
| **Obsidian Git** | Notları otomatik Git ile yedekleme | Önerilen |
| **Omnisearch** | Vault genelinde tam metin arama | Önerilen |

> **Önemli Not:** Tüm eklentilerin gelişmiş ayarları ve kısayolları bu kasada önceden yapılandırılmıştır. Eklentileri sadece kurup etkinleştirmeniz yeterlidir.

---

## Kurulum Adımları

1. **Kasayı İndirin:**
   GitHub üzerinden bu depoyu ZIP olarak indirin veya klonlayın.

2. **Obsidian'da Açın:**
   Obsidian uygulamasını açın ve **Open folder as vault** seçeneğine tıklayarak indirdiğiniz klasörün içindeki `Vault-TR/` klasörünü seçin.

3. **Eklentileri Etkinleştirin:**
   Obsidian güven soracaktır. **Trust and Enable Plugins** seçeneğine tıklayın.
   **Settings -> Community Plugins** menüsüne giderek **Restricted Mode**'u kapatın ve yukarıdaki eklentileri yükleyip aktif edin.

4. **Temayı Uygulayın:**
   **Settings -> Appearance -> Themes** menüsünden **Things** temasını arayıp yükleyin. (Açık ve koyu modlarla tam uyumludur).

5. **Kullanmaya Başlayın:**
   Ana sayfa olarak `00_Dashboard/main.md` dosyasını açın. Takviminiz otomatik olarak yüklenecektir.

---

## Günlük Çalışma Akışı

### Görev Ekleme
* Herhangi bir notun içindeyken **Ctrl+X** kısayoluna basın. Açılan kutuya görev adını yazın, Enter'a basın ve takvimden bir bitiş tarihi seçin.
* Sistem satıra otomatik olarak şu formatı ekler: `- [ ] #task göreviniz [due:: YYYY-MM-DD]`
* *Not:* Kanban tablolarında `Ctrl+X` çalışmaz. Kanban kartlarında görev eklemek için doğrudan **+** butonunu, tarih eklemek için ise kartın içine `@{YYYY-MM-DD}` yazımını kullanın.

### Yeni Bilgi Notu Oluşturma
1. `03_Knowledge/<ilgili-alan>/` klasörüne gidin.
2. Yeni bir not oluşturun (şablon otomatik uygulanacaktır).
3. Notun özellikler (properties) kısmındaki `tags` alanına `alan/alt-konu/detay` (Örn: `ml/supervised/xgboost`) formatında hiyerarşik etiket ekleyin.
4. `parent:` alanına üst konunun Obsidian bağlantısını (`[[Konu]]`) yerleştirin.

### Yeni Proje Başlatma
1. `02_Projects/<proje-adi>/` klasörünü oluşturun.
2. İçerisine `<proje-adi>.md` dosyası oluşturun (şablon otomatik yüklenir).
3. Projeyi Kanban tahtasıyla takip etmek isterseniz, `_Templates/TPL_Kanban-Project` şablonunu kullanarak `<proje-adi>-Kanban.md` dosyası oluşturun.

---

## Git Yedekleme Yapılandırması (İsteğe Bağlı)

Kasanızı kendi özel GitHub deponuza `Obsidian Git` eklentisiyle yedeklemek isterseniz:
1. Terminalde kasa klasörünüzün içine (`Vault-TR/`) gidin ve Git'i ilklendirin:
   ```bash
   git init
   git remote add origin <kendi-ozel-repo-urlniz>
   git add .
   git commit -m "kasa kurulumu"
   git push -u origin main
   ```
2. Obsidian içerisinden **Settings -> Community Plugins** menüsüne gidip **Obsidian Git** eklentisini aktifleştirin. Notlarınız arka planda otomatik yedeklenmeye başlayacaktır.

---

## Katkıda Bulunanlar / Credits

- Panodaki (Dashboard) özel aylık görev takvimi (`tasksCalendar/`), 702573N tarafından geliştirilen [Obsidian-Tasks-Calendar](https://github.com/702573N/Obsidian-Tasks-Calendar) projesinden uyarlanmıştır. Bu harika görselleştirme aracını açık kaynak olarak paylaştığı için kendisine teşekkür ederiz.