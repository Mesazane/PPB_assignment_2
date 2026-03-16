# Flutter Application - My First App

## Widget Tree

```
main()
└── MyApp (StatelessWidget)
    └── MaterialApp
        └── RowColumnPage (StatelessWidget)
            └── Scaffold
                ├── AppBar
                │   └── Text("My First App")
                └── body: Column
                    ├── Container (AspectRatio - Image)
                    │   ├── AspectRatio
                    │   └── Image.network
                    ├── Container (Text)
                    │   └── Text("What image is that")
                    ├── Container (Row - Icons)
                    │   └── Row
                    │       ├── Column
                    │       │   ├── Icon(Icons.food_bank)
                    │       │   └── Text("Food")
                    │       ├── Column
                    │       │   ├── Icon(Icons.landscape)
                    │       │   └── Text("Scenery")
                    │       └── Column
                    │           ├── Icon(Icons.people)
                    │           └── Text("People")
                    └── CounterCard (StatefulWidget)
                        └── Container
                            └── Row
                                ├── Text (Counter value)
                                └── IconButton (Add)
```

## Deskripsi Widget

### MyApp (StatelessWidget)
Root widget aplikasi yang membungkus seluruh aplikasi dengan `MaterialApp`.
- **Fungsi**: Mendefinisikan tema aplikasi dan konfigurasi global
- **Properti utama**:
  - `title`: 'Flutter Demo' - judul aplikasi
  - `theme`: Menggunakan `ColorScheme.fromSeed` dengan `Colors.deepPurple`
  - `useMaterial3`: `true` - menggunakan Material Design 3
  - `home`: `RowColumnPage` - halaman utama aplikasi

### RowColumnPage (StatelessWidget)
Halaman utama yang menampilkan layout dengan kombinasi Row dan Column.
- **Fungsi**: Menampilkan konten utama aplikasi dengan berbagai layout widget
- **Properti utama**:
  - `Scaffold`: Menyediakan struktur dasar halaman dengan AppBar dan body
  - `AppBar`: Bar berjudul "My First App" dengan background warna orange
  - **Body** terdiri dari 4 bagian:
    1. **Container dengan AspectRatio dan Image**: Menampilkan gambar dari network (https://picsum.photos/200) dengan rasio aspek 1:1
    2. **Container Text**: Menampilkan teks "What image is that" dengan background pink
    3. **Container dengan Row**: Menampilkan 3 kategori (Food, Scenery, People) dengan icon dan label, di-arrange secara horizontal dengan `Row`
    4. **CounterCard**: Widget counter yang interaktif (StatefulWidget)

### CounterCard (StatefulWidget)
Widget yang menampilkan counter interaktif dengan tombol untuk menambah nilai.
- **Fungsi**: Mendemonstrasikan penggunaan StatefulWidget dan state management dengan `setState`
- **State**:
  - `_counter`: Integer yang menyimpan nilai counter, dimulai dari 0
- **Method**:
  - `_incrementCounter()`: Meningkatkan nilai `_counter` ketika tombol ditekan
- **UI Layout**:
  - `Container`: Background dengan warna cyan
  - `Row` dengan dua elemen:
    1. **Text**: Menampilkan nilai counter saat ini
    2. **Icon Button**: Tombol dengan icon plus (`Icons.add`) untuk meningkatkan counter
  - Menggunakan `MainAxisAlignment.spaceBetween` untuk spacing antar elemen

## Fitur Utama
- ✅ Layout responsif menggunakan Row dan Column
- ✅ Penggunaan MediaQuery untuk ukuran layar dinamis
- ✅ StatelessWidget dan StatefulWidget
- ✅ State management dengan setState
- ✅ Implementasi Theme Material Design 3
