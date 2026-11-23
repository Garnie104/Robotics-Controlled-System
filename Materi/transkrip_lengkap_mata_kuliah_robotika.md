# Transkrip Lengkap Perkuliahan: Sistem Persepsi, Robot Vision, & Arsitektur Kognitif Robotika

* **Mata Kuliah:** Robotika (Pertemuan Minggu ke-10)
* **File Audio Sumber:** `Robot pertemuan minggu 10.mp3`
* **Durasi Rekaman:** 00:42:55
* **Pembicara:** Dosen Pengampu (Pak Agung) & Mahasiswa

---

## Sesi 1: Kinematika Dasar, Differential Drive, dan Kontrol PID (00:00 – 02:34)

**[00:00] [Dosen]:**
Dia punya dua penggerak utama, kiri dan kanan. Jadi ini adalah orientasinya yang mengarah ke arah tertentu dan apa, putaran sudut antara roda kiri dan roda kanan atau motor kiri dan motor kanan, RPM-nya ini akan menghasilkan *velocity command* ya, ke arah mana. *Velocity vector*-nya ke mana, dan kecepatannya seperti apa, yang besarnya.

**[00:25] [Dosen]:**
Nah, ini akan sangat bergantung. Jadi simpelnya adalah ketika kita ingin gerakkan robotnya lurus, RPM kiri dan kanan harus sama. Karena begitu ada selisih, pasti robotnya akan belok. Kalau yang lebih kencang yang kiri otomatis dia akan belok kanan. Dan sebaliknya kan, kalau yang lebih kencang adalah putaran motor kanan maka robotnya akan belok ke kiri gitu.

**[00:48] [Dosen]:**
Kalau misalkan punya kecepatan sama tapi arahnya berbeda ya, maka robotnya akan berputar pada poros. Ini... atau titik beratnya ya, titik beratnya di mana nanti robotnya akan berputar di situ.

**[01:08] [Dosen]:**
Jadi, ini yang paling simpel ya, kalau teman-teman kalau ini ya kalau mau coba gitu kalau di sini ada studi robot dasar itu pakai *line follower*, itu kan hanya dua motor yang kiri dan kanan. Kiri dan kanan yang pakai konstruksi *differential drive*. Jadi cukup memberikan *command* kepada motor kiri dan kanan mau geraknya seperti apa. Kalau mau lurus, berarti RPM-nya harus sama, gitu ya.

**[01:40] [Dosen]:**
Dan kalau kalian bermain lagi di apa, di kuliah kontrol ada yang namanya PID. Nah PID itu juga akan mengatur nanti ketika kita sudah menentukan *set point*-nya lurus. Ketika *set point*-nya lurus, berarti diturunkan sehingga diketahui bahwa si RPM-nya harus sama persis antara kiri dan kanan.

**[02:05] [Dosen]:**
*Even* itu sangat sulit dicapai, sehingga biasanya robotnya tetap akan berosilasi. Dia tidak akan *smoothly* lurus gitu. Pasti akan ya, apa, agak geser dikit lah. Nanti akan kembali lurus. Dan kiri kanan, kiri kanan, berosilasi.

---

## Sesi 2: Sistem Persepsi Robotika: Proprioception dan Exteroception (02:35 – 05:24)

**[02:35] [Dosen]:**
Nah, tadi berkaitan dengan sistem persepsi ya. Sistem persepsi di dalam robotika ini *proprioception* dan *exteroception*.

**[02:45] [Dosen]:**
Jadi untuk yang *proprio*, ini internal ya, *internal state*. Jadi *internal state* ini biasanya berkaitan dengan dirinya, jadi contoh sensor yang biasanya di-*apply* adalah *encoders* ya. *Encoders* berarti menghitung putaran, ya putaran dari roda. Misalkan berapa kali putaran rodanya. Jadi ini digunakan untuk mengatur hal tadi. Robotnya mau bergerak lurus, mau belok, atau mau seperti apa, ya. Itu biasanya pakai *encoders*.

**[03:15] [Dosen]:**
Kemudian IMU, IMU berarti untuk mengatur apanya? Apa? *Attitude*, ya. *Attitude* dalam arti ya sikap, ya sikap dari robotnya. Apakah nanti dia harus apa menyesuaikan gitu ya *balancing* untuk penyeimbang. Ketika dia berat sebelah, kan bagaimana mengembalikan agar *center of gravity* dari robot itu bergeser ke tengah. Nah itu bisa diatur caranya dengan, ya tadi dia memberikan gaya berbeda antara kiri dan kanan sebagai penyeimbang. Mana yang lebih berat gitu.

**[03:55] [Dosen]:**
Kemudian baterai *level*, contohnya tadi ya, biasanya dipakai di apa eksplorasi robot gitu, robot yang digunakan untuk *explore* baik yang *drone*, yang terbang, UGV, UAV dan lain-lain. Biasanya pergerakannya jauh. Jadi untuk mendeteksi atau mengatur agar robot tidak hilang. Ya dan lain-lain lah ya, cukup banyak kalau...

