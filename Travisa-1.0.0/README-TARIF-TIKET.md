# Dokumentasi Halaman Tarif Tiket Terminal BMD Cilacap

## 📋 Struktur File Tarif Tiket

### File Utama
- **`tarif_tiket.html`** - Halaman utama dengan navigasi tab untuk semua provinsi
- **`tarif_banten.html`** - Halaman khusus untuk tarif ke Provinsi Banten  
- **`tarif_jakarta.html`** - Halaman khusus untuk tarif ke DKI Jakarta
- **`css/tarif-tiket-custom.css`** - File CSS kustom untuk styling

## 🎨 Desain dan Fitur

### 1. **Navigasi Tab Bootstrap** 
- Tab yang responsif dengan tema warna biru dan kuning
- Smooth transition dan hover effects
- Mobile-friendly dengan layout yang adaptif

### 2. **Card Design dengan Shadow**
- Card dengan shadow dan border radius untuk tampilan modern
- Header card dengan gradient background
- Hover effects untuk interaksi yang lebih baik

### 3. **Tabel Responsif**
- Tabel dengan styling khusus dan color coding
- Responsive table yang bisa di-scroll pada layar kecil
- Header tabel dengan background kuning sesuai tema

### 4. **Informasi Tambahan**
- Alert box dengan informasi penting
- Icon dan styling yang konsisten
- Breadcrumb navigation untuk navigasi yang jelas

## 📱 Responsivitas

### Desktop (>768px)
- Tab horizontal dengan spacing yang baik
- Tabel penuh dengan semua kolom terlihat
- Card layout yang optimal

### Tablet (768px - 576px)  
- Tab tetap horizontal tapi dengan font lebih kecil
- Tabel dengan scroll horizontal
- Padding yang disesuaikan

### Mobile (<576px)
- Tab berubah menjadi vertical stack
- Tabel dengan scroll horizontal
- Font size yang disesuaikan untuk readability

## 🔧 Cara Edit Data Tarif

### Mengedit Data di File Tab (tarif_tiket.html)
1. Buka file `tarif_tiket.html`
2. Cari section dengan id `banten` atau `jakarta`
3. Edit data di dalam `<tbody>` table
4. Format: `<tr><td>No</td><td>PO Bus</td><td>Kelas</td><td>Tujuan</td><td>Harga</td><td>Jam</td><td>Nomor Agen</td></tr>`

### Mengedit Data di File Terpisah
1. Buka `tarif_banten.html` atau `tarif_jakarta.html`
2. Cari section table dalam card
3. Edit data yang sama seperti di atas

### Menambah Provinsi Baru
1. **Di File Tab**: Tambahkan tab baru dan content di `tarif_tiket.html`
2. **File Terpisah**: Buat file baru berdasarkan template `tarif_banten.html`

## 🎯 Keuntungan Setiap Pendekatan

### ✅ **Pendekatan Tab (Recommended)**
**File**: `tarif_tiket.html`

**Keuntungan:**
- ✅ Satu halaman untuk semua data
- ✅ Loading lebih cepat (tidak perlu pindah halaman)  
- ✅ SEO friendly (semua content dalam satu halaman)
- ✅ Mudah untuk pencarian dalam halaman (Ctrl+F)
- ✅ Pengalaman pengguna yang lebih smooth

**Kapan Menggunakan:**
- Jika data tidak terlalu banyak (<50 baris per provinsi)
- Jika ingin tampilan yang lebih interaktif
- Jika prioritas adalah user experience

### ✅ **Pendekatan File Terpisah**
**File**: `tarif_banten.html`, `tarif_jakarta.html`

**Keuntungan:**
- ✅ Halaman lebih ringan per load
- ✅ Mudah untuk maintenance data per provinsi
- ✅ Bisa diakses langsung dengan URL spesifik
- ✅ Lebih mudah untuk tim yang mengelola data berbeda
- ✅ Bisa dioptimasi SEO per provinsi

**Kapan Menggunakan:**
- Jika data sangat banyak (>50 baris per provinsi)
- Jika ada tim terpisah yang mengelola data per provinsi
- Jika ingin SEO yang lebih spesifik per provinsi
- Jika ada rencana menambah banyak provinsi

## 📊 Rekomendasi Berdasarkan Kebutuhan

### **Untuk Website Terminal BMD Cilacap Saat Ini:**

**🏆 PILIH PENDEKATAN TAB** karena:
1. **Data masih manageable** (32 baris Banten + 20 baris Jakarta = 52 total)
2. **User experience lebih baik** - tidak perlu loading halaman baru
3. **Maintenance lebih sederhana** - hanya 1 file untuk diupdate
4. **Loading lebih cepat** - semua data sudah loaded

### **Jika di Masa Depan:**
- **Data bertambah >100 baris per provinsi** → Pindah ke file terpisah
- **Ada >5 provinsi** → Pindah ke file terpisah  
- **Ada tim terpisah per provinsi** → Gunakan file terpisah

## 🛠️ Cara Menggunakan

### Menggunakan Pendekatan Tab
1. Hapus file `tarif_banten.html` dan `tarif_jakarta.html`
2. Gunakan hanya `tarif_tiket.html`
3. Update menu dropdown di navbar untuk menghapus link sub-menu

### Menggunakan Pendekatan File Terpisah  
1. Update file `tarif_tiket.html` untuk menampilkan ringkasan dan link ke file detail
2. Gunakan `tarif_banten.html` dan `tarif_jakarta.html` sebagai halaman detail
3. Update menu navbar untuk menambahkan sub-menu

## 🎨 Customization CSS

File `css/tarif-tiket-custom.css` berisi:
- **Tab styling** dengan warna tema website
- **Card effects** dan shadows
- **Table styling** dengan color coding
- **Responsive breakpoints** untuk mobile
- **Print styles** untuk pencetakan
- **Animation effects** untuk transisi

### Mengubah Warna Tema
```css
/* Primary color (biru) */
--primary-color: #0d6efd;

/* Warning color (kuning) */  
--warning-color: #ffc107;
```

## 📋 Checklist Maintenance

### Mingguan
- [ ] Cek apakah ada perubahan jadwal
- [ ] Update harga jika ada perubahan
- [ ] Verifikasi nomor telepon agen

### Bulanan  
- [ ] Review data yang tidak aktif
- [ ] Update informasi kontak jika berubah
- [ ] Cek responsivitas di berbagai device

### Tahunan
- [ ] Review struktur halaman
- [ ] Evaluasi performa loading
- [ ] Pertimbangkan penambahan fitur baru

## 🚀 Future Enhancements

1. **Search & Filter Functionality**
   - Pencarian berdasarkan tujuan
   - Filter berdasarkan harga
   - Filter berdasarkan waktu keberangkatan

2. **Interactive Features**
   - Sort tabel berdasarkan kolom
   - Export data ke PDF/Excel
   - Print-friendly view

3. **Integration**
   - API untuk update real-time
   - Integration dengan sistem booking
   - WhatsApp integration untuk kontak agen

---

**💡 Kesimpulan**: Untuk saat ini, **gunakan pendekatan TAB** karena lebih sesuai dengan kebutuhan dan memberikan user experience yang lebih baik. File terpisah bisa dipertimbangkan jika data bertambah significantly di masa depan.