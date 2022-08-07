# ZTE-MF286D
My compilation with LuCI (Master Openwrt SNAPSHOT)

![GitHub release (latest by date)](https://img.shields.io/github/v/release/4IceG/ZTE-MF286D?style=flat-square)
![GitHub stars](https://img.shields.io/github/stars/4IceG/ZTE-MF286D?style=flat-square)
![GitHub forks](https://img.shields.io/github/forks/4IceG/ZTE-MF286D?style=flat-square)
![GitHub All Releases](https://img.shields.io/github/downloads/4IceG/ZTE-MF286D/total)

> I added presets for my packages (luci-app-3ginfo-lite/luci-app-sms-tool/luci-app-lite-watchdog).

> All you need to do is change the apn (for qmi in LuCI) and set up wi-fi.



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

``` bash
LuCI packages available in the image at this time:
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
luci-app-openvpn
luci-app-opkg
luci-app-p910nd
luci-app-sms-tool
luci-app-vpnbypass
luci-app-wifischedule
luci-app-wireguard
luci-app-wrtbwmon
```
