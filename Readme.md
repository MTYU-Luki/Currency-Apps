# Currency Apps
Aplikasi ini mencakup fungsi perhitungan ilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp. 15.000

## Scope & Functionalities
- User dapat memasukan angka
- User dapat menyentuh tombol hitung
- User mendapatkan info "INVALID" jika yang dimasukan berupa text

## How Does it works?
Diawali dari method MainWindows pada class `MainWindows.Xaml.cs`, Lengkapnya sebagai berikut;

```csharp
public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
```

logika perhitungan terdapat pada class `CurencyController.cs` sebagai berikut cara kerjanya;

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```

# Latihan
1. Review kembali percobaan 1 sampai dengan 3 dengan menjawab pertanyaan-pertanyaan pada latihan tersebut.
2. Mengapa perlu membuat class CurrencyController.cs pada percobaan 4 ?
3. Jelaskan kegunaan method isAllowed pada percobaan 4!
4. Jelaskan secara singkat mengenai Regex pada percobaan 4!
5. Buatlah class diagramnya pada percobaan 4! 


# Jawaban No 1
- pada percobaan 1, jika kita memasukan angka berapapun pada textbox kemudian kita klik button hitung, maka yang akan keluar adalah sama seperti angka yang kita masukan
- Percobaan 2, jika kita memasukan sebarang angka pada textbox dan kita klik button hitung maka angka tersebut akan dikalikan 15000 `(var result = nominalDouble * 15000;)`, dan jika kita  memasukan sembarang huruf pada textbox maka akan terjadi carsh, karena kita baru membuat fugsi yang bisa meghitung angka.
- Percobaan 3, sama seperti percobaan 2 , cuma yang membedakan jika kita memasukan huruf ke text box akan menampilkan kalimat "INVALID" karena kita sudah menambahkan fugsi jika kita memasukan huruf.

# Jawabn No 2
- Untuk memisah logika/ fungsi dari perhitungan matematika `CurencyController.cs` dan logika untuk mengontrol tampilan `Mainwindows.xaml.cs`

# Jawaban No 3
- Untuk megizinkan dari inputtextbox, jika yang diinputkan angka maka akan menjalankan fungsi matematic dan jika yang diinputkan huruf maka akan mengembalikan "INVALID" karena tidak diizinkan.

# Jawaban No 4
- Fungsi Regex adalah mencari suatu pola spesifik dari fungsi `Regex("[^0-9,-]+");`

# Jawaban No 5
