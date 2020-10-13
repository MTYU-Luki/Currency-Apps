# Currency Apps
Aplikasi ini mencakup fungsi perhitungan ilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp. 15.000

## Scope & Functionalities
- User dapat memasukan angka
- User dapat menyentuh tombol hitung
- User mendapatkan info "INVALID" jika yang dimasukan berupa text

## How Does it works?
Diawali dari method MainWindows pada class `MainWindows.Xaml.cs`, kita mendeklarasikan

```csharp
public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
```

logika perhitungan terdapat pada class `CurencyController.cs` sebagai berikut
berikut cara kerjanya

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```