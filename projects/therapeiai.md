# TherapeiAİ — teknik vitrin

**Çınar Özgürgil · Kişisel proje · Kapalı kaynak · 22 Kasım 2026**

Düşünceleri toparlama ve kendini ifade etme üzerine geliştirdiğim yazılım projesi. Bu sayfa projenin teknik gelişimini gösterir. Kaynak kodunun tamamını, özel kullanıcı verisini veya tüm ürün planını paylaşmaz.

## Mevcut durum

| Bölüm | Kaynakta görülen durum |
| --- | --- |
| Açılış ve başlangıç akışı | Next.js/React arayüz prototipi |
| Sohbet ve kota ekranları | Örnek arayüz davranışı; çalışan AI servisi değil |
| Mesaj saklama | React belleğinde; yenilemede kaybolur |
| Veri katmanı | MySQL bağlantı havuzu, şema/migration taslağı; canlı bağlantı doğrulanmadı |
| Model / fine-tuning | Ürüne bağlanmış model veya yayımlanmış eğitim ölçümü yok |
| Hesap, ödeme, psikolojik test | Üretimde çalışan özellik olarak sunulmuyor |

## Benim katkım

TherapeiAİ adını belirledim; fikir, kullanıcı akışı ve geliştirme sürecini yürütüyorum. Açılış, başlangıç tercihleri ve sohbet deneyimi üzerinde çalışıyorum. Teknik hedefim arayüzü, veri akışını ve LLM entegrasyonunu anlaşılır ve test edilebilir bir bütün hâline getirmek.

## Teknik kararlar

- Arayüz: Next.js, React, TypeScript.
- Veri: MySQL için bağlantı havuzu ve şema hazırlığı var. Mevcut demo kalıcı kayıt yaptığını iddia etmiyor.
- Marka görselleri tasarım çalışmasıdır; tek başına çalışan özellik kanıtı değildir.
- Ürün kodu özel kalır; incelenebilir yöntem ve sonuçlar ayrı deney deposunda paylaşılır.

## Model seçimi ve deney

[SmolLM3 Fine-tuning Lab](https://github.com/HunterLion2/smollm3-finetuning-lab) içinde **HuggingFaceTB/SmolLM3-3B + PEFT/LoRA** ile bağımsız bir deney hazırladım. BANKING77 ile yapılan görev niyet sınıflandırmasıdır. TherapeiAİ için ruh sağlığı eğitimi, Türkçe kalite kanıtı veya klinik doğrulama değildir.

Deneyde eğitim/test ayrımı, sabit seed, veri/model sürümleri, eğitim ayarları ve temel model/adaptör karşılaştırması görünür olacak. Ayrı test örnekleri üzerinde aynı üretim ayarları kullanılacak; doğruluk, geçersiz çıktı oranı, hata örnekleri ve olumsuz sonuçlar da raporlanacak.

## Sonuçlar: ne tamamlandı, ne tamamlanmadı?

Arayüz prototipi ve veri katmanı hazırlığı mevcut. Önceki geliştirme kayıtlarında derleme ve kod kontrolleri bulunuyor; bunlar AI kalitesi veya klinik geçerlilik testi değildir.

**Yeni deneyin eğitimi henüz çalıştırılmadı; doğruluk artışı, eğitilmiş adaptör veya önce/sonra model çıktısı yayımlanmış değil.** Ölçüm elde edildiğinde sonuç raporuna gerçek değerler eklenecek. Sonuç iyileşmezse bu da açıkça yazılacak.

## Kalan işler

1. Deney eğitimini çalıştırıp eğitimden ayrı değerlendirmeyi tamamlamak.
2. Türkçe kullanım için ayrı veri, kalite ve güvenlik değerlendirmesi tasarlamak.
3. Model API entegrasyonunu ve kalıcı kayıtları uygulayıp doğrulamak.
4. Tamamlanan akışın kısa demosunu ve sınırlarını paylaşmak.

Bu prototip klinik olarak doğrulanmış bir hizmet değildir; terapi/teşhis veya etkili tedavi iddiası taşımaz.

[Profilime dön](../README.md) · [Deney deposunu incele](https://github.com/HunterLion2/smollm3-finetuning-lab)
