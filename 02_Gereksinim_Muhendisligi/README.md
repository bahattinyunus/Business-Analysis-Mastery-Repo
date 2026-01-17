# 📐 Modül 02: Gereksinim Mühendisliği (Requirements Engineering)

> **"Müşterinin ne istediğini değil, neye ihtiyacı olduğunu bulmak; işte mühendislik budur."**

## 🎯 Modül Hedefleri

Gereksinim Mühendisliği, iş analizinin kalbidir. Bu modül, soyut fikirleri ve dağınık istekleri, yazılım ekipleri tarafından inşa edilebilecek somut, net ve test edilebilir teknik özelliklere dönüştürme sürecini kapsar. Burada, bir dedektif gibi iz sürmeyi, bir diplomat gibi müzakere etmeyi ve bir avukat gibi hassas dokümantasyon yapmayı öğreneceksiniz.

## 📚 İçerik Başlıkları ve Derinlemesine Bakış

### 1. Gereksinim Piramidi (Types of Requirements)
Gereksinimler tek bir türden oluşmaz; hiyerarşik bir yapıları vardır. Bu hiyerarşiyi anlamak, kargaşayı önler.
*   **İş Gereksinimleri (Business Requirements):** Şirketin **neden** bu projeyi yaptığı. (Örn: "Pazar payını %10 artırmak", "Maliyetleri %15 düşürmek").
*   **Paydaş Gereksinimleri (Stakeholder Requirements):** Kullanıcıların işlerini yapmak için **neye** ihtiyaç duydukları. (Örn: "Muhasebeci olarak faturaları toplu onaylayabilmeliyim").
*   **Çözüm Gereksinimleri (Solution Requirements):** Sistemin **nasıl** davranacağı. İkiye ayrılır:
    *   **Fonksiyonel (Functional):** Sistem ne yapacak? (Örn: "Sistem, kullanıcıya PDF çıktısı vermelidir").
    *   **Fonksiyonel Olmayan (Non-Functional / QoS):** Sistem nasıl olmalı? (Örn: "Sayfa 2 saniyede yüklenmeli", "Sistem 7/24 çalışmalı").
*   **Geçiş Gereksinimleri (Transition Requirements):** AS-IS durumundan TO-BE durumuna geçerken neye ihtiyacımız var? (Örn: "Eski verilerin yeni sisteme aktarılması", "Kullanıcı eğitimi").

### 2. Gereksinim Çıkarımı (Elicitation) - Bilgi Madenciliği
Gereksinimler ortada durup toplanmayı beklemez; onları kazıp çıkarmanız gerekir. Bu "Elicitation" (Çıkarım) sanatıdır.
*   **Mülakatlar (Interviews):** Birebir görüşmeler. Hazırlıklı gitmek, doğru soruları sormak ve güven ortamı oluşturmak kritiktir.
*   **Çalıştaylar (Workshops / JAD):** Farklı paydaşları aynı odaya kapatıp, çatışan gereksinimleri orada çözmek. En hızlı sonuç alınan yöntemdir.
*   **Gözlem (Job Shadowing):** Kullanıcının ne söylediğine değil, ne yaptığına bakmak. Genellikle kullanıcılar rutin işlerini anlatmayı unuturlar, ama siz gözlemlerken fark edersiniz.
*   **Prototipleme (Prototyping):** İnsanlar görsel bir şey gördüklerinde ne istediklerini (veya ne istemediklerini) daha iyi anlarlar. "Fail fast" (hızlı hata yap) prensibi için mükemmeldir.

### 3. Analiz ve Modelleme - Karmaşıklığı Yönetmek
Toplanan ham veri yığını, analiz edilmeden işe yaramaz.
*   **Gereksinim Önceliklendirme:** MoSCoW tekniği (Must have, Should have, Could have, Won't have). Her şey acil ve önemli olamaz.
*   **Modelleme:** Metinler yanlış anlaşılmaya açıktır, diyagramlar ise nettir. Use Case diyagramları, State Machine diyagramları ile gereksinimleri görselleştirin.

### 4. Dokümantasyon ve Spesifikasyon (SRS / BRD)
Söz uçar, yazı kalır. Analistin imzası, ürettiği dokümandır.
*   **BRD (Business Requirement Document):** Projenin iş hedeflerini ve yüksek seviye kapsamını anlatır. Yöneticiler içindir.
*   **SRS (Software Requirement Specification):** Yazılımcılar ve test uzmanları için İncil niteliğindedir. Sistemin her davranışını en ince ayrıntısına kadar teknik dille anlatır. "Atomic" (bölünemez), "Unambiguous" (muğlak olmayan) ve "Testable" (test edilebilir) olmalıdır.

### 5. Doğrulama ve Onay (Verification & Validation)
*   **Verification:** "Sistemi doğru mu inşa ediyoruz?" (Gereksinimler kaliteli mi, standartlara uygun mu?)
*   **Validation:** "Doğru sistemi mi inşa ediyoruz?" (Bu gereksinimler müşterinin gerçek ihtiyacını karşılıyor mu?)

## 🛠️ Teknisyen Notları (Metal Yaka Perspektifi)

*   **Müşteri Her Zaman Haklı Değildir, Ama Her Zaman Bir Derdi Vardır:** Müşteri "Bana uçan araba yap" diyorsa, belki de sadece "trafiğe takılmadan eve gitmek" istiyordur. Çözüme değil, probleme odaklan.
*   **'Neden?' Sorusu En Güçlü Silahınızdır:** Bir istek geldiğinde en az 3 kere "Neden?" diye sorun (5 Why Tekniği). Gerçek kök nedene ancak böyle inersiniz.
*   **Muğlaklık Düşmanınızdır:** "Kullanıcı dostu arayüz" bir gereksinim değildir. "Kullanıcı 3 tıkla işlemi bitirebilmeli" bir gereksinimdir. Ölçülebilir olun.

---
*Gereksinim mühendisliği, belirsizliğe karşı açılmış bir savaştır.*
