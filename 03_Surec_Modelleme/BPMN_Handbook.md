# 🔄 BPMN 2.0 Handbook: Süreçlerin Dili

Business Process Model and Notation (BPMN), iş süreçlerini çizmek için kullanılan küresel bir standarttır. "Kutular ve oklar" çizmenin ötesinde, bir sürecin mantığını işletilebilir (executable) hale getirmektir.

## 1. Temel Semboller (Cheat Sheet)

### 🟢 Eventler (Olaylar)
*   **Start Event (İnce Çember):** Süreci tetikleyen olay. (Örn: "Müşteri Sipariş Verdi").
*   **Intermediate Event (Çift Çember):** Süreç sırasında olan olaylar. (Örn: "Onay Bekleniyor", "5 Dakika Zaman Aşımı").
*   **End Event (Kalın Çember):** Sürecin sonu. (Örn: "Sipariş Teslim Edildi").

### 🟦 Aktiviteler (Activities)
*   **Task (Köşeli Dikdörtgen):** Tek bir iş birimi. (Örn: "Faturayı Kontrol Et").
*   **Sub-Process (Artı İşaretli Dikdörtgen):** İçinde başka bir akış barındıran kompleks aktivite. Detayı gizlemek için kullanılır.

### 🔶 Gatewayler (Karar Noktaları)
*   **Exclusive Gateway (X):** "YA/YA DA". Sadece tek bir yola gidilebilir. (Örn: Kredi Onaylandı MI? Evet ise A yoluna, Hayır ise B yoluna).
*   **Parallel Gateway (+):** "VE". Aynı anda birden fazla yola gidilir. (Örn: Bir yandan Kargo Hazırlanırken, diğer yandan Fatura Kesilir).

## 2. Havuz ve Kulvar (Pool & Lane) Mantığı

*   **Pool (Havuz):** Sürecin sahibi olan Organizasyon veya Sistem. (Örn: "E-Ticaret Şirketi", "Müşteri").
*   **Lane (Kulvar):** Havuzun içindeki roller veya departmanlar. (Örn: "Satış Ekibi", "Depo Sorumlusu", "Muhasebe").

> **Kural:** Oklar (Sequence Flow), Pool sınırlarını aşamaz! İki farklı Pool (Örn: Şirket vs Müşteri) birbiriyle ancak "Message Flow" (Kesik çizgili ok) ile konuşabilir.

## 3. İyi Bir Diyagram İçin Altın Kurallar

1.  **Soldan Sağa Akış:** Süreç daima zaman ekseninde soldan sağa akmalıdır.
2.  **Happy Path:** Önce sürecin en, sorunsuz, ideal akışını çizin. "Exception"ları (Hata durumlarını) sonra ekleyin.
3.  **Adlandırma:** Aktiviteleri daima **"Fiil + İsim"** şeklinde adlandırın.
    *   ❌ Fatura
    *   ✅ Faturayı Oluştur
    *   ✅ Ödemeyi Kontrol Et

## 4. Araçlar (Tools)
*   **Lucidchart / Visio:** Görsel çizim için standart.
*   **Camunda Modeler:** BPMN 2.0 executable modeller için profesyonel araç (Developer dostu).
*   **Draw.io:** Ücretsiz ve hızlı çözüm.

---
*Bir süreç modeline bakan herkes (CEO da, Junior Developer da) aynı şeyi anlamalıdır. BPMN bunun anahtarıdır.*
