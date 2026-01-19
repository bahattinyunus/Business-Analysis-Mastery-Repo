# 🛠️ JIRA Power User Guide

JIRA, bir proje yönetim aracıdır ama doğru kullanılırsa bir Analistin "Kontrol Kulesi"ne dönüşür. Sadece task açıp kapatmak yetmez, JIRA'yı yönetmeniz gerekir.

## 1. JIRA Hiyerarşisi
Bu yapıyı bozmayın, kaos çıkar:
*   **Epic:** Büyük proje veya modül. (Örn: "Mobil Uygulama yenilemesi").
*   **User Story:** Epic'in parçası, kullanıcı değeri. (Örn: "Login Ekranı Tasarımı").
*   **Task:** Teknik işler. (Örn: "Database tablosunun oluşturulması").
*   **Sub-Task:** Task'ı yapan kişinin kendine notları. (Örn: "API dokümanını oku").
*   **Bug:** Hata kaydı.

## 2. JQL (Jira Query Language) - Sihirli Değnek
JIRA'nın arama çubuğuna yazacağınız basit kodlarla yüzlerce task arasından iğneyle kuyu kazabilirsiniz.

*   **Açık kalan işlerim:**
    `assignee = currentUser() AND status != Done`
*   **Benim açtığım ama başkasında bekleyen işler:**
    `reporter = currentUser() AND status not in (Done, Closed)`
*   **Geçen hafta tamamlananlar:**
    `project = "PH" AND status = Done AND resolutiondate > -7d`
*   **Önceliği yüksek ama dokunulmamışlar:**
    `priority in (High, Highest) AND updated < -5d`

## 3. Workflow (İş Akışı) Durumları
Bir story'nin yaşam döngüsü şöyledir:
1.  **To Do:** Backlog'da bekliyor.
2.  **In Analysis:** Analist (Siz) üzerinde çalışıyorsunuz.
3.  **Ready for Dev:** Analiz bitti, yazılımcı alabilir. (DOR - Definition of Ready).
4.  **In Progress:** Yazılım yapılıyor.
5.  **In QA / Testing:** Test ediliyor.
6.  **Done:** Bitti ve Canlıya çıkmaya hazır. (DOD - Definition of Done).

> **İpucu:** Analist olarak sizin en kritik durağınız **"Ready for Dev"** statüsüdür. Analizi bitmemiş, kriterleri netleşmemiş, ekran görüntüsü eklenmemiş bir işi ASLA yazılımcıya atamayın. Bu, çöp üretimine yol açar.

---
*JIRA bir çöplük de olabilir, bir hazine de. Farkı yaratan, içine girdiğiniz verinin kalitesidir.*
