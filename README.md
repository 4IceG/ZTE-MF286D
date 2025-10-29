# ZTE-MF286D

<p align="center">
<img src="https://github.com/4IceG/Personal_data/blob/master/developmaster.png?raw=true" />
</p>

My compilation :: user friendly :: OpenWrt SNAPSHOT / LuCI Main

![GitHub release (latest by date)](https://img.shields.io/github/v/release/4IceG/ZTE-MF286D?style=flat-square)
![GitHub stars](https://img.shields.io/github/stars/4IceG/ZTE-MF286D?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/4IceG/ZTE-MF286D?style=flat-square)
![GitHub All Releases](https://img.shields.io/github/downloads/4IceG/ZTE-MF286D/total)

### 1. <img src="https://raw.githubusercontent.com/4IceG/Personal_data/master/dooffy_design_icons_EU_flags_United_Kingdom.png" height="24"> What You Should Know / <img src="https://raw.githubusercontent.com/4IceG/Personal_data/master/dooffy_design_icons_EU_flags_Poland.png" height="24"> Co powinieneś wiedzieć

+ #### Installation of additional packages / Instalacja dodatkowych pakietów
> Snapshots are built daily, and that sets time limits to installing new packages with opkg. Due to kernel version checksums, you can only install “kmod” kernel modules and other kernel version dependent modules from the exactly same snapshot build. So, a few hours after flashing the firmware you may not be able to install new modules with opkg any more (as the next snapshot has been built into the download repo and has different checksums).   
> Obrazy snapshots budowane są codziennie, a to ustawia limity czasowe na instalację nowych pakietów za pomocą opkg. Z powodu sum kontrolnych wersji jądra, możesz zainstalować tylko moduły "kmod" i inne moduły zależne od wersji jądra z dokładnie tego samego snapshotu. Tak więc, kilka godzin po flashowaniu firmware możesz nie być w stanie zainstalować nowych modułów za pomocą opkg (ponieważ następny snapshot został wbudowany w repo i ma inne sumy kontrolne).

+ #### User's own configuration / Konfiguracja przez użytkownika
> Router requires user to check the configuration and optionally enable packages for transfer statistics and watchdog.   
> Router wymaga sprawdzenia konfiguracji przez użytkownika i opcjonalnego włączenia pakietów do statystyk transferu oraz watchdoga.

+ #### LuCI theme / Motyw LuCI
> Main theme: Bootstrap.   
> Główny motyw: Bootstrap.

+ #### My modifications / Moje modyfikacje
> I changed the miniDLNA icon.   
> Zmieniłem ikonę dla miniDLNA.
<details>
   <summary>Pokaż | Show me</summary>
   
![](https://github.com/4IceG/Personal_data/blob/master/nicons.PNG?raw=true)
   
![](https://github.com/4IceG/Personal_data/blob/master/MF286D.PNG?raw=true=true)
</details>

+ #### Languages added to image / Języki dodane do obrazu
> Language packs: German, English, Italian, Polish, Russian, Vietnamese, Simplified Chinese  
> Pakiety językowe: Niemiecki, Angielski, Włoski, Polski, Rosyjski, Wietnamski, Chiński.

### 2. Internet connection setup | Change of apn for mobile internet operator
<details>
   <summary>Pokaż | Show me</summary>
   
   > We go in the menu to Network \ Interfaces.
    
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/1.PNG?raw=true)
   
   > For the QMI protocol, go to the settings by clicking the Edit button.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/2.PNG?raw=true)
   
   > Enter the apn name of internet provider and click save.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/3b.PNG?raw=true)
   
   > If after changing the apn we do not have internet, we have to manually set the apn in the modem. 
   To do this, go to the Modem \ SMS Messages menu.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/4.PNG?raw=true)
   
   > Go to the at command tab and select APN setup from the drop-down menu.
   Enter the apn of internet operator and click on the button that sends the command.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/5.PNG?raw=true)
   
   > Now we restart the modem so that the modem starts up with the new apn.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/6.PNG?raw=true)

</details>

### 3. Useful AT commands (also available in the built image)
<details>
   <summary>Pokaż | Show me</summary>
   
``` bash
APN info ➜ AT+CGDCONT?;AT+CGDCONT?
APN setup ➜ AT+CGDCONT=1,"IP","internet","",0,0;AT+CGDCONT=1,"IP","internet","",0,0
APN apply ➜ AT+CGACT=1,1;AT+CGACT=1,1
Cell lock info ➜ AT+ZLOCKCELL?;AT+ZLOCKCELL?
Cell lock disabled ➜ AT+ZLOCKCELL=0;AT+ZLOCKCELL=0
Cell lock ➜ AT+ZLOCKCELL=earfcn_tag,pci_tag;AT+ZLOCKCELL=AAAA,BBB
Network mode info ➜ AT+ZSNT?;AT+ZSNT?
Prefer 4G (Blue LED blinks) ➜ AT+ZSNT=0,0,0;AT+ZSNT=0,0,0
4G/3G only ➜ AT+ZSNT=7,0,0;AT+ZSNT=7,0,0
4G only ➜ AT+ZSNT=6,0,0;AT+ZSNT=6,0,0
3G only (LED turns green) ➜ AT+ZSNT=2,0,0;AT+ZSNT=2,0,0
2G only (LED turns red) ➜ AT+ZSNT=1,0,0;AT+ZSNT=1,0,0
DL CA info ➜ AT+ZCAINFO?;AT+ZCAINFO?
UL CA info ➜ AT+ZULCA?;AT+ZULCA?
UL CA disabled ➜ AT+ZULCA=0;AT+ZULCA=0
UL CA enabled ➜ AT+ZULCA=1;AT+ZULCA=1
Locked band info ➜ AT+ZNLOCKBAND?;AT+ZNLOCKBAND?
Modem reboot ➜ AT+CFUN=1,1;AT+CFUN=1,1
```

</details>

### 4. LuCI packages available in the image:
<details>
   <summary>Pokaż | Show me</summary>
   
``` bash
List coming soon..
```
</details>