**[04:25] [Dosen]:**
Kemudian yang *exteroception*, tadi contohnya ya *range finder* gitu pakai LiDAR misalkan. Dia pakai ultrasonik. Dia pakai *depth cam*, dan lain sebagainya. Atau yang secara visual. Secara visual menggunakan kamera. Kamera biasanya nanti berhubungan dengan *computer vision*, di dalam sistem kognitifnya. Bagaimana *image* atau *video stream* yang ditangkap itu bisa dipersepsikan menjadi satu penanda, ya apakah digunakan misalkan untuk *visual homing*, ya untuk *landmarking* dan lain sebagainya kan. Ini pakai kamera.

**[04:58] [Dosen]:**
LiDAR pun sama ya, LiDAR juga bisa digunakan untuk melakukan pemetaan, mengenali posisi ya di dalam lingkungan, dan lain sebagainya. Ya ini tidak perlu lah ini kalian rasanya sudah kenal anak semester akhir ya, sensor-sensor di dunia dengan IMU... ini untuk apa? *Encoder* tadi...

---

## Sesi 3: Implementasi Persepsi & Studi Kasus Vacuum Cleaner (05:25 – 09:59)

**[05:25] [Dosen]:**
Nah ini *implementation*-nya, ya implementasinya. Jadi *perception* ini tadi ya sensor. Jadi bisa *single sensor* bisa *multi-sensor*. Bisa berupa *fusion sensor* juga. Ya menggabungkan informasi dari beberapa sensor yang dipakai untuk mempersepsikan keadaan lingkungan ataupun keadaan dirinya.

**[05:50] [Dosen]:**
Oke misalkan di dalam *drone*, kalau *drone* kan yang bisa dibilang cukup kompleks ya, karena *dynamics*-nya 3D gitu, *three-dimensional*. Kalau kita mempersepsikan sikap dari *drone*, ini biasanya gabungan semua sensornya. Ya, baik berupa IMU, *gyroscope*, kemudian apa lagi? *Optical flow*, barometer, dan lain sebagainya. Karena dia harus mengetahui keseimbangan dirinya sekaligus mengetahui keadaan ini ya sori, keadaan atau posisinya itu berada di ketinggian berapa. Ya biasanya menggunakan tambahan dari barometer, dari *optical flow*, *even* untuk mengetahui posisi diri juga dia menggabungkan dengan GPS-nya juga. Ya. Jadi sekaligus dia menggabungkan baik dari *proprio*-nya, *internal state*-nya, dengan *external state*-nya juga.

**[06:45] [Dosen]:**
Nah ini yang sederhana misalkan untuk konteks ini *vacuum cleaner* ya. *Vacuum cleaner* sederhana. Jadi persepsinya hanya menggunakan *bump sensor* atau tabrak. Itu biasanya hanya pakai *limit switch*. Jadi ketika dia berbenturan dengan dinding ya sudah berarti ada yang menabrak di situ. Ya.

**[07:05] [Dosen]:**
Kemudian untuk *cognition system*-nya dia menggunakan mikrokontroler. Ya kalau sekarang mungkin tidak hanya sekedar mikrokontroler ya, tapi juga bisa menggunakan mikrokomputer ya, misalkan Raspi, ya terus pakai apa lagi selain Raspi? Oke, apa Jetson gitu ya? Atau lagi yang ya pakai jenis-jenis itulah ya, komputer mini gitu, bisa diterapkan.

**[07:25] [Dosen]:**
Kemudian, nah konstruksinya hanya menggunakan *differential drive*. Jadi robot sederhana ini. Kemudian dari apa, *action*, *action* ditujukan untuk... karena dia beraksi di dalam lingkungan pasti akan berubah ya *state*-nya. Apakah *state position* atau ya keadaan di lingkungannya sendiri.

**[07:45] [Dosen]:**
Ini penerapan pada *vacuum cleaner* yang menggunakan konsep reaktif. Kalau kita lihat contohnya kurang lebih seperti ini. Ya dia bergerak secara *random*. Ketika berbenturan maka dia akan memberikan satu... paradigma reaktif tertentu bergerak ke mana. Apakah mundur, apakah dia belok sekian derajat, atau lurus atau seperti apa. Ya. Jadi *randomly*. Secara *random* dia akan men-*generate* gerakannya. Ya apakah tahu posisinya sudah bersih atau belum? Ya tidak. Kalau model-model yang sekarang...

**[08:10] [Mahasiswa]:**
*(Bertanya pelan mengenai kepastian pembersihan dan sensor pada vacuum cleaner)* ...memastikan gitu, Pak... apakah dia harus...

**[08:25] [Dosen]:**
Ya ini contohnya. Jadi kalau kita lihat sebenarnya *bump sensor* itu hanya *limit switch* biasa saja sebenarnya. Jadi kayak ya *limiter* saja. Ketika dia berbenturan ada *input* ya, *digital input* hanya *logic* 0 atau *logic* 1. Kemudian ada ini si untuk *charging station*-nya, *infrared*. Kemudian ada ini rodanya jadi menggunakan dua motor ya kiri dan kanan dan pakai *encoder* sebagai tambahan untuk melihat putaran dan tentu menggerakkan beloknya sudutnya sudah berapa derajat, berfungsi untuk membelokkan...

