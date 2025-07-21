# r8125-UbuntuFix

## DKMS Driver for Linux

### 📌 Purpose:

This is a driver for **Realtek RTL8125/8125B/8125BG/8125BGS/8125B-CG** network adapters to work properly on Linux distributions.

### 📥 Source:

The source code was **downloaded from the official Realtek website** and adapted for compatibility with newer Linux kernels.

---

## ✅ Requirements:

* **OS**: Linux (Ubuntu, Debian, Arch, Fedora, etc.)
* **Kernel**: 4.15 or higher (tested on 6.11)
* **Permissions**: root (or `sudo`)
* **Dependencies**:

  * `dkms`
  * `build-essential`
  * `linux-headers-$(uname -r)`
  * `make`, `gcc`, `perl`

---

## 🚀 Installation:

```bash
git clone https://github.com/Mirik9724/r8125-UbuntuFix.git
cd r8125-UbuntuFix
sudo make
```

---

## 🔍 Verifying Installation:

```bash
sudo modprobe r8125
ip a | grep enp
```

If you see an interface like `enpXs0` (or `r8125`), the driver is working correctly.

---

## 🔄 Automatic Kernel Support:

Thanks to **DKMS**, the driver automatically rebuilds after kernel updates.

---

## ❌ Uninstall:

```bash
sudo dkms remove r8125/9.011.00 --all
```

---

## 📝 Notes:

* A reboot may be required after installation.
* Compatible with many distributions, including Ubuntu, Debian, Arch Linux, and derivatives.
* No need for manual rebuilding after kernel upgrades.
