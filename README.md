# Robotics & Controlled System (CEH4C3)

Repositori ini berisi seluruh materi perkuliahan, penugasan, telaah literatur ilmiah, dokumen Capstone Design pendukung, serta proyek tugas besar (Tubes) untuk mata kuliah **Robotics and Intelligent System (CEH4C3)** - Program Studi S1 Teknik Komputer, Fakultas Teknik Elektro, Universitas Telkom.

---

## 📁 Struktur Direktori

```text
Robotic & Controlled System/
├── Assesment 1/              # Telaah paper dan FGD Perakitan Robotik (Robotic Assembly)
├── Assesment 2/              # Telaah komprehensif strategi kontrol manipulator robot
├── Dokumen Capstone Design/  # Dokumen CD-1 & CD-2: Studi kasus irigasi kebun jeruk limau Ciberes, Subang
├── Materi/                   # Bahan ajar kuliah (Lecture 1a s/d Lecture 9, 15 file format .ppsx)
├── Tubes Robot/              # Tugas Besar: Dual-Arm Mobile Robot (Navigasi A* & IK 2-DoF) untuk Penyiraman Presisi
└── README.md
```

---

## 📑 Rincian Konten

### 1. `Assesment 1`
* **Paper Rujukan:** *Recent progress and challenges of key technologies in robotic assembly* (Longhui Qin, *Chinese Journal of Mechanical Engineering*, 2026).
* **Dokumen Laporan:** [Assesment Robotika dan sistem cerdas.pdf](Assesment%201/Assesment%20Robotika%20dan%20sistem%20cerdas.pdf)
* **Fokus:** Persepsi sensor (visual 2D/3D, F/T, taktil, fusi multimodal), jenis *end-effector*, strategi kontrol kontak, pembelajaran robot (*LfD, LfI/RL, Sim2Real*), metrik evaluasi, serta hasil Focus Group Discussion (FGD).

### 2. `Assesment 2`
* **Paper Rujukan:** *In-Depth Review of Advanced Control Strategies and Cutting-Edge Trends in Robot Manipulators* (Sherif I. Abdelmaksoud, dkk. - *IEEE Access*, 2024).
* **Dokumen Laporan:** [Assesment Robotika 2.pdf](Assesment%202/Assesment%20Robotika%202.pdf)
* **Fokus:** Pemodelan dinamika tautan (*rigid, flexible, rigid-flexible, multi-link*), 7 kerumitan matematis manipulator, metode kontrol modern (*SMC, LQR, ZNN, Observer-based, RL*), tren riset, serta identifikasi *research gap*.

### 3. `Dokumen Capstone Design`
* **Dokumen:**
  * [CD 1 - Analisis Permasalahan](Dokumen%20Capstone%20Design/CD%201%20-%20ANALISIS%20PERMASALAHAN%20PENYIRAMAN%20MANUAL%20PADA%20KEBUN%20JERUK%20LIMAU%20DI%20CIBERES%20SUBANG.pdf)
  * [CD 2 - Spesifikasi & Batasan Desain](Dokumen%20Capstone%20Design/CD%202%20-%20ANALISIS%20PERMASALAHAN%20PENYIRAMAN%20MANUAL%20PADA%20KEBUN%20JERUK%20LIMAU%20DI%20CIBERES%20SUBANG.pdf)
* **Fokus:** Analisis permasalahan penyiraman manual pada kebun jeruk limau (*Citrus amblycarpa*) di Desa Ciberes, Subang (~3.000 m², 500–600 pohon) serta penetapan batasan rekayasa (`C-01`–`C-05`) dan spesifikasi kuantitatif sistem irigasi (`S-01`–`S-14`).

### 4. `Materi`
* Seluruh slide presentasi interaktif dosen dari pertemuan awal hingga akhir (15 file `.ppsx`):
  * Lecture 1 (`1a`–`1d_2`): *Introduction to Robotics, Position & Orientation, Manipulator & Mobile Robot*
  * Lecture 2: *Basic Translation and Rotation Dynamics*
  * Lecture 3: *Kinematics (Links & Joints, D-H, Forward & Inverse)*
  * Lecture 4: *Path and Trajectory Planning*
  * Lecture 5 (`5a`–`5c`): *Robot Autonomy (Differential Drive, Perception & Vision, Paradigms)*
  * Lecture 6: *Robot Navigation (Topological, Bug, Grid-based A\*)*
  * Lecture 7: *Localization and Mapping (Kalman/Particle Filters, Occupancy Grid, SLAM)*
  * Lecture 8: *Multi Robot System & Swarm Robotics*
  * Lecture 9: *Start a Robotic Project / ROS*

### 5. `Tubes Robot`
* **Topik Resmi:** *Shortest Path Implementation on Robotic*
* **Judul Proyek:** Perancangan dan Simulasi Dual-Arm Mobile Robot untuk Navigasi Jalur Terpendek dan Penyiraman Presisi pada Perkebunan Jeruk Limau
* **Integrasi:** Menyelaraskan implementasi algoritma *Shortest Path* (A*) pada *Differential Drive Mobile Base* dan kinematika balik (*Inverse Kinematics*) *Dual-Arm* 2-DoF dengan studi kasus kebun jeruk limau Ciberes, Subang pada `Dokumen Capstone Design`.
* **Dokumen:**
  * [Laporan_Tahap_1_Perencanaan_Sistem.docx](Tubes%20Robot/Laporan_Tahap_1_Perencanaan_Sistem.docx) ([.pdf](Tubes%20Robot/Laporan_Tahap_1_Perencanaan_Sistem.pdf) | [.md](Tubes%20Robot/Laporan_Tahap_1_Perencanaan_Sistem.md))
  * [Resume_Diskusi_Tubes_Robotika.docx](Tubes%20Robot/Resume_Diskusi_Tubes_Robotika.docx) ([.pdf](Tubes%20Robot/Resume_Diskusi_Tubes_Robotika.pdf))