**[09:05] [Dosen]:**
Dia menggunakan mekanisme reaktif ya atau *reactive behavior* ya, *reactive programming*. Jadi simpel sebenarnya kalau secara algoritma ya. Jadi kalau misalkan dia nabrak, maka yang dilakukan apa? Belok. Beloknya berapa? *Random*. Kalau nggak nabrak sudah dia gerak lurus sampai nabrak. Jadi ini sederhana ya, penerapan itu macam-macam. Jadi kalian kalau belajar ya harus mulai dari yang paling sederhana dulu.

**[09:40] [Dosen]:**
Nah apakah dia bertemu *obstacle*, jadi tidak ada mekanisme *obstacle avoidance*-nya, kalau ada *obstacle* tabrak saja. Nanti dia akan belok gitu nah.

---

## Sesi 4: Perilaku Navigasi Dasar & Multi-Robot (10:00 – 14:59)

**[10:00] [Dosen]:**
Nah berbeda kalau robot-robot yang sudah mulai kompleks dia sudah ada *obstacle avoidance*, maka dia akan menentukan satu jarak aman gitu. Ya, apakah pakai *potential field* atau menggunakan *spanning tree* / *space tree* ya dan sebagainya, RRT dan sebagainya lah ya. Banyak sekali metode yang dikembangkan.

**[10:25] [Dosen]:**
Nah ini contoh yang lebih kompleks. Contoh yang lebih kompleks misalkan untuk navigasi biasanya menggunakan *wall following*. Yang paling simpel. Ini *wall following* jadi hanya meraba dinding saja. Jadi pergerakannya adalah sejajar dengan dinding. Jadi ketika ketemu dinding ya sudah itu dijadikan sebagai pegangan. Ibaratnya orang buta, orang buta kalau jalan dia akan mengikuti satu penanda, dia punya pegangan. Nah pegangannya apa kalau *wall following* adalah dinding. Jadi kecenderungannya dalam penerapan *wall following* robot hanya akan bergerak di dekat dinding saja. Ya. Jadi di tengah bukan merupakan lintasan dari robot. Lintasan robot akan ter-*define* hanya di dekat dinding.

**[11:15] [Dosen]:**
Nah *visual homing* bisa dilakukan secara visual ataupun menggunakan apa, *point cloud* ya. *Point cloud* nanti bisa di-*generate* pakai LiDAR, pakai sensor *infrared* dan lain sebagainya, yang bisa kita *define* ketika dia mendapat satu *landmark*. *Landmark*-nya apa? Misalkan bentuk T, bentuk sudut siku dan seterusnya. Nah ini bisa di-*construct* baik secara visual maupun non-visual kalau sekarang. Jadi kalau misalkan dia *visual homing* ya, kalau ketemu posisi gambar tertentu sebagai *landmark* maka itu tujuan atau posisi awal. Ini tergantung nanti terdefinisinya di sistem seperti apa. Ya.

**[12:10] [Dosen]:**
Terus *centering*. Nah, kalau *centering* dia akan menetapkan posisi ya posisi pegangan kiri dan kanan, dia akan menetapkan di tengah. Bisa di-*construct* dari sensor visual kayak kamera yang umum kalau misalkan sekarang diterapkan di *autonomous car* gitu ya. *Autonomous car* kemudian bisa juga menggunakan pegangan sensor lain ya seperti untuk ini *ranging* ya. Jadi pakai LiDAR juga, pakai apa radar ya. Jadi untuk menetapkan mana batas kiri mana batas kanan, sehingga dia akan memposisikan diri di tengah.

**[12:50] [Dosen]:**
Nah, *collision avoiding* ini dia akan mengetahui posisi-posisi ini ya. Jadi kalau misalkan dilakukan secara *offline*, ini jalur dulu ditentukan di awal maka *map*-nya harus *known* ya, harus benar-benar sudah ditetapkan. Jadi *fully known environment* sehingga dia bisa menetapkan jalurnya seperti apa. Nah ini banyak metodenya, pendekatannya juga cukup banyak kalau *path planning*. Jadi bisa pakai apa **A\* (*A-star*)** yang paling simpel sampai dengan misalkan kalian menerapkan yang namanya *Voronoi algorithm* / *Voronoi graph* gitu itu juga sangat memungkinkan.

**[13:35] [Dosen]:**
Kemudian kalau kita sudah bicara tentang apa *multi-robot* ya, penerapan di *multi-robot* ini ada mekanisme yang namanya *flocking*. Jadi *flocking* ini menetapkan posisi robot, posisi satu robot berdasarkan posisi robot lain. Jadi harus saling mengetahui posisi juga. Ya. Jadi dalam *flocking* itu nanti akan membentuk satu apa satu kesatuan titik ya. Atau biasanya nanti kalau dalam apa penerapan yang lebih *advance*, *formation control*. Jadi membentuk suatu formasi tertentu. Ya. Kayak misalkan kita bicara tentang ya robot yang bergerak dalam satu formasi tertentu ya untuk keperluan apa misalkan. Ya atau kalian pernah lihat *show* ini ya, *show drone*, *drone show* yang jumlahnya banyak itu sudah *swarming* dan dia *flocking* di posisi-posisinya. Sehingga membentuk kayak burung api / bola api ya, misalkan tulisan. Jadi itu posisinya harus saling dikoordinasikan.

