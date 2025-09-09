# Tugas-DAE-Outlier

## 📌 Apa itu Outlier?

**Outlier** adalah data yang memiliki nilai **jauh berbeda** dibandingkan sebagian besar data lainnya.

Contoh:
Jika sebagian besar data berada di kisaran 40–60, tapi ada nilai seperti 100 atau 120, maka itu kemungkinan besar adalah outlier.

---

## 🧠 Mengapa Outlier Penting?

- 🔍 **Mengganggu rata-rata**: Outlier bisa menaikkan atau menurunkan mean (rata-rata) secara ekstrem.
- ⚠️ **Bisa menandakan kesalahan input** atau masalah lain pada data.
- 📉 **Mempengaruhi model machine learning**, terutama model berbasis statistik seperti regresi linear.

---

## 🛠️ Cara Deteksi Outlier (Metode IQR)

Salah satu metode umum untuk mendeteksi outlier adalah **Interquartile Range (IQR)**:

1. Hitung **Q1** (kuartil bawah) dan **Q3** (kuartil atas)
2. Hitung **IQR = Q3 - Q1**
3. Tentukan batas:
   - Batas bawah = Q1 - 1.5 × IQR
   - Batas atas = Q3 + 1.5 × IQR
4. Data di luar batas ini dianggap outlier

---

## 📊 Visualisasi

### ✅ Boxplot

Boxplot digunakan untuk melihat distribusi data dan mengidentifikasi outlier:

```python
sns.boxplot(x=df['nilai'])
