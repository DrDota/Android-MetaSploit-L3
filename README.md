## Decompile and Recompile An android APK 🧰

Ghasd darim yek app ra decompile karde va pas az tazrigh metasploit dobare recompile konim 

$ bad az sakht metasploit tebgh ravesh gofte shode dar `Android-MetaSploit-L1` 2 kar zer ra bayad anjam dahim

```bash
apktool d /home/kali/Dekstop/app.apk
```

```bash
apktool d /home/kali/Dekstop/app.apk
```

har 2 app ra decompile mikonim


## Install apktool ⬇️

abzar "apktool" b sorat pishfarz dar kali linux nasb nist va b shekl zer eghdam b nasb namaed

```bash
sudo apt install apktool
```

$ bar roye joft poshe haye decompile shode app ha ras click karde va gozine `open as Root` ra mizanim ta baz shavand

### 3 kar ra bayad anjam dahim

1. **Jaygozine metasploit** Poshe "metasploit" ra az app alode dar address `smali > com > metasploit` dar hamin address dar app asli jaygozin mikonim 
2. **Edit AndroidManifest.xml** bar roye har 2 file `AndroidManifext.xml` click rast karde va `Open With "MousePad" ra mizanim va karhaye zer ra anjam midahim

```text
- copy ebeart ro b ro az "rat" b "app"        <uses-permission android:""/>

```
4. **Credentials** configured - This can be done manually or by running the `make setup` command from the root of this repo
