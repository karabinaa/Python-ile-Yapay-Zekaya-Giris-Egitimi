# 1 - Miniconda Kurulumu

## Windows için Miniconda Kurulumu

### 📥 Adım 1: Miniconda Yükleyicisini İndirme

- [Miniconda İndirme Sayfası](https://www.anaconda.com/download/success) adresine gidin.
- İşletim sisteminize uygun olan **Miniconda Windows Installer**'ı indirin (64-bit önerilir).

### 🛠️ Adım 2: Miniconda’yı Kurma

1. İndirilen `.exe` dosyasını çalıştırın.
2. Lisans sözleşmesini kabul edin.
3. "Just Me" seçeneğini işaretleyin ve **Next** butonuna tıklayın.
4. Kurulum dizinini seçin (varsayılan dizin önerilir).
5. **"Add Miniconda3 to my PATH environment variable"** seçeneğini **işaretleyin** (Bu adım isteğe bağlıdır, ancak conda’yı komut satırından kullanmayı kolaylaştırır).
6. **"Register Miniconda3 as the default Python"** seçeneğini **işaretleyebilirsiniz** (varsayılan Python olarak ayarlanmasını sağlar).
7. **Install** butonuna tıklayarak kurulumu tamamlayın.

### ✅ Adım 3: Miniconda’yı Doğrulama

Kurulumu doğrulamak için Komut İstemi'ni açın ve aşağıdaki komutları çalıştırın:

```sh
conda --version
python --version
```

Eğer sürüm bilgilerini görüyorsanız kurulum başarılıdır.

### PATH Değişkenini Manuel Olarak Ayarlama

Eğer `conda` komutu çalışmıyorsa, Miniconda’nın yüklü olduğu dizini PATH değişkenine ekleyin.
Windows’ta PATH değişkenine Miniconda dizinini eklemek için şu adımları izleyin:

1. **Başlat Menüsü**'ne gidin ve "Gelişmiş sistem ayarlarını görüntüle" yazıp açın.
2. Açılan pencerede **Ortam Değişkenleri (Environment Variables)** butonuna tıklayın.
3. **Sistem değişkenleri (System Variables)** bölümünde **Path** değişkenini seçip **Düzenle (Edit)** butonuna tıklayın.
4. **Yeni (New)** butonuna tıklayarak aşağıdaki yolu ekleyin:
   ```
   C:\Users\<kullanıcı_adınız>\Miniconda3\Scripts
   ```
5. **Tamam (OK)** butonuna basarak tüm pencereleri kapatın.
6. Komut İstemi'ni yeniden başlatarak aşağıdaki komutu çalıştırarak ayarın uygulandığını doğrulayın:
   ```sh
   conda --version
   ```
---

## macOS için Miniconda Kurulumu

### 📥 Adım 1: Miniconda Yükleyicisini İndirme

- [Miniconda İndirme Sayfası](https://www.anaconda.com/download/success) üzerinden **macOS (Intel veya Apple Silicon)** için uygun sürümü indirin.
- `.pkg` veya `.sh` uzantılı yükleyiciyi seçin.

### 🛠️ Adım 2: Terminal Üzerinden Kurulum

- `.sh` dosyası indirdiyseniz Terminal'i açıp aşağıdaki komutu çalıştırın:

```sh
bash Miniconda3-latest-MacOSX-x86_64.sh  # Intel için
bash Miniconda3-latest-MacOSX-arm64.sh  # Apple Silicon için
```

- Lisans sözleşmesini onaylayın (`yes` yazıp Enter'a basın).
- Kurulum dizini seçin (varsayılan önerilir).
- `conda init` komutunu çalıştırarak Miniconda’yı kabuk ortamınıza entegre edin.

### ✅ Adım 3: Miniconda’yı Doğrulama

Terminal’de aşağıdaki komutları çalıştırın:

```sh
conda --version
python --version
```

Eğer sürüm bilgilerini görüyorsanız kurulum başarılıdır.


### PATH Değişkenini Manuel Olarak Ayarlama

Eğer `conda` komutu çalışmıyorsa, Miniconda’nın yüklü olduğu dizini PATH değişkenine ekleyin.

Terminal’de aşağıdaki komutu çalıştırarak `~/.bashrc` veya `~/.zshrc` dosyanıza Miniconda'nın yolunu ekleyin:

```sh
echo 'export PATH="~/miniconda3/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```


---

## Linux için Miniconda Kurulumu

### 📥 Adım 1: Miniconda Yükleyicisini İndirme

- [Miniconda İndirme Sayfası](https://www.anaconda.com/download/success) üzerinden **Linux** için uygun sürümü indirin.
- Genellikle `.sh` uzantılı yükleyici tercih edilir.

### 🛠️ Adım 2: Terminal Üzerinden Kurulum

İndirilen dosyanın bulunduğu dizine gidip şu komutu çalıştırın:

```sh
bash Miniconda3-latest-Linux-x86_64.sh
```

- Lisans sözleşmesini kabul etmek için `yes` yazın.
- Kurulum dizinini seçin (varsayılan önerilir).
- `conda init` komutunu çalıştırarak Miniconda’yı kabuk ortamınıza entegre edin.

### ✅ Adım 3: Miniconda’yı Doğrulama

Kurulumu doğrulamak için aşağıdaki komutları çalıştırın:

```sh
conda --version
python --version
```

### PATH Değişkenini Manuel Olarak Ayarlama

Eğer `conda` komutu çalışmıyorsa, Miniconda’nın yüklü olduğu dizini PATH değişkenine ekleyin.

**Windows:**

- `C:\Users\<kullanıcı_adınız>\Miniconda3\Scripts` dizinini `PATH` değişkenine ekleyin.

**macOS/Linux:** Terminal’de aşağıdaki komutu çalıştırarak `~/.bashrc` veya `~/.zshrc` dosyanıza Miniconda'nın yolunu ekleyin:

```sh
echo 'export PATH="~/miniconda3/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

## 2. Conda ortamı oluşturma

Yeni bir conda ortamı oluşturup Jupyter dahil gerekli paketleri yüklemek için aşağıdaki adımları takip edebilirsiniz:

### 📌 Adım 1: Yeni Conda Ortamı Oluşturma

```sh
conda create --name yapayzeka python=3.9
```

Oluşturulan ortamı etkinleştirmek için:

```sh
conda activate oyk25
```

### 🛠️ Adım 2: Gerekli Kütüphaneleri Kurma

```sh
conda install numpy pandas scikit-learn matplotlib keras jupyter
```

### ✅ Adım 3: Jupyter Notebook’u Başlatma

```sh
jupyter notebook
```



