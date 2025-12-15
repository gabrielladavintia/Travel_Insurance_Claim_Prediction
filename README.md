# Travel_Insurance_Claim_Prediction
Travel Insurance Claim Prediction Using Data Analytics and Machine Learning

## Overview Project

Project ini bertujuan untuk membangun **model machine learning** yang dapat memprediksi kemungkinan **klaim asuransi perjalanan (Travel Insurance Claim)** berdasarkan karakteristik pemegang polis dan detail perjalanan.
Model dikembangkan untuk membantu perusahaan asuransi dalam **manajemen risiko**, **efisiensi biaya**, dan **pengambilan keputusan berbasis data**.

Dataset yang digunakan berisi informasi demografis, detail perjalanan, produk asuransi, serta status klaim (Claim / No Claim).

---

## Stakeholder

* Investor
  Mengevaluasi keberlanjutan dan profitabilitas perusahaan.
* **Manajemen Perusahaan Asuransi**
  Mengambil keputusan strategis terkait risiko dan premi.
* **Tim Underwriting & Risk Management**
  Mengidentifikasi polis berisiko tinggi sejak awal.
* **Tim Data / Analytics**
  Mengembangkan dan memelihara model prediksi klaim.

---

## Tujuan Project

* Memprediksi kemungkinan **terjadinya klaim asuransi perjalanan**
* Mengurangi risiko **klaim yang tidak terdeteksi (False Negative)**
* Membantu **prioritisasi polis berisiko tinggi**
* Mendukung strategi:

  * Penentuan premi
  * Alokasi dana cadangan klaim
  * Mitigasi risiko sejak polis diterbitkan

---

## Result / Output Project

### 🔹 Model Terbaik

* **Model:** LightGBM (Tuned)
* **Evaluasi Utama:**

  * ROC AUC: Lebih baik dibanding model default
  * Recall (Claim): **±65%**
  * Precision (Claim): Rendah (±6%)
* Model lebih **berorientasi pada recall**, sesuai tujuan bisnis untuk meminimalkan risiko klaim yang terlewat.

### 🔹 Insight Penting

* Dataset sangat **imbalanced** (klaim jauh lebih sedikit)
* Beberapa fitur numerik menunjukkan **outlier**, namun masih relevan secara bisnis
* Model tree-based (LightGBM) relatif **robust terhadap outlier**

### 🔹 Cost–Benefit Perspective

* **Benefit:**

  * Mengurangi risiko kerugian besar akibat klaim yang tidak terdeteksi
  * Membantu fokus pada polis berisiko tinggi
* **Cost:**

  * Meningkatkan False Positive → potensi biaya operasional tambahan
* Trade-off ini **masih dapat diterima** untuk fungsi *early warning system*

---

## Rekomendasi

### Rekomendasi Bisnis

* Gunakan model sebagai **early warning / screening tool**
* Fokus pada **prioritisasi**, bukan keputusan final otomatis
* Mendukung pengambilan keputusan terkait premi dan cadangan klaim

### Rekomendasi Model

* Retrain model secara berkala (6–12 bulan)
* Monitor metrik utama: **Recall & F2-score**

### Rekomendasi Data

* Tambahkan fitur:

  * Riwayat klaim pelanggan
  * Jenis perjalanan (bisnis/liburan)
  * Risiko negara tujuan
* Kurangi missing value (misalnya pada fitur Gender)

---

**Author:**
Gabriella Davintia
****
