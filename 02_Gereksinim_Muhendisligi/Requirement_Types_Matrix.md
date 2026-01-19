# 📋 Requirement Types Matrix & Quality Checklist

İyi bir gereksinim dokümanı (BRD/SRS), hukuki bir sözleşme kadar net olmalıdır. Yoruma açık her cümle, gelecekte bir "Bug" veya "Change Request" olarak size geri dönecektir.

## 1. Gereksinim Hiyerarşisi Matrisi

| Gereksinim Tipi | Odak Sorusu | Örnek (E-Ticaret Sitesi) | Sahibi |
| :--- | :--- | :--- | :--- |
| **Business Req.** | **NEDEN?** (Hedef) | "Sepeti terk etme oranını 6 ayda %20 azaltmak." | Sponsor / CEO |
| **Stakeholder Req.** | **NE?** (İhtiyaç) | "Müşteriler, üye olmadan da hızlıca ödeme yapabilmeli (Guest Checkout)." | Product Manager |
| **Functional Req.** | **NE YAPACAK?** (Davranış) | "Sistem, 'Ödeme Yap' butonuna basıldığında kullanıcının email adresini kontrol etmelidir." | İş Analisti (BA) |
| **Non-Functional** | **NASIL OLACAK?** (Kalite) | "Ödeme sayfası mobilde 2 saniyenin altında yüklenmelidir." | System Architect |
| **Transition Req.** | **GEÇİŞ?** (Hazırlık) | "Mevcut 10.000 ürünün verisi yeni veritabanına aktarılmalıdır." | Data Team |

## 2. Mükemmel Gereksinim İçin "INVEST" Kriterleri

User Story yazarken bu filtreyi kullanın:

*   **I - Independent (Bağımsız):** Başka bir story'ye bağımlı olmadan geliştirilebilir mi?
*   **N - Negotiable (Müzakere Edilebilir):** Detayları tartışmaya açık mı? (Emir değil, davet olmalı).
*   **V - Valuable (Değerli):** Kullanıcıya veya müşteriye bir fayda sağlıyor mu?
*   **E - Estimable (Tahmin Edilebilir):** Ekip bunun ne kadar süreceğini kestirebiliyor mu?
*   **S - Small (Küçük):** Bir Sprint içine sığacak kadar küçük mü?
*   **T - Testable (Test Edilebilir):** Bittiğinde "Tamam" diyebilmek için net kriterleri var mı?

## 3. Kötü vs İyi Gereksinim Örnekleri

**❌ Kötü:** "Sistem kullanıcı dostu ve hızlı olmalı."
*   *Neden Kötü?* "Hızlı" kime göre? "Kullanıcı dostu" nasıl ölçülür? Test edilemez.

**✅ İyi:** "Sistem, ana sayfayı 4G bağlantıda 3 saniyenin altında yüklemelidir."
*   *Neden İyi?* Ölçülebilir, net, test edilebilir.

**❌ Kötü:** "Raporlama ekranı geliştirilmeli."
*   *Neden Kötü?* Hangi rapor? Hangi formatta? Kim görecek?

**✅ İyi:** "Finans Müdürü, aylık satış raporunu Excel formatında, tarih aralığı seçerek indirebilmelidir."
*   *Neden İyi?* Aktör belli, aksiyon belli, çıktı belli.

---
*Gereksinim yazmak, geleceği kodlamaktır. Hatalı yazılan her satır, teknik borçtur.*
