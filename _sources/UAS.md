---
title: Column 1

---

$$(P\to\ Q)\to(R\to\ S)$$

| P   | Q   | R   | S   | 
| --- | --- | --- | --- |
| T   | F   | T   | T   |
| T   | T   | F   | T   |
| F   | T   | T   | F   |
| F   | T   | F   | F   |
| T   | F   | F   | T   |
| F   | T   | T   | F   |
| T   | F   | F   | T   |
| F   | T   | T   | F   |




## Hitung Closenes Centrality = G 
## Hitung Betweenness Centrality = F
![Gambar WhatsApp 2024-12-09 pukul 14.04.23_0e5641d3](https://hackmd.io/_uploads/SkgWUfNNJl.jpg)

### Closenes Centrality
 (G,F)= 1
 (G,D)= 1
 (G,E)= 1
 (G,B)= 2
 (G,C)= 2
 (G,A)= 3

Total jarak=1+1+1+2+2+3=10


$$
C(G) = \frac{n - 1}{\text{Total Jarak}} = \frac{7 - 1}{10} = \frac{6}{10} = 0.6
$$

### Betweenness Centrality

$$
Graf memiliki 7 node: ( A, B, C, D, E, F, G ). Pasangan unik adalah:
(A, B), (A, C), (A, D), (A, E), (A, F), (A, G), (B, C), (B, D), (B, E)
$$Total pasangan: $$ \binom{7}{2} = 21 $$

### *Jalur yang Melewati \( F \):
$$1.  (A, F) :  A \to D \to F  (*melewati  F )$$
$$2.  (B, F) :  B \to D \to F  (*melewati  F )$$
$$3.  (C, F) :  C \to D \to F  (*melewati  F )$$
$$4.  (E, F) :  E \to D \to F  (*melewati  F )$$
$$5.  (G, F) :  G \to D \to F  (*melewati  F )$$

$$
C_B(F) = \frac{5}{21} \approx 0.238
$$
