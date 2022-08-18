# ZTE-MF286D
My compilation :: user friendly :: OpenWrt SNAPSHOT / LuCI Master 

![GitHub release (latest by date)](https://img.shields.io/github/v/release/4IceG/ZTE-MF286D?style=flat-square)
![GitHub stars](https://img.shields.io/github/stars/4IceG/ZTE-MF286D?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/4IceG/ZTE-MF286D?style=flat-square)
![GitHub All Releases](https://img.shields.io/github/downloads/4IceG/ZTE-MF286D/total)

> I added presets for my packages (luci-app-3ginfo-lite/luci-app-sms-tool/luci-app-lite-watchdog).

> All you need to do is change the apn (for qmi in LuCI) and set up wi-fi/passwords.



### Internet connection setup | Change of apn for mobile internet operator
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

### Useful AT commands (also available in the built image)
<details>
   <summary>Pokaż | Show me</summary>
   
``` bash
APN info ➜ AT+CGDCONT?;AT+CGDCONT?
APN setup ➜ AT+CGDCONT=1,"IP","internet","",0,0;AT+CGDCONT=1,"IP","internet","",0,0
APN apply ➜ AT+CGACT=1,1;AT+CGACT=1,1
Cell lock info ➜ AT+ZLOCKCELL?;AT+ZLOCKCELL?
Cell lock disabled ➜ AT+ZLOCKCELL=0;AT+ZLOCKCELL=0
Cell lock ➜ AT+ZLOCKCELL=earfcn_tag,pci_tag;AT+ZLOCKCELL=AAAA,BBB
DL CA info ➜ AT+ZCAINFO?;AT+ZCAINFO?
UL CA info ➜ AT+ZULCA?;AT+ZULCA?
UL CA disabled ➜ AT+ZULCA=0;AT+ZULCA=0
UL CA enabled ➜ AT+ZULCA=1;AT+ZULCA=1
Locked band info ➜ AT+ZNLOCKBAND?;AT+ZNLOCKBAND?
Modem reboot ➜ AT+CFUN=1,1;AT+CFUN=1,1
```

</details>

### LuCI packages available in the image:
<details>
   <summary>Pokaż | Show me</summary>
   
``` bash
luci-app-3ginfo-lite
luci-app-adblock
luci-app-atinout-mod
luci-app-commands
luci-app-cpu-status-mini
luci-app-ddns
luci-app-ekooneplstat
luci-app-firewall
luci-app-internet-detector
luci-app-ksmbd
luci-app-lite-watchdog
luci-app-minidlna
luci-app-modemband
luci-app-nft-qos
luci-app-openvpn
luci-app-opkg
luci-app-p910nd
luci-app-sms-tool
luci-app-vpnbypass
luci-app-watchcat
luci-app-wifischedule
luci-app-wireguard
luci-app-wrtbwmon
```
</details>
