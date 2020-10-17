# The Cashier
Aplikasi ini mencakup perhitungan penjumlahan 
dan perkalian untuk menghitung harga barang 
yang akan di beli maupun jasa, barang atau jasa 
yang sudah di inputkan dan sudah di jumlahkan 
maupun di kalikan akan masuk pada data list.


# Scope & Functionalities

- User dapat menginputkan huruf/angka
- User dapat menyentuh tombol opsi pilihan barang/jasa
- User dapat menambahkan barang/jasa
- User dapat melihat data list yang sudah di inputkan 

# How Does it Works
Diawali dari method `MainWindow` pada class MainWindow.xaml.cs,
kita mendeklarasikan Calculator untuk membuat controllernya dan membuat fungsi fungsinya

```java
 public MainWindow()
        {
            InitializeComponent();
            calculator = new Calculator();
            listBox.ItemsSource = calculator.getListItem();
        }
```
Logika perhitungan terdapat pada class `Item.cs` cara 
kerjanya jumlah barang yang di inputkan akan dikalikan dengan harga lalu di jumlahkan dengan barang selanjutnya nanti akan ketemu subtotal/jumnlah harga
```javascript
public double getSubTotal()
        {
            subtotal = price * quantity;
            return subtotal;
        }
```