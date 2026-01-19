# 💾 SQL Cheat Sheet: Verinin Anahtarı

Bir İş Analisti için SQL (Structured Query Language), "nice to have" değil, "must have" bir yetkinliktir. Yazılımcıya "bana rapor gönder" demek yerine, veriyi kaynağından kendiniz almalısınız.

## 1. Temel İskelet (Anatomi)

Her SQL sorgusu bu temel iskelet üzerine kuruludur:

```sql
SELECT kol1, kol2    -- Neyi görmek istiyorum? (Sütunlar)
FROM tablo_adi       -- Nereden almak istiyorum? (Tablo)
WHERE kosul          -- Hangi satırları istiyorum? (Filtre)
ORDER BY kol1 ASC;   -- Nasıl sıralamak istiyorum? (Sıralama)
```

## 2. JOIN: Tabloları Birleştirmek

Analistlerin en sık kullandığı (ve karıştırdığı) konudur.

*   **INNER JOIN:** Kesişim Kümesi. Sadece **her iki tabloda da** eşleşen kayıtları getirir. (Örn: Sadece sipariş vermiş müşteriler).
*   **LEFT JOIN:** Sol tablonun **HEPSİ** + Sağ tablonun eşleşenleri. (Örn: Tüm müşteriler ve varsa siparişleri. Siparişi olmayanlar NULL gelir). *En sık kullanılan budur.*
*   **RIGHT JOIN:** Sağ tablonun **HEPSİ** + Sol tablonun eşleşenleri.
*   **FULL OUTER JOIN:** Birleşim Kümesi. Her iki tablodaki her şeyi getirir.

```sql
SELECT M.MusteriAdi, S.SiparisTarihi
FROM Musteriler M
LEFT JOIN Siparisler S ON M.MusteriID = S.MusteriID;
```

## 3. Gruplama ve Filtreleme (GROUP BY & HAVING)

Veriyi özetlemek için kullanılır.

*   **COUNT():** Satır sayar.
*   **SUM():** Toplar.
*   **AVG():** Ortalamasını alır.

> **⚠️ Kritik Fark:** `WHERE` ham veriyi filtreler, `HAVING` ise gruplanmış (özetlenmiş) veriyi filtreler.

**Örnek:** Toplam sipariş tutarı 10.000 TL'den büyük olan müşterileri getir.

```sql
SELECT MusteriID, SUM(Tutar) as ToplamCiro
FROM Siparisler
GROUP BY MusteriID
HAVING SUM(Tutar) > 10000;
```

## 🛠️ Metal Yaka İpuçları
1.  **SELECT * FROM Yapmayın:** `SELECT *` (Tüm sütunları getir) veritabanını yorar. Sadece ihtiyacınız olan sütunları yazın.
2.  **NOLOCK Kullanımı:** Canlı sistemde rapor çekerken tabloyu kilitlememek için (MSSQL'de) `WITH (NOLOCK)` kullanmayı alışkanlık edinin.
3.  **NULL Kontrolü:** Veri her zaman dolu gelmez. `IS NULL` veya `IS NOT NULL` kontrollerini unutmayın.