**[14:35] [Dosen]:**
Ini konteksnya di apa kontrol reaktif ya. Jadi tadi dalam prinsip otonom ya, prinsip otonomi, maka ditentukan dulu semuanya. Ini pakai ROS. Nah ini contoh kalau misalkan kalian ini kalau nggak salah ada ya? Apa kalian mau coba nanti harusnya masih jalan.

---

## Sesi 5: Karakteristik Sensor, Active vs Passive System, dan Depth/LiDAR (15:00 – 19:59)

**[15:00] [Dosen]:**
Kemudian kalau kita bicara tentang lebih dalam ya, terkait dengan *perception*. Nah ini contoh-contoh sensor yang banyak sekali sekarang diterapkan yang berbasisnya menggunakan untuk *infrared* untuk *ranging*, pakai radar ini radio ya gelombang radio, kalau LiDAR dia pakai *light*. Sama seperti *infrared* tapi dia lebih panjang gitu spektrumnya atau gelombangnya. Sonar, sonar mirip dengan radar sebenarnya *sound* ya gelombangnya gelombang suara, radar gelombang radio. Dia punya frekuensi yang berbeda.

**[15:30] [Dosen]:**
Sonar biasanya dipakai di mana? *Underwater* kan? Untuk *underwater* biasanya menggunakan sonar. Kalau radar itu di udara. Karena cepat rambatnya beda. Dan apa tingkat redaman yang terjadi kalau misalkan di udara dengan di air tentunya berbeda. Itu yang kenapa sonar mungkin banyak sekali diterapkannya justru di bawah air.

**[16:00] [Dosen]:**
Kemudian nah *stereo cam*, *stereo cam* berarti apa menggabungkan visual dengan *depth*, dengan jarak. *Stereo cam*. *Depth cam* ini sama ya kayak stereo. Nah kalau *depth* gimana? *Depth* ini ya sama sebenarnya hanya menggabungkan antara visual dengan sistem ya dengan sistem lain.

**[16:20] [Dosen]:**
Nah, untuk mekanisme *sensing* sendiri ada yang namanya *active system* dan *passive system*. Jadi kalau untuk *passive system* dia *rely on optic properties*-nya saja. Jadi misalkan *stereo vision* di pasif. Kemudian *depth* ini hanya digunakan untuk memfokuskan titik penangkapan visualnya. Berbeda kalau dengan aktif. Kalau aktif ini sensornya akan mengirim dulu sinyal keluar. Jadi dia punya *transmitter* dan punya *receiver* kembali.

**[16:50] [Dosen]:**
Contohnya apa? Ya kayak misalkan LiDAR atau radar. Dia kan nembakin ya. Dia menembakkan sinyal apa gelombang ya gelombang cahaya atau gelombang radio, misalkan untuk konteks LiDAR ya gelombang cahaya, kalau radar gelombang radio. Kemudian dia punya penangkap ya punya *receiver* juga. Itu *active system* untuk sensor.

**[17:10] [Dosen]:**
Jadi yang diukur *time of flight*-nya, jadi waktu respons *feedback*-nya ya. *Feedback* respons-nya ini ditangkap dalam waktu berapa lama, berapa *microsecond* atau *nanosecond* yang akan didefinisikan sebagai jarak. Ini jarak pantulnya yang diukur ya. Jarak pantulnya berdasarkan waktu yang diterima ya waktu pantulan yang diterima maupun intensitas kemudian distorsi, faktor distorsi, atau ini atenuasi ya kalau kita sudah bicara radio dan lain-lain dia ada pembelokan, ada peredaman. Nah kekuatan diterimanya berapa, dalam waktu berapa lama itu bisa digunakan untuk mengonstruksi baik bentuk maupun jarak dari lingkungan ya jarak terhadap satu *obstacle*.

**[17:35] [Dosen]:**
Ini *depth* kamera, *depth* kamera ini contoh yang sudah *obsolete* ya sebenarnya kalau *depth* kamera zaman-zaman Xbox dulu yang ada Kinect-nya itu sudah tidak ada ya sekarang. Nah ini biasanya untuk ya tidak hanya secara visual tapi juga menangkap jarak. Nanti akan di-*create* sebagai *image grayscale* yang hitam putih saja gitu tampak luarnya.

**[18:05] [Dosen]:**
Dan ini banyak sekali digunakan misalkan untuk *collision avoidance*, *obstacle avoidance*, bisa juga untuk *mapping* pemetaan untuk proses navigasi. Jadi akan kenal yang namanya *localization and mapping* jadi memposisikan diri sekaligus melakukan pemetaan. Jadi mengonstruksi *map* dari lingkungan secara langsung ya, itu bentuknya seperti apa di sekitar robot itu bisa menggunakan *depth* kamera.

**[18:30] [Dosen]:**
Mungkin kalau sekarang sudah di-*replace* kebanyakan menggunakan LiDAR. Karena harganya sudah terjangkau produk-produk untuk LiDAR ya. Berbeda kalau dulu LiDAR itu relatif masih mahal. Sekarang produk-produk LiDAR murahan juga cukup banyak meskipun jarak deteksi maupun *error* akurasinya juga mungkin tidak terlalu bagus. Tapi *at least* biasanya untuk navigasi UGV ya robot-robot sederhana itu sudah cukup.

