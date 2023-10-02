# wifi-networkmanager for RetroPie-Setup  
![wifi-networkmanager.png](https://raw.githubusercontent.com/RapidEdwin08/wifi-networkmanager/master/wifi-networkmanager.png)  

A modified version of the RetroPie-Setup Module Script [wifi.sh] that supports NetworkManager Configs.  

CHANGES:
-------------
- Updated Connecting to WiFi to use [nmcli] in addition to updating [wpa_supplicant.conf]  
- Updated Remove WiFi Config to Remove [/etc/NetworkManager/system-connections/*.nmconnection] in addition to [wpa_supplicant.conf]  
- Updated method of obtaining [ip_wlan] Variable  
- Updated Available ESSIDs Menu List to Include [$quality] $essid [$frequency]  
- Added Enable/Disable WiFi Interface 0ptions  
- Added Re-Scan for Wireless networks 0ption to Available ESSIDs Menu List  
- Added sleep [wait_for_wlan] Variable to [_set_interface_wifi] UP/DOWN due to Device Busy Issue on some Devices  
- Added [wifi_interface] Variable for 0ther WiFi Devices  
- x3 Options for [signal_quality_method]: [dBm_to_percent_A] [dBm_to_percent_B] [dBm_no_conversion]  

## INSTALLATION
1 - **Backup** Current [wifi.sh] if not already:  
```bash
if [ ! -f ~/RetroPie-Setup/scriptmodules/supplementary/wifi.sh.BAK ]; then mv ~/RetroPie-Setup/scriptmodules/supplementary/wifi.sh ~/RetroPie-Setup/scriptmodules/supplementary/wifi.sh.BAK; fi

```  

2 - Get wifi-networkmanager [wifi.sh]:  
```bash
wget https://raw.githubusercontent.com/RapidEdwin08/wifi-networkmanager/master/scriptmodules/supplementary/wifi.sh -P ~/RetroPie-Setup/scriptmodules/supplementary

```  

## To REMOVE wifi-networkmanager [wifi.sh] and Restore Backup [wifi.sh.BAK]:  
```bash
if [ -f ~/RetroPie-Setup/scriptmodules/supplementary/wifi.sh.BAK ]; then mv ~/RetroPie-Setup/scriptmodules/supplementary/wifi.sh.BAK ~/RetroPie-Setup/scriptmodules/supplementary/wifi.sh; fi

```

***SOURCES:***  
[./RetroPie-Setup/scriptmodules/supplementary/wifi.sh](https://github.com/RetroPie/RetroPie-Setup/blob/master/scriptmodules/supplementary/wifi.sh)  
[wifi.sh from RetroPie v4.8.4 with OSK moved to scriptmodules/helpers.sh](https://github.com/RetroPie/RetroPie-Setup/commit/e1935ab5da917cb81a192002e627646a3438c2b4)  
[how-to-convert-wifi-signal-strength-from-quality-percent-to-rssi-dbm](https://stackoverflow.com/questions/15797920/how-to-convert-wifi-signal-strength-from-quality-percent-to-rssi-dbm)  
