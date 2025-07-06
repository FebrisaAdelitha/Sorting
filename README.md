# Sorting
# Fungsi untuk mengurutkan daftar produk menggunakan bubble sort
def bubble_sort(products):
    n = len(products)
    # Melakukan iterasi untuk setiap elemen dalam daftar
    for i in range(n):
        # Melakukan perbandingan elemen yang berdekatan
        for j in range(0, n-i-1):
            # Jika elemen saat ini lebih besar dari elemen berikutnya, tukar
            if products[j]['harga'] > products[j+1]['harga']:
                products[j], products[j+1] = products[j+1], products[j]

# Contoh daftar produk
produk = [
    {'nama': 'Produk A', 'harga': 15000},
    {'nama': 'Produk B', 'harga': 10000},
    {'nama': 'Produk C', 'harga': 20000},
    {'nama': 'Produk D', 'harga': 12000}
]

# Menampilkan daftar produk sebelum diurutkan
print("Sebelum diurutkan:")
for p in produk:
    print(f"{p['nama']} - Harga: {p['harga']}")

# Mengurutkan daftar produk
bubble_sort(produk)

# Menampilkan daftar produk setelah diurutkan
print("\nSetelah diurutkan:")
for p in produk:
    print(f"{p['nama']} - Harga: {p['harga']}")
