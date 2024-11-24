---
title: deret & rekursif

---

# Deretan dan Rekursi

## Deretan (Sequence)
Deretan adalah suatu urutan atau susunan elemen atau objek yang disusun secara teratur berdasarkan suatu aturan tertentu. Elemen dalam deretan biasanya berupa angka, huruf, simbol, atau objek lainnya.

### Definisi
Sebuah deretan adalah fungsi dari subset suatu himpunan bilangan bulat (biasanya \( \mathbb{N} \) atau \( \mathbb{P} \)) ke sebuah himpunan \( S \).

$$
\mathbb{N} = \{1, 2, 3, 4, \dots \}
$$

Contoh:
$$
S = \{2, 4, 6, 8, \dots \}, \quad \{1/3, 1/5, 1/7, \dots \}, \quad \text{dsb.}
$$

Notasi deretan:
$$
\{a_n\}
$$

Deretan umumnya dinyatakan dalam formula:
$$
a_n = 2n, \quad a_n = \frac{1}{n}, \quad a_n = 7 - 3n
$$

Contoh deretan:
- Deretan bilangan ganjil: \(1, 3, 5, 7, \dots\)
- Deretan bilangan genap: \(2, 4, 6, 8, \dots\)
- Deretan aritmetika: \(3, 6, 9, 12, \dots\)

---

## Penjumlahan Deretan

### Deret Geometri
$$
S = \sum_{i=1}^{n} ar^{i-1} = a \frac{1-r^n}{1-r}, \quad r \neq 1
$$

### Deret Aritmetika
$$
S = \sum_{i=1}^{n} a + (i-1)d = \frac{n}{2} \big(2a + (n-1)d\big)
$$

### Sumasi Ganda
Contoh penggunaan: Hitung jumlah operasi "+" dalam algoritma berikut:

```plaintext
x = 0
for j = 1 to 10 do
    for k = 1 to j do
        x = x + 2
    end for
end for
