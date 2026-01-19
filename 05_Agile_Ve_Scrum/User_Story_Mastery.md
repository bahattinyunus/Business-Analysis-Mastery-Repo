# 📝 User Story Mastery & Kabul Kriterleri

User Story, bir gereksinimi teknik dille değil, kullanıcının ağzından anlatan kısa bir hikayedir. Amaç dokümantasyon değil, üzerine konuşulacak bir zemin oluşturmaktır.

## 1. 3C Modeli
User Story sadece bir cümleden ibaret değildir:
1.  **Card:** Hikayenin yazıldığı kart (Özet cümle).
2.  **Conversation:** Analist, PO ve Yazılımcı arasındaki tartışma. Detaylar burada çıkar.
3.  **Confirmation:** İşin bittiğini doğrulayan kriterler (Acceptance Criteria).

## 2. Standart Format
> **AS A** (Kim?) <Rol>
> **I WANT TO** (Ne?) <Eylem/Özellik>
> **SO THAT** (Neden?) <Değer/Fayda>

**Örnek:**
*   **As a** Premium Üye,
*   **I want to** ödeme adımında kayıtlı kartlarımı görebilmek istiyorum,
*   **So that** her seferinde kart numaramı girmekle uğraşmam (Hız kazanırım).

## 3. Kabul Kriterleri (Acceptance Criteria) - Gherkin Syntax
Yazılımcıya "ne yapacağını", Testçiye "neyi test edeceğini" söyleyen kısımdır. **GIVEN / WHEN / THEN** formatı endüstri standardıdır.

**Senaryo: Başarılı Ödeme**
*   **GIVEN (Ön Koşul):** Kullanıcı "Ödeme" sayfasındadır VE sepetinde ürün vardır.
*   **WHEN (Eylem):** Kullanıcı "Öde" butonuna tıkladığında.
*   **THEN (Sonuç):** Sistem kredi kartı provizyonunu almalıdır VE kullanıcıyı "Sipariş Onayı" sayfasına yönlendirmelidir.

**Senaryo: Yetersiz Bakiye**
*   **GIVEN:** Kullanıcının kartında yeterli limit yoktur.
*   **WHEN:** Kullanıcı "Öde" butonuna tıkladığında.
*   **THEN:** Sistem "Yetersiz Bakiye" hata mesajı göstermelidir VE sipariş oluşmamalıdır.

## 4. Bir Story Nasıl Parçalanır? (Splitting)
Devasa bir hikayeyi (Epic) yutamazsınız, lokmalara ayırmanız gerekir:
1.  **Workflow Adımları:** (Giriş Yap -> Ara -> Sepete At -> Öde). Her adım bir story olabilir.
2.  **Business Rules:** (Normal Ödeme vs Taksitli Ödeme).
3.  **Data Varyasyonları:** (Türkçe Arayüz vs İngilizce Arayüz).

---
*İyi bir User Story, "Nasıl" sorusunu yazılımcıya bırakır, "Ne" ve "Neden" sorularına odaklanır.*