**[19:00] [Dosen]:**
Ini contoh penerapan di ini gabungan ya dari banyak sensor dan visual kalau di kendaraan otonom. Kendaraan otonom dia akan mendeteksi depan, kemudian samping mobil, ketika ada mobil berarti si kalau sekarang kan sudah mulai cukup banyak ya ada mobil setengah otonom, mungkin bukan *full* otonom ya. Jadi di mobil-mobil modern sudah ada pendeteksi kalau misalkan ada objek di belakang, ada objek di *blind spot* ya kayak sensor-sensor parkir, sudah mulai juga banyak yang parkir otomatis gitu apa. Kalau di *lane* ya dia akan *focus lane* gitu untuk apa namanya menjalankan kendaraan tetap di jalurnya selama tidak ada halangan, atau *lane assist*, ketika ada objek di depan dan lain sebagainya. Ini kan sebenarnya gabungan dari banyak sekali sensor.

**[19:40] [Dosen]:**
Dan ya riset di kita ya riset di Indonesia juga sudah sangat banyak sebenarnya. Ini di BRIN juga berkutat banyak riset-riset yang kaitannya dengan *vision* karena visual. Jadi objek-objek visualnya ya dari lingkungan itu akan didefinisikan sebagai *landmark* kemudian objek-objek yang tertangkap di sekitar itu juga akan di-*define* untuk diterapkan di *obstacle avoidance* atau *collision avoidance*. Banyak sekali sekarang.

---

## Sesi 6: Perbandingan Robot Vision vs Computer Vision (20:00 – 25:44)

**[20:00] [Dosen]:**
Oke. Ada pertanyaan? Ada diskusi? Jadi kalau kita bicara *robot vision*, *robot vision* itu ya sama ya *computer vision* saja. Cuman kalau *computer vision* ya menggunakan komputer, biasanya konteksnya dalam ya kayak simulasi atau aplikasi. Tapi *robot vision* berarti diterapkan di robot. Biasanya *computing resource*-nya lebih rendah dibanding *computer vision*. Karena kalau *robot vision* *at least* dia harus *mobile*. Tingkat *mobility*-nya lebih tinggi dibanding penerapan di *computer vision*. *Resource*-nya lebih *low-power* gitu. Bedanya cuma di sana. Jadi kalau *robot vision* ini biasanya kompensasi dengan *resource computing*.

**[20:45] [Dosen]:**
Oke ya. Jadi kalau kita bicara *robot vision* ini penerapan sensori visual di dalam robotik. Jadi bagaimana dia kemudian bisa beroperasi di *real world*, mendefinisikan *real world* di sekitar *environment*-nya di sekitar robot di mana dia beroperasi atau bergerak.

**[21:05] [Dosen]:**
Dan ya kalau hari-hari ini artinya kenapa lebih ke *robot vision*? Karena sensor-sensor visual ini harganya jauh lebih murah. Kayak sekarang ESP-Cam itu cuma berapa puluh ribu. Terus Pi Cam / Raspi Cam itu cuma berapa ratus ribu. Itu kan harganya relatif jauh lebih murah dibanding *depth cam* atau dibanding LiDAR. Ya LiDAR masih lebih mahal dibanding kamera-kamera yang resolusi rendah seperti itu. Ya pikselnya sudah kecil memang, tapi *at least* ya cukup lah ya. Ya sebenarnya lebih dari cukup untuk menerapkan robot-robot yang hanya beroperasi di lingkungan *indoor* dan sebagainya. Dan secara *computing* ini akan lebih murah juga.

**[21:45] [Dosen]:**
Jadi kalau kita bicara antara *robot vision* dan *computer vision*, jadi lebih terbatas komputasinya, *limited*, ya *less memory* karena di-*embedded* ya. Kemudian *action-driven* jadi lebih ke reaktif tadi ya, *reactive programming*. Misalkan bagaimana responsnya biasanya juga dituntut lebih cepat. Karena dari persepsi ya ketika kita menangkap secara visual lingkungan, kondisi lingkungan itu harus secepat mungkin diproses dan menjadi satu *action* tertentu. Katakanlah berangkat apakah robotnya akan mengambil keputusan untuk bergerak lurus atau dia belok atau dia berhenti. Ini kan *action-driven*.

**[22:25] [Dosen]:**
Jadi kadang gini, kadang kalau di *robot vision* ini yang lebih dikejar adalah tingkat performansi dari sisi waktu dibanding akurasi. Jadi kayak misalkan sekarang nih terkait geopolitik, kan lagi perang. Banyak *drone-drone* yang dipakai untuk nyerang. Apakah harus akurat? Tidak. Itu yang penting titiknya ter-*define*. Ya sudah miring nggak apa-apa. Yang penting memang targetnya kena karena targetnya pasti target gede ya. Mau titiknya ya geser juga nggak ada masalah yang penting dekat dengan target. Itu yang dikejar. Karena mengejar murah, mengejar cepat responsnya.

