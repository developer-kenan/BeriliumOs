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

Öncelikle Linux sisteminize yukarıda belirtilen assembler'lardan (örneğin fasm veya nasm) birini kurun.

### Adım 2: Projeyi Derleme ve Çalıştırma

öncelikle nasm veya fasm kurmalısınız nasm için debian sistemlerde sudo apt install nasm 
fasm içinde sudo apt install fasm yazmanız yeter öncelikle BeriliumOs klasörüne cd ile giriyoruz sonra fasm_syntax sa isteyen nasm_syntax a da girebilir
fasm syntax i derlemek için 
fasm beril.asm beril.bin
sonra dd if=beril of=beril.img yazıp imaj dosyasını alabilirsiniz
nasm için de
cd nasm_syntax yapıp sonra
nasm -f bin beril.asm -o beril
dd if=beril of=beril.img yaparak imaj dosyasını alabilirsiniz
## Reverse Engineering
ndisasm beril yaparak (nasm için)
fasm içinde xxd veya hexdump kullanabilirsiniz
xxd beril.bin
veya
hexdump -C beril.bin yapabilirsiniz.
