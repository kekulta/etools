# etools

This repo contains a few scripts to make your life easier if you work with Android Terminals from command line.

### adbr (adb restart)

Automate your adb resatart when adb won't see your device ~~again~~:
```console
$ adb kill-server
$ adb start-server
```

### emanager (emulator manager)

This command will search for available emulators and let you choose which one launch. After that it starts emulator and connects to it with telnet.
This command relies on ```expect``` available in your ```$PATH``` and available ```~/.emulator_console_auth_token ```.

```console
$ emanager
Choose device:
[0] Pixel_3_XL_API_30
[1] Pixel_6_API_24
[2] Pixel_6_API_30
$ 0
Pixel_3_XL_API_30 emulator is being started...
```
You can exit from dialog with ```quit``` or ```exit```.
```console
$ emanager
Choose device:
[0] Pixel_3_XL_API_30
[1] Pixel_6_API_24
[2] Pixel_6_API_30
$ quit
Goodbye!
```

```emanager``` could also be started with arguments:
| Flag | Description |
| ----------- | ----------- |
| ```-w```      | Wipes emulator by starting it with ```-wipe-data```       |
| ```-v```   | All of the ```emulator``` output will be shown, not only stderr        |
| ```-a args```  | ```args``` will be added to the ```emulator``` command |

With ```-a``` flag you can do basically anything with emulator but you do not need find available avds or manually connect to the console.

**Enjoy**!
