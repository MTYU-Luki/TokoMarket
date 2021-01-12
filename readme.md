## Nama : Luki Fiagnia Saputra
## Nim : 19.11.2729
## kelas : Infomatika 03

# TokoMarket

## 1. Penjelasan 
Sebuah Aplikasi Toko market yang bisa memasukan pesanan, menambahkan promo dll.

## 2. penjelasan program
dimulai dari class `Menu.xaml.cs` dan `Menu.xaml` berguna untuk menampilkan daftar menu, 
`Promo.Xaml` dan `Promo.xaml.cs` berguna untuk menampilkan daftar promo.

```csharp
public void updateTotal(double subTotal, double promo)
        {

            double total = subTotal - promo;
            this.paymentListener.onPriceUpdated(subTotal, total, promo);

        }
```
berguna untuk mengupdate total bayar jika kita menggunakan promo maka total pembayaran akan di potong promo yang di pakai

```csharp
 public void addItem(Item item)
        {
            this.itemkeranjangBelanja.Add(item);
            this.onKeranjangBelanjaChangedListener.addItemSucceed();
            calculateSubTotal();
        }
```
fungsi yang digunakan untuk menambahkan item ke kranjang belanja dari daftar belanja

```csharp
 public List<Item> getItems()
        {
            return this.itemkeranjangBelanja;
        }

 public List<Diskon> getDiskon()
        {
            return this.diskonDipakai;
        }
```
mengambil daftr list pada item dan diskon

## 3. Class Diagram 
### Coupon With OCP
![alt text](https://github.com/MTYU-Luki/TokoMarket/blob/master/ClassDiagram1.png)