**[22:55] [Dosen]:**
Jadi kalau misalkan dalam *drone* aplikasi kalau aplikasi *drone-drone* yang dipakai buat apa bom, nah yang namanya apa *drone* itu kan harus mendapatkan *input* yang cepat agar dia nggak tiba-tiba oleng atau *stall*. Jadi nggak berpengaruh apakah dia akurat atau tidak, atau *less accurate* ya. Katakanlah akurasinya 60% *it's okay*, yang penting responsnya cepat. Ya ketika dia ternyata miring ya tinggal perbaiki lagi nanti sistem apa arahnya ya, arahnya tinggal dibuat respons yang lebih cepat. Nah itu yang dilakukan.

**[23:25] [Dosen]:**
Kemudian *updating image*-nya ini biasanya sambil bergerak. Berbeda dengan *computer vision*. Kalau *computer vision* ini kita dapat data ini ya apa posisi dari komputer itu cenderung statis, posisi kameranya juga statis. Kayak kalian menerapkan apa sistem presensi berbasis wajah misalkan. Kan dia nggak gerak-gerak. Berbeda kalau misalkan penerapan *robot vision*, ini tantangannya lebih ke sana sebenarnya.

**[24:00] [Dosen]:**
Ini apa *abstraction* apakah mau diambil semua atau kita cukup ngambil *layer-layer* tertentu saja. Jadi kayak misalkan *input* itu kan tetap bisa kita *set*. Apakah kita hanya ambil *frame* tertentu atau memproses semua *video stream* yang masuk. Jadi dengan *frame rate* tertentu yang akan justru membebani sistem *computing*-nya. Ini juga harus hati-hati, makanya tadi kenapa ada apa ya *trade-off* ya antara akurasi dengan respons. Karena biasanya ini penerapan kita hanya mengambil *layer-layer* atau *frame* tertentunya saja, tidak semua *frame* diproses.

**[24:25] [Dosen]:**
Jadi kita hanya mengambil *frame* yang dianggap penting atau secara periodik ya kita tetapkan satu periode atau *frame rate* yang lambat dan itu kita proses atau hanya *capturing* saja. Kita hanya *capture image*, proses, kemudian robotnya bergerak, sebenarnya buta gitu ya, tapi dalam periode tertentu dia akan *capturing* lagi dan proses. Sehingga resolusi maupun akurasi pasti turun rendah tapi responsnya akan jauh lebih cepat.

**[24:50] [Dosen]:**
Oke *color cam*, nah kalau *color cam* ini tergantung ya aplikasinya. Apakah aplikasinya di standar industri, kalau standar industri yang membutuhkan presisi tinggi kalau kamera itu cukup penting diproses biasanya tidak menggunakan *image* yang aslinya RGB tapi akan *convert* ke HSV karena lebih *strong* ya. Dia lebih handal terhadap perubahan cahaya. Bahkan di-*scale* bukan hanya di *tri-color* dengan format dan lain sebagainya. Proses segmentasi ya ini silakan nanti dicoba saja sendiri, pelajari.

---

## Sesi 7: Sistem Kognisi, Finite State Machine (FSM), dan Parallel Behaviors (25:45 – 30:54)

**[25:45] [Dosen]:**
*Next* kita akan bicara *cognition*. Nah ini contohnya untuk *trash collector*. Jadi robot yang tugasnya ngambil sampah misalkan. Yang perlu diperhatikan apa kalau dalam *cognition*? *Cognition* bicaranya adalah struktur *computing*. Ya. Jadi biasanya kalian membuat apa sih, *flowchart*. *Flowchart* kerja atau diagram kerja, diagram alirnya, diagram prosesnya, atau bisa menggunakan penggambaran menggunakan apa FSM, *Finite State Machine*.

**[26:20] [Dosen]:**
Nah jadi untuk dia menggambarkan prosesnya dari mana ke mana apakah ada proses yang berulang atau lebih memperlihatkan *state* ya dan perubahannya. Karena kalau di kontrol sistem itu kan sebenarnya yang kita lihat untuk mengukur *performance* itu *response time*-nya. Yang di mana *response time* ini sebenarnya melihat waktu perubahan dari satu *state* ke *state* yang berikutnya. Nah ini yang dikejar kan di sana. Sehingga penggambaran proses itu biasanya lebih banyak dalam bentuk *Finite State Machine*.

**[26:55] [Dosen]:**
Jadi perubahan *state*-nya dari *state* awal robot hanya berkeliling. Kemudian apakah dia melihat sampah atau tidak. Apa yang dilakukan kalau misalkan dia melihat sampah. Berarti pergerakan akan diarahkan ke posisi sampah. Ya. Kemudian dia akan *grabbing* sampah dan seterusnya. Ya sampai dengan penuh, sampai dengan dibuang di *trash can*. Gitu. Ya mana yang dia akan pegang, mana yang dia tidak akan pegang, mana yang hanya melakukan *wandering* dan seterusnya. Ini semuanya di-*define* dalam *state diagram*-nya.

