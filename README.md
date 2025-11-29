Hoşlandığım kız için yaptığım proje Seni Çok Seviyorum Beril <3
---

## 🛠️ Derleme ve Çalıştırma Gereksinimleri

Bu projeyi derlemek ve çalıştırmak için aşağıdaki araçlara ihtiyacınız olacaktır:

### 1. Sistem Gereksinimi
* **Linux** tabanlı bir işletim sistemi.

### 2. Derleyici (Assembler)
* Sisteminizde kurulu bir **Assembler** (çevirici).
    * **fasm** veya **nasm** önerilir.
    * İleride **gas** (GNU Assembler) desteği de eklenecektir.

### 3. Opsiyonel: USB Bellek
* Projenin ikili dosyasını (binary) doğrudan çalıştırmak için **USB bellek**.

### 4. Çalıştırma Ortamı (Emülatör/Sanal Makine)
Projenin **ikili dosyasını** çalıştırmak için aşağıdaki emülatör veya sanal makinelerden herhangi birini kullanabilirsiniz:

* **Qemu**
* **Bochs**
* **VMware**
* **VirtualBox**
* **Alternatif:** Ayrıca `copy.sh/v86` adresi üzerinden de çalıştırabilirsiniz.

---

## 🚀 Başlangıç

### Adım 1: Assembler Kurulumu

Derleme ve çalıştırma işlemi için Fasm (Flat Assembler) veya Nasm (Netwide Assembler) kullanmanız önerilir.
Kurmak için:

### Debian (nasm)
```bash
sudo apt install nasm
```
### Debian (fasm)
```bash
sudo apt install fasm
```

### Arch Linux (nasm)
```bash
sudo pacman -S nasm
```
### Arch Linux (fasm)
```bash
sudo pacman -S fasm
```

### Diğer dağıtımlar:

[Nasm](https://pkgs.org/search/?q=nasm)
[Fasm](https://pkgs.org/search/?q=fasm)

### Adım 2: Projeyi Derleme ve Çalıştırma
Projeyi klonlayalım dizin ve içine girelim:

```bash
git clone https://github.com/developer-kenan/BeriliumOs.git
cd BeriliumOs
```

Fasm syntax ile derlemek için:

```bash
cd fasm_syntax
fasm beril.asm beril.bin
dd if=beril of=beril.img
```

Nasm syntax ile derlemek için:

```bash
cd nasm_syntax
nasm -f bin beril.asm -o beril
dd if=beril of=beril.img
```

## Tersine mühendislik
### (Proje zaten açık kaynak kodlu ama siz bilirsiniz)

### Nasm:

```bash
ndisasm beril
```

### Fasm:

```bash
xxd beril.bin
```

Veya:

```bash
hexdump -C beril.bin
```

