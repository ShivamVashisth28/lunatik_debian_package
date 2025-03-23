###  Lunatik Debian Package  

Lunatik is a framework for scripting the Linux kernel with Lua. This repository contains the `.deb` package for installing Lunatik on Debian-based Linux distributions (e.g., Ubuntu).  

---

##  Installation  

###  Download the `.deb` Package  
Clone this repository or manually download the `.deb` file from the **Releases** section.  

```bash
git clone git@github.com:ShivamVashisth28/lunatik_debian_package.git
cd lunatik_debian_package
```

###  Install the Package  
Run the following command to install Lunatik:  

```bash
sudo dpkg -i lunatik_*.deb
```

If you encounter missing dependencies, run:  

```bash
sudo apt --fix-broken install
```

---

##  Usage  

After installation, you can verify that Lunatik is working by running:  

```bash
sudo lunatik
```

To test a Lua script inside the kernel, you can load a sample script:  

```lua
print("Hello from Lunatik!")
```

For advanced use cases, check out the `examples/` directory for sample Lua scripts.

---

##  Uninstallation  

To remove Lunatik from your system, use:  

```bash
sudo apt remove --purge lunatik
sudo apt autoremove
```

If the command still launches `lunatik`, check for any remaining binaries:  

```bash
which lunatik  # Locate the binary path
sudo rm -f /usr/bin/lunatik  # Remove it manually if needed
```

---
