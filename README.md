# ZTE-MF286D

<p align="center">
<img src="https://github.com/4IceG/Personal_data/blob/master/developmaster.png?raw=true" />
</p>

My compilation :: user friendly :: OpenWrt SNAPSHOT / LuCI Master

![GitHub release (latest by date)](https://img.shields.io/github/v/release/4IceG/ZTE-MF286D?style=flat-square)
![GitHub stars](https://img.shields.io/github/stars/4IceG/ZTE-MF286D?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/4IceG/ZTE-MF286D?style=flat-square)
![GitHub All Releases](https://img.shields.io/github/downloads/4IceG/ZTE-MF286D/total)

### <img src="https://raw.githubusercontent.com/4IceG/Personal_data/master/dooffy_design_icons_EU_flags_United_Kingdom.png" height="24"> What You Should Know / <img src="https://raw.githubusercontent.com/4IceG/Personal_data/master/dooffy_design_icons_EU_flags_Poland.png" height="24"> Co powinieneś wiedzieć

> Snapshots are built daily, and that sets time limits to installing new packages with opkg. Due to kernel version checksums, you can only install “kmod” kernel modules and other kernel version dependent modules from the exactly same snapshot build. So, a few hours after flashing the firmware you may not be able to install new modules with opkg any more (as the next snapshot has been built into the download repo and has different checksums).   
> Obrazy snapshots budowane są codziennie, a to ustawia limity czasowe na instalację nowych pakietów za pomocą opkg. Z powodu sum kontrolnych wersji jądra, możesz zainstalować tylko moduły "kmod" i inne moduły zależne od wersji jądra z dokładnie tego samego snapshotu. Tak więc, kilka godzin po flashowaniu firmware możesz nie być w stanie zainstalować nowych modułów za pomocą opkg (ponieważ następny snapshot został wbudowany w repo i ma inne sumy kontrolne).

> All you need to do is change the apn (for qmi in LuCI) and set up wi-fi/passwords.   
> Wszystko, co musisz zrobić, to zmienić apn (dla qmi w LuCI) i skonfigurować Wi-Fi/hasła.

> Main theme: Bootstrap.   
> Główny motyw: Bootstrap.

> I changed the minidlna, lan ports, wi-fi, signal levels icons.   
> Zmieniłem ikony dla minidlna, portów lan, wi-fi, poziomów sygnału.

> Language packs: English and Polish. (I can add other languages, but this will require translating my packages / add-ons).   
> Pakiety językowe: angielski i polski. (Mogę dodać inne języki, ale będzie to wymagało przetłumaczenia moich pakietów/dodatków).

#### Internet connection setup | Change of apn for mobile internet operator
<details>
   <summary>Pokaż | Show me</summary>
    We go in the menu to Network \ Interfaces.
    
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/1.PNG?raw=true)
   
   For the QMI protocol, go to the settings by clicking the Edit button.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/2.PNG?raw=true)
   
   Enter the apn name of internet provider and click save.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/3.PNG?raw=true)
   
   If after changing the apn we do not have internet, we have to manually set the apn in the modem. 
   To do this, go to the Modem \ SMS Messages menu.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/4.PNG?raw=true)
   
   Go to the at command tab and select APN setup from the drop-down menu.
   Enter the apn of internet operator and click on the button that sends the command.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/5.PNG?raw=true)
   
   Now we restart the modem so that the modem starts up with the new apn.
   
   ![](https://github.com/4IceG/Personal_data/blob/master/zrzuty/apntutorialsm/6.PNG?raw=true)

</details>

#### Useful AT commands (also available in the built image)
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

#### LuCI packages available in the image:
<details>
   <summary>Pokaż | Show me</summary>
   
``` bash
luci-app-3ginfo-lite
luci-app-adblock
luci-app-aria2
luci-app-atcommands
luci-app-commands
luci-app-cpu-status-mini
luci-app-ddns
luci-app-drive-status-mini
luci-app-ekooneplstat
luci-app-firewall
luci-app-internet-detector
luci-app-ksmbd
luci-app-ledcontrol
luci-app-lite-watchdog
luci-app-minidlna
luci-app-modemband
luci-app-mwan3
luci-app-nft-qos
luci-app-openvpn
luci-app-opkg
luci-app-p910nd
luci-app-sms-tool-js
luci-app-wifischedule
luci-app-wrtbwmon
luci-proto-wireguard
```
</details>
