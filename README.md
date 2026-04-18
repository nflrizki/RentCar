# RentCar

Aplikasi mobile React Native untuk layanan sewa mobil dan motor, dibangun dengan Expo dan Firebase.

## Fitur

- **Autentikasi Pengguna**: Fungsi pendaftaran dan masuk
- **Penelusuran Kendaraan**: Telusuri mobil dan motor yang tersedia untuk disewa
- **Layanan Lokasi**: Temukan kantor sewa dan dapatkan petunjuk arah
- **Sistem Pemesanan**: Sewa kendaraan dengan pemilihan tanggal
- **Riwayat Pemesanan**: Lihat sewa masa lalu dan saat ini
- **Profil Pengguna**: Kelola informasi pribadi
- **Integrasi Peta**: Lihat lokasi sewa di peta
- **Data Real-time**: Integrasi Firebase Firestore untuk data kendaraan

## Teknologi

- **Framework**: React Native dengan Expo (v47)
- **Navigasi**: React Navigation v6
- **Backend**: Firebase (Firestore, Authentication)
- **Peta**: React Native Maps dengan Google Places
- **Komponen UI**: Native Base, React Native Paper
- **Manajemen State**: React Class Components
- **Penyimpanan**: AsyncStorage untuk persistensi data lokal

## Persyaratan

- Node.js (v14 atau lebih tinggi)
- npm atau yarn
- Expo CLI
- Akun Firebase
- Android Studio atau Xcode (untuk pengujian perangkat)

## Instalasi

1. Clone repository:
```bash
git clone <repository-url>
cd RentCar
```

2. Install dependensi:
```bash
npm install
# atau
yarn install
```

3. Setup Firebase:
   - Buat proyek baru di [Firebase Console](https://console.firebase.google.com/)
   - Aktifkan Firestore Database
   - Aktifkan Authentication (Email/Password)
   - Ganti konfigurasi Firebase di `src/config/config.jsx` dengan kredensial Anda sendiri

4. Jalankan server development:
```bash
npm start
# atau
yarn start
```

## Menjalankan Aplikasi

### Di Web
```bash
npm run web
```

### Di Android
```bash
npm run android
```

### Di iOS
```bash
npm run ios
```

### Menggunakan Expo Go
1. Install Expo Go di perangkat mobile Anda
2. Scan QR code yang ditampilkan di terminal setelah menjalankan `npm start`

## Struktur Project

```
RentCar/
├── src/
│   ├── config/
│   │   ├── config.jsx      # Konfigurasi Firebase
│   │   ├── environments.ts # Variabel lingkungan
│   │   └── style.js        # Gaya global
│   └── screens/
│       ├── auth/
│       │   ├── signin.js   # Layar masuk
│       │   └── signup.js   # Layar pendaftaran
│       ├── splash.js       # Layar splash
│       ├── home.js         # Layar beranda dengan daftar kendaraan
│       ├── profile.js      # Layar profil pengguna
│       ├── history.js      # Layar riwayat pemesanan
│       ├── order.js        # Layar pesan/sewa kendaraan
│       ├── editProfile.js  # Layar edit profil
│       ├── location.js     # Layar lokasi/peta
│       └── officeloc.tsx   # Layar lokasi kantor
├── App.js                  # Komponen utama aplikasi dengan navigasi
├── app.json               # Konfigurasi Expo
├── package.json           # Dependensi dan script
└── babel.config.js        # Konfigurasi Babel
```

## Konfigurasi Firebase

Update `src/config/config.jsx` dengan kredensial proyek Firebase Anda:

```javascript
const firebaseConfig = {
  apiKey: "YOUR_API_KEY",
  authDomain: "YOUR_PROJECT.firebaseapp.com",
  projectId: "YOUR_PROJECT_ID",
  storageBucket: "YOUR_PROJECT.appspot.com",
  messagingSenderId: "YOUR_SENDER_ID",
  appId: "YOUR_APP_ID",
  measurementId: "YOUR_MEASUREMENT_ID"
};
```

## Script yang Tersedia

- `npm start` - Memulai server development Expo
- `npm run android` - Menjalankan di perangkat/emulator Android
- `npm run ios` - Menjalankan di perangkat/simulator iOS
- `npm run web` - Menjalankan di browser web

## Dependensi Utama

- `expo` - Framework React Native
- `firebase` - Layanan backend
- `@react-navigation/native` - Library navigasi
- `react-native-maps` - Integrasi peta
- `react-native-google-places-autocomplete` - Pencarian lokasi
- `native-base` - Library komponen UI
- `moment` - Penanganan tanggal/waktu
- `@react-native-async-storage/async-storage` - Penyimpanan lokal

## Lisensi

Proyek ini dilisensikan di bawah MIT License.

## Kontribusi

Kontribusi sangat welcome! Silakan kirim Pull Request.