**[27:45] [Dosen]:**
Nah kemudian dari *state diagram* ini bisa di-*define* yang namanya *behavior*. Nah *behavior* ini biasanya ditetapkan atau dibuat dalam bentuk paralel. Jadi mana yang bisa dilakukan secara paralel. Ini untuk mempermudah struktur ini ya eksekusi. Ya jadi ketika misalkan ini kan dari apa persepsi ya dari persepsi ke *arbiter*-nya. Jadi untuk sampai ke *action* jadi kalau dia mempersepsikan sesuatu ya mendapatkan persepsi apakah ada sampah maka yang dilakukan apa, kalau tidak ada sampah apa yang dilakukan. Kemudian *action*-nya apa yang dilakukan: *drop trash*, *grab trash*, *move to can* dan lain-lain.

**[28:25] [Dosen]:**
Nah ini yang perlu dilihat ya kalau misalkan ada *parallel behavior*. Jadi ada yang *concurrent* atau tidak. Nah untuk *rules* yang *concurrent* ya *state-state* yang sifatnya *concurrent* itu harus diperlakukan dengan cara tertentu. Apakah dia dilihat sebagai *no state* ya *state* yang sebenarnya tidak ada apa tidak ada *action* juga, atau dalam kondisi tertentu justru *behavior* harus dilakukan secara bersamaan. Jadi akan aktif secara paralel atau bersamaan ya. Berarti ini akan men-*drive action* yang paralel, apakah motornya atau si apa namanya penjepitnya ya dan lain sebagainya. Ini harus ditentukan ya.

**[29:15] [Dosen]:**
Kemudian bagaimana *parallel behavior* ini punya satu keunggulan ya dibanding hanya murni reaktif *behavior*. Jadi biasanya lebih realistis. Kan kita melakukan sesuatu juga biasanya paralel. Tangan kita megang sesuatu sambil kita jalan itu kan sebuah tindakan yang paralel juga. Sambil kita jalan kita melihat ke depan, kaki kita bergerak, sambil apa lagi? Sambil memegang sesuatu, sambil gandengan misalnya, atau sambil apa lagi dan seterusnya. Jadi ada sambil sambil sambil. Nah ini yang diterapkan dalam struktur kognitif di robotik. Itu juga sama. Jadi mana yang bisa dilakukan sambil gitu ya. Jadi robotnya bisa melakukan apa (`while` melakukan sesuatu sambil hal lain). Nah ini semuanya ditetapkan dulu. Jadi ketika dibuat struktur programnya itu juga akan lebih mudah. Apalagi sekarang dukungan *programming* untuk *multithreading* dan lain sebagainya sudah cukup banyak.

---

## Sesi 8: Paradigma Arsitektur Robotika: Deliberatif, Reaktif, Hybrid, dan Model Modern (30:55 – 34:59)

**[30:55] [Dosen]:**
*Then* kita akan masuk ke sini. Jadi untuk struktur berpikirnya juga kurang lebih sama ya kalau kita lihat secara urutan. Jadi yang pertama kali dilakukan untuk setiap *behavior* tentunya dimulai dari *state sense* ya *sensing*. Jadi proses *sensing*, proses *percepting* sampai dia akan membuat satu *sequence*. Merencanakan satu *sequence* ketika mendeteksi satu atau mempersepsikan atau menangkap satu kondisi tertentu berdasarkan sensor. Baru melakukan *action*. Ya. Dan ini kalau di robot ya tentunya berbeda dengan sistem. Ini kalau satu robot tuh *sense-plan-act*-nya pasti banyak sekali. Nggak mungkin cuma satu. Kalau satu ya belum sampai ke tahap robot, hanya sistem sederhana saja. Kalau robot tuh ya dia bergerak, kemudian dia melakukan *sensing* dan lain sebagainya.

**[31:55] [Dosen]:**
Ini gambarannya secara deliberatif ya. Jadi *sense, plan, act*. Kalau tadi juga ada reaktif menggunakan *parallel behaviors* penerapannya dan kemudian *hybrid* arsitektur kita bisa menggabungkannya menggunakan *finite state*. Bisa digabung juga ya. Ketika *hybrid*, *hybrid* ini ya ini ya jadi *every behavior* ini *contain* ini sebenarnya kan *sense-plan-act* digambarkan dalam bentuk *finite state machine*. Bisa seperti itu.

**[32:30] [Dosen]:**
Ini *classical view* kalau kita lihat bandingan antara yang atas dan yang bawah. Secara klasik ya tadi ada *perception*, ada *cognition* hingga ke *action*. Nah *action* ini yang akan mempengaruhi posisi robot terhadap lingkungan. Nanti perubahan tersebut akan di-*perceive* lagi, masuk ke tahap kognisi lagi dan seterusnya ya. Ini *loop* proses di robot seperti itu.

