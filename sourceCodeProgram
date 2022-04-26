# Mengambil inputan plaintext (setiap karakter, diconvert menjadi huruf kapital)
plaintext = input("Plaintext: ").upper()
ptlen = len(plaintext)

# Mengambil key yang valid (semua huruf, setidaknya memiliki panjang 3)
key = ""
while not key.isalpha() or len(key) < 3:
    key = input("Key: ").upper()
keylen = len(key)

# Membuat keytext (membuat keytext lebih panjang dari yang diinginkan, kemudian ditrim)
keytext = key * (ptlen // keylen + 1)
keytext = keytext[:ptlen]

# Menentukan value pada enkripsi
alphabet = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
ciphertext = ""
# melakukan looping pada setiap karakter di plaintext dan keytext sejumlah length
for i in range(ptlen):
    # jika karakter adalah huruf -- dienkripsi
    if plaintext[i] in alphabet:
        # menjumlah plaintext dan values pada key
        # (offshift 1 untuk index)
        ptval = alphabet.find(plaintext[i]) + 1
        ktval = alphabet.find(keytext[i]) + 1
        newval = ptval + ktval
        # melakukan pengurangan apabila value terlalu besar
        if newval > 26:
            newval -= 26
        # menentukan karakter baru (offshift 1 untuk index)
        ciphertext += alphabet[newval - 1]
    # karakter bukan huruf -- diskip
    else:
        ciphertext += plaintext[i]

# menampilkan pesan yang sudah dienkripsi
print("Pesan yang sudah dienkripsi adalah '{}'.".format(ciphertext))
