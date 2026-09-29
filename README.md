<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&color=0:FCAF01,50:FE2C6B,100:FC05AC&height=160&section=header&text=Trade&fontSize=60&fontColor=FFFFFF&fontAlignY=42&desc=Spigot%20%2F%20Paper%20%E2%80%A2%201.8%20%E2%86%92%201.21.11&descSize=15&descAlignY=72&animation=fadeIn" alt="Trade" width="100%" />
</p>

<p align="center">
  <a href="https://github.com/coslant/Trade/releases/latest"><img src="https://img.shields.io/github/v/release/coslant/Trade?style=for-the-badge&label=%C4%B0ndir&color=FE2C6B&logo=github" alt="Download" /></a>
  <a href="https://discord.gg/forges"><img src="https://img.shields.io/badge/Discord-Forges%20Studio-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord: Forges Studio" /></a>
</p>

<p align="center">
  <a href="https://github.com/coslant/Trade/actions/workflows/build.yml"><img src="https://img.shields.io/github/actions/workflow/status/coslant/Trade/build.yml?branch=main&style=flat-square&label=build" alt="Build" /></a>
  <img src="https://img.shields.io/badge/Minecraft-1.8%20%E2%86%92%201.21.11-FCAF01?style=flat-square" alt="Minecraft 1.8 - 1.21.11" />
  <img src="https://img.shields.io/badge/Spigot%20%7C%20Paper-FE9808?style=flat-square" alt="Spigot | Paper" />
  <img src="https://img.shields.io/badge/Java-8-FD6C29?style=flat-square&logo=openjdk&logoColor=white" alt="Java 8" />
  <a href="LICENSE"><img src="https://img.shields.io/github/license/coslant/Trade?style=flat-square&color=FB0C9E&label=lisans" alt="License" /></a>
</p>

<p align="center">
  <b>Güvenli oyuncular arası takas (dupe ve scam korumalı).</b>
  <br>
  <sub><kbd>EN</kbd> Safe player-to-player trading with dupe and last-second-swap protection.</sub>
</p>

İki oyuncu karşılıklı bir pencerede eşyalarını koyar, ikisi de onaylayınca takas yapılır.
Dupe ve scam korumalıdır. Tek jar **1.8 – 1.21.11** arası çalışır.

## ✨ Özellikler

- 🤝 Yan yana iki taraflı takas penceresi — karşının koyduğu her şeyi anlık görürsün
- 🔄 **Teklif değişince iki tarafın da onayı sıfırlanır** — son an değiştirme scam'ini engeller
- ⏳ Onay sonrası kısa bir **kilit süresi**; bu sırada teklif değiştirilemez
- 📦 **Hiçbir eşya kaybolmaz** — karşı taraf çıkarsa eşyalar teslim kuyruğuna yazılır ve bir dahaki girişinde verilir
- 💀 Takas sırasında ölüm, çıkış veya sunucu kapanması: takas iptal olur, herkes kendi eşyasını geri alır
- 🚫 Belirli eşyalar takasa kapatılabilir (`blacklist`)
- 📏 İsteğe bağlı mesafe sınırı
- 📝 Tamamlanan takaslar konsola yazılır

## 🛡️ Güvenlik

| Risk | Önlem |
| :-- | :-- |
| Son an eşya değiştirme | Teklif değişince iki onay da sıfırlanır + kilit süresi |
| Karşı taraf çıkınca eşya kaybı | Teslim kuyruğu (`pending.yml`), girişte otomatik verilir |
| Takas sırasında ölüm | Takas iptal, herkes kendi eşyasını alır |
| Sunucu çökmesi / kapanması | Açık takaslar kapanışta iptal edilir |
| Sürükle-bırak ile kopyalama | Pencerede tüm sürükleme ve kaydırma işlemleri kapalı |

## 📥 Kurulum

1. [Releases](https://github.com/coslant/Trade/releases/latest) sayfasından `Trade.jar` dosyasını indir.
2. Sunucunun `plugins/` klasörüne at.
3. Sunucuyu yeniden başlat.
4. `plugins/Trade/config.yml` dosyasından süreleri ve mesajları düzenle.

## 🎮 Komutlar

| Komut | Açıklama | Yetki |
|-------|----------|-------|
| `/trade <oyuncu>` | Takas isteği gönderir | `trade.use` |
| `/trade kabul` | Gelen isteği kabul eder | `trade.use` |
| `/trade ret` | Gelen isteği reddeder | `trade.use` |
| `/trade iptal` | İsteği ya da açık takası iptal eder | `trade.use` |

**Alias:** `/takas`

## 🔑 Yetkiler

| Yetki | Açıklama | Varsayılan |
|-------|----------|------------|
| `trade.use` | Takas yapabilir | herkes |

## ⚙️ Ayarlar (config.yml)

| Anahtar | Açıklama |
|---------|----------|
| `request-timeout` | İstek kaç saniye sonra düşer |
| `max-distance` | Takas için en fazla uzaklık (0 = sınırsız) |
| `confirm-delay-ticks` | Onay sonrası kilit süresi (20 tick = 1 sn) |
| `blacklist` | Takas edilemeyecek eşyalar |
| `log-trades` | Takasları konsola yaz |
| `gui.title` / `gui.filler` | Pencere başlığı ve dolgu bloğu |
| `messages.*` | Tüm mesajlar ve GUI düğme yazıları |

## 🛠️ Derleme

```bash
mvn clean package
```

Çıktı: `target/Trade.jar`

> 1.8 uyumluluğu için Java 8 hedefiyle derlenir. En sorunsuz derleme **JDK 8, 11 veya 17** iledir.

Her push'ta [GitHub Actions](https://github.com/coslant/Trade/actions/workflows/build.yml) projeyi otomatik derler; etiketlenen sürümler (`v*`) jar'ıyla birlikte [Releases](https://github.com/coslant/Trade/releases) sayfasında yayınlanır.

## 💬 Destek

- 🐛 Hata bildirimi ve öneriler için [Issues](https://github.com/coslant/Trade/issues) sekmesini kullan.
- 💬 Sorular ve destek için [Forges Studio Discord](https://discord.gg/forges) sunucusuna katıl.

## 📄 Lisans

[MIT](LICENSE) — dilediğin gibi kullan, değiştir, dağıt.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:FCAF01,50:FE2C6B,100:FC05AC&height=4&section=footer" width="100%" alt="" />
  <br>
  <sub>🔥 <a href="https://github.com/coslant">coslant</a> tarafından geliştirildi · <a href="https://discord.gg/forges">Forges Studio</a></sub>
</p>
