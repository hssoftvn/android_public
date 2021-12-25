# android #
Useful utilities and source code support Android projects


<b>Content</b>
1. [Wireless ADB](https://github.com/TinySonhh/android#1-wireless-adb)
2. [English Words](https://github.com/TinySonhh/android#2-english-words)

<br>

## 1. Wireless ADB ##
Keep your Android phone devices cable free with PC via ADB.

**Prepare**:
* Connect your Android phone/device with PC via suitable cable
* Make sure **Developer Options** is turned on
* Make sure **USB debugging** option is enabled
* Make sure the **Android SDK** is correctly installed and working well.
    * To test this, open CMD, then type ```adb devices```
    * Expected result: 
```
1List of devices attached
RFXXXXXXX     device
```
* Make sure your PC/Laptop and Android phone are on the same network

<br>

**Action**
* Download this tool - [adbwifi.exe](https://github.com/TinySonhh/android/blob/main/tools/wifiadb.exe) into your local storage.
* To be able run the file from anywhere, put this file in `%windir%` directory
* Run dirrectly the file, or open CMD, and type `adbwifi` then ENTER
* Wait for a sec, to have the expected result:

```
---- WIFI ADB ----
1/ Adb devices
List of devices attached
RF8XXXXXXX     device


2/ adb tcpip 5555
restarting in TCP mode port: 5555

... Waiting while switching to TcpIp mode....
3/adb shell ip addr show wlan0
40: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 3000
    link/ether xx:xx:xx:xx:xx:xx brd ff:ff:ff:ff:ff:ff
    inet 192.168.1.104/24 brd 192.168.1.255 scope global wlan0
       valid_lft forever preferred_lft forever
    inet6 xxxx::xxxx:xxxx:xxxx:xxxx/64 scope link
       valid_lft forever preferred_lft forever

40: wlan0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 3000
    link/ether xx:x:xx:xx:xx:a1 brd ff:ff:ff:ff:ff:ff
    inet 192.168.1.104/24 brd 192.168.1.255 scope global wlan0
       valid_lft forever preferred_lft forever
    inet6 xxxx::xxxx:xxxx:xxxx:xxxx/64 scope link
       valid_lft forever preferred_lft forever

4/adb connect 192.168.1.104
connected to 192.168.1.104:5555

5/ Adb devices
List of devices attached
RF8XXXXXX     device
192.168.1.104:5555      device
```

With the above result, you managed to connect to your Android phone via WIFI.

**Continue**

* Unplug the USB cable
* Type `adb devices` or `adb logcat` to check if the logcat is working.
* If it says that device is still **offline**,
  * Open Developer Options
  * Find USDB Debugging
  * Turn off it, then turn on again
* Recheck with `adb devices` or `adb logcat` if devices is online

Good luck!


## 2. English Words ##
All possible English words that can help you in developing applications or games about word in English language.
* [words.txt](https://github.com/TinySonhh/android/blob/main/languages/english/words.txt)
* [words_more.txt ](https://github.com/TinySonhh/android/blob/main/languages/english/words_more.txt)


THANK YOU.