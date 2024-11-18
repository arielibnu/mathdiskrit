---
title: Graph

---

# Graph
 Graph merupakan kumpulan note yang saling berhubungan.
 
### Social Network Analysis
merupakan bidang kajian yang mengekplorasitentang hubungan manusia dengan menggunakan teori graf. Implementasi Social Network Analysis dapat menjelaskan relasi atau hubungan antar aktor melalui visualisasi berbentuk graf. Relasi dalam analisis jaringan sosial dapat diproses dalam bentuk perhitungan yang disebut centrality dalam sebuah jaringan sosial sesuai dengan posisi masing-masing aktor di dalam struktur jaringan tersebut


### Social Network

![image](https://hackmd.io/_uploads/HJYO_H_fJx.png)

![image](https://hackmd.io/_uploads/HyHK_ruGyg.png)


 Terdapat node yang mewakili  orang atau individu atau aktor. Relasi antar objek dapat dinyatakan dengan link atau edges yang terjadi antara aktor tersebut Social Network terdiri dari banyak aktor yang mempunyai relasi satu sama lain hingga membentuk petra jaringan sosial yang dinyatakan dengan Graph
 
- Tidak semua node dalam jaringan adalah penting  (aktor)
- Mencari node yang paling penting dalam suatu jaringan
- Centrality adalah penentuan aktor menggunakan ukuran pada Social Network Centrality dalam teori graf dan social network .Dibagi menjadi empat jenis, 
-degree centrality, 
-betweeness centrality, 
-closeness centrality 
-eigenvector centrality
 
### Degree Centrality 
- Degree Centrality adalah jumlah edge yang terkoneksi pada satu node yang mewakili interaksi.
- Pentingnya node ditentukan oleh jumlah node yang berdekatan dengan node tersebut
-Lebih besar derajatnya (degree), maka lebih penting node tersebut dalam suatu jaringan
-Hanya sebagian kecil node yang memiliki derajat tinggi dalam jaringan

- Degree Centrality: $C_D(v_i) = d_i = \sum A_{ij}$
- Normalisasi Degree Centrality: $C_D(v_i) = \frac{d_i}{(n - 1)}$

![image](https://hackmd.io/_uploads/r1UwOB_MJg.png)

Untuk  node 1, degree centrality adalah 3;
Normalisasi degree centrality adalah
$\frac3{(9-1)}=\frac38$.



### Closenes Centrality
Closenes Centrality adalah nilai kedekatan antara satu node dengan node lain dalam jaringan dengan menghitung rata-rata dari jarak relasi node-node tersebut. Skor Closeness Centrality mewakili kecepatan dalam penyebaran informasi.

- Average Distance: $D_{avg}(v_i) = \frac{1}{n-1} \sum_{j \neq i}^{n} g(v_i, v_j)$
- Closeness Centrality: $C_c(v_i) = \left[ \frac{1}{n-1} \sum_{j \neq i}^{n} g(v_i, v_j) \right]^{-1} = \frac{n-1}{\sum_{j \neq i} g(v_i, v_j)}$


### Betweenness Centrality
- Skor Betweenness Centrality mewakili beberapa besar informasi yang tersebatr dari suatu aktor . Semakin besar skor, artinya aktor tersebut semakin berperan dalam penyebaran informasi.

- Semakin banya lintasan yang harus melewati persimpangan itu (misal tidak ada jalan alternatif), maka semakin penting arti persimpangan tersebut. Hal ini menandakan seberapa besar suatu node diperlukan sebagai penghubung dalam penyebaran informasi di dalam jaringan.

- Ukuran ini juga bisa digunakan untuk mengidentifikasi Boundary spanners, yaitu orang atau node yang berperan sebagai penghubung (jembatan) antara dua komunitas.

- Menghitung jumlah lintasan terpendek yang melewati suatu node
- Node dengan  betweenness  tinggi  adalah  penting dalam komunikasi dan penyebaran informasi
- Betweenness Centrality

$C_B(u_i) = \sum_{\substack{u_j \neq u_i \\ u_j \in V, s < t}} \frac{\sigma_{st}(u_i)}{\sigma_{st}}$

$\sigma_{st}$ Jumlah lintasan terpendek antara  s dan t

$\sigma_{st}(v_i)$ Jumlah lintasan terpendek antara s dan t yang melewati $v_i$

![image](https://hackmd.io/_uploads/B1OS6H_fye.png)
$C_B$ (4) = 15

![image](https://hackmd.io/_uploads/HyGY6r_zJl.png)

betweenness centrality untuk node 5?
$\sigma_{st}$ = Jumlah lintasan terpendek antara  s dan t

$\sigma_{st}(v_i)$ Jumlah lintasan terpendek antara s dan t yang melewati $v_i$

$C_B(u_i) = \sum_{\substack{u_j \neq u_i \\ u_j \in V, s < t}} \frac{\sigma_{st}(u_i)}{\sigma_{st}}$

### Normalisasi Betweenness Centrality
$C'_B(i) = \frac{C_B(i)}{(n-1)(n-2)/2}$