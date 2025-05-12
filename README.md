

## A feladat során a vizsgázónak szerverek és munkaállomások beállítását kell elvégeznie. Mind a Windows, mind a Linux szervert érintve.

**Tantárgy:** Szerverek és felhőszolgáltatások  
**Vizsgázó neve:** _______________________________  
**Dátum:** _______________________________

**Instrukciók:**

- A dolgozat során csak a megadott hálózati tartományt és konfigurációs beállításokat használja.
- A vizsga teljes időtartama:  -

## !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
## Használható eszközök:
- Linux segédlet

bármely más eszköz használata, a vizsgáról való azonnali kizárással jár!
## !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

---

### 0. VirtualBox konfiguráció és telepítés 

a. Hozzon létre egy virtuális környezetet, amely biztosítja a szerver és a kliensgépek megfelelő működését. (meghajtók, hálókátyák)  
b. Használja a megfelelő lemezképfájlokat  
- Végezze el a telepítést és az alapvető beállításokat

# Windows Szerver:

### 1. Windows konfiguráció
- A jelszó legyen "Teszt1234_"
- A szerver neve legyen: „TesztWindows”.
- A szerver IP-címe a hálózat utolsó kiosztható címe legyen. 
- A szerveren az elsődleges DNS a 8.8.8.8, a másodlagos DNS pedig 1.1.1.1, harmadlagos 8.8.4.4
- Telepítse a szükséges szoftvereket és szolgáltatásokat. 

### 2. Active Directory tartományvezérlő telepítése és konfigurálása
- A tartomány neve legyen: „teszt.lan”. 
- Hozza létre a "dolgozok" és "adminok" csoportokat.
- Adja hozzá a következő felhasználókat:

| Teljes név             | Belépési név | Csoport  |
| ---------------------- | ------------ | -------- |
| Vickes Viktor          | vickes       | dolgozok |
| Szorgalmas Szebasztián | szorgalmas   | admin    |
| Dolgozó Olga           | dolgozo      | dolgozok |

- Hozzon létre egy megosztott mappát aminek a neve "Találtfileok"
- Csak olvasási joggal rendelkezik és automatikusan felcsatolásra kerül.

### 3. RAID 
- A szolgáltatás segítségével  és a meghajtók használatával hozd létre 

---

# Linux Szerver:

### 4. Linux konfiguráció
- A jelszó legyen "Admin123"
- A felhasználónév legyen "admin"
- A szerver neve legyen: „TesztLinux”.
- Szerkessze a GRUB konfigurációt úgy, hogy az időzítés 5 másodpercre legyen állítva
- Szerkessze a GRUB konfigurációt úgy, hogy muted üzemmódban induljon
- Állítsa be a szervert úgy, hogy mindig multi-user.target állapotban induljon

### 5. Statikus IP-cím beállítása
- Nyissa meg és szerkessze a Netplan konfigurációt. 
- Állítsa be az utolsó előtti IP-címre 

### 6. DHCP szerver beállítása
- Telepítse és konfigurálja az **ISC DHCP szervert**. (1p)
- Állítsa be a DHCP hatókört **a hálózati tartományban**. (1p)
- Állítsa be az alapértelmezett átjárót 192.168.1.1-re. 
- Engedélyezze és indítsa el a DHCP szolgáltatást.

## Hálózati kiosztás 192.168.10.0/28 (255.255.255.240)

| Eszköz                 | IP-cím | Megjegyzés                   |
| ---------------------- | ------ | ---------------------------- |
| TesztLinux (szerver)   | ?      | Szerver az utolsó előtti cím |
| TesztWindows (szerver) | ?      | Szerver az utolsó  cím       |

---

## Megjegyzések és értékelés:

| Feladat                                                           | Max. Pont | Elért Pont |
| ----------------------------------------------------------------- | --------- | ---------- |
| Windows konfiguráció                                              | 0         |            |
| Active Directory tartományvezérlő telepítése és konfigurálása     | 0         |            |
| RAID                                                              | 0         |            |
| Linux konfiguráció                                                | 0         |            |
| Statikus IP-cím beállítása                                        | 0         |            |
| DHCP konfigurálása                                                | 0         |            |
| DHCP szerver beállítása                                           | 0         |            |
|                                                                   |           |            |
| **Összesen**                                                      | **?**     | **/**      |

**Megjegyzések:**  
A vizsga befejezése után kérjük, hogy adja le a dokumentációt és a jegyzőkönyvet a vizsgáztatónak.