**[33:05] [Dosen]:**
Nah kemudian yang bawah ya *radical idea*-nya ini dirubah. Jadi *perception* dan *action* ini satu kesatuan. Jadi ketika ada *perception* maka akan langsung ke *action* tanpa proses kognitif yang berlebihan. Tapi kognitifnya akan dilakukan... ya jadi apa ya, memisahkan lah ya. Jadi kalau ini kan secara *sequence*, ketika ketemu sesuatu berdasarkan sensor maka akan melalui proses kognitif. Kalau ini nggak, semuanya akan dikognitifkan. Bagaimana cara dia berpikir. Jadi ini yang tadi ya ketika kemudian robotnya bisa melakukan segala sesuatu secara paralel. Jadi justru kognitifnya yang mengatur secara keseluruhan. Ketika ada persepsi *action*, persepsi *action*. Jadi langsung kayak misalkan *if* langsung *then else* gitu ya. *If then, if then, if then*, itu semuanya dalam satu kesatuan. Jadi diatur di apa *higher layer*-nya, *upper layer*.

**[33:55] [Dosen]:**
Nah ini kalau kita lihat dibandingkan antara model lama dan model baru. Kalau model lama dari sensor kemudian melakukan *perception* kemudian eksekusi ya *planning, modeling, planning, task execution*, kemudian baru ke *action*-nya biasanya berupa *motor control*. Nah ini penerapannya. Jadi ketika ada sensor dia akan langsung... sebenarnya sudah ada *library* ya, sudah ada *library* proses yang dibangun di dalam sistem kognitif secara keseluruhan sehingga ketika mendapati sesuatu dia akan lebih cepat menghasilkan *action*. Gitu. Karena model berpikirnya sudah secara kompleks dibangun dan mengetahui apa yang harus dilakukan ketika menemukan sesuatu. Jadi tidak dilakukan dari awal secara terus-menerus.

---

## Sesi 9: Diskusi, Informasi Tugas Besar (Tubes), Presensi, dan Penutup (35:00 – 42:55)

**[35:00] [Dosen]:**
Oke, sampai sini ada yang mau ditanyakan nggak? Silakan kalau ada. Kalau nggak ada ya kayaknya materinya cukup satu *slide* [pertemuan] saja ya. Mau dua *slide*? Banyak. Silakan kalau ada yang mau ditanyakan, tanyakan.

**[35:55] [Dosen]:**
Jadi paling ini, ini kan pekan ke berapa? Minggu ke berapa? 10 ya? Minggu 10. Untuk presentasi tubes itu kita lakukan di minggu 15 dan 16. Jadi kalian punya waktu 4 minggu atau sebulan untuk menyelesaikan tubes-nya ya. Jadi jangan borongan dibikin H-3 hari menjelang presentasi. Lakukan dari sekarang.

**[36:35] [Dosen]:**
Sambil paralel terus kita ketemu, tapi kalau minggu depan perlu saya sampaikan depan saya nggak bisa masuk. Karena minggu depan kebetulan saya dimintai tolong ini ya ada lomba dulu.

**[36:55] [Dosen]:**
Jadi untuk minggu depan itu saja yang proposal singkat, jadi pakai aja ikutin *template* saja yang gampang biar halamannya nggak banyak. Kalau halamannya banyak saya juga malas bacanya. Jadi cukup ya 2 sampai 6 lembar gitu kan. Nah kalau untuk proposal kan paling cukup 2 lembar. Poin pentingnya aja ditulis, kecuali banyak gambar — kalau banyak gambar mungkin paling 3 lembar. Ya.

**[37:25] [Dosen]:**
Terus silakan dikirimkan ke grup WA saja jadi biar saling tahu ya apa yang dikerjakan kelompok lain jadi biar tidak ada yang sama. Tujuan saya kalian harus mengirim di grup WA biar... kecuali tugas yang sifatnya beda-beda kemarin ya. Itu kan tidak berkaitan dengan tubes. Biar paling konteks untuk kirimnya email. Tapi kalau terkait dengan tugas besar semuanya tolong di-*share* di WA saja. Jadi bisa memonitor: "Oh ini sama", berarti kalian cari suatu topik yang lain, jangan pada sama.

**[38:15] [Mahasiswa]:**
Pak, buat *tools* simulasi untuk tubes-nya ada ketentuan, Pak, harus *software* tertentu atau gimana?

**[38:25] [Dosen]:**
Nggak ada. Tapi saya sih *encourage* kalian pakainya Robot Operating System ya, pakai ROS saja. Karena itu akan jauh lebih mudah. Kalian bisa *bridging* juga. Asal jangan *full* pakai bot/paket *cloud* yang instan gitu ya *(terdengar seperti PyPot/Pipebot cloud)* terus tinggal *importing* / manggil saja tanpa paham prosesnya. Ya. Jadi tetap kalian harus memahami caranya seperti itu.

**[39:15] [Mahasiswa]:**
*(Diskusi ringan beberapa mahasiswa membahas pilihan software/simulator setelah sesi tanya jawab berakhir)*

**[40:10] [Dosen]:**
*(Melakukan presensi akhir kelas)*
Nataniel... Maheswara...

**[40:18] [Mahasiswa]:**
Hadir.

**[40:25] [Dosen]:**
*(Melanjutkan presensi)* ... Ya udah itu jadi minggu depan gunakan untuk buat proposal saja kemudian mulai *construct* untuk tubes-nya. Ya. Kita mulai lagi nanti setelah minggu depan.

**[40:45 – 42:55]**
*(Suara aktivitas akhir kelas dan diskusi mahasiswa hingga rekaman berakhir pada 42:55.)*
