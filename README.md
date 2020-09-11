# DebloatAndroid V.1.0
Welcome!
**If you want to remove apps that come pre-installed** on your Android and you couldn't make it from the device, **this is your place**.

## PreDebloat
The commands used here must be executed in a powershell terminal as administrator.

1. First, we are going to install Chocolatey  
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
2. We use Chocolatey for install ADB (Android Debug Bridge - https://developer.android.com/studio/command-line/adb)  
```powershell
choco install adb
```
3. Enable developer options in your mobile phone
> Settings -> About phone -> Software Information -> x8 taps/clicks on "Compilation Number"

4. Enable "USB Debugging"
> Settings -> Developer options -> USB Debugging :white_check_mark:

5. Check if ADB recognizes your device
```powershell
adb devices
```

6. That's all, now you can execute ADB commands

## Debloat
This is the moment, you just have to execute the ps1 file in a powershell terminal as administrator.
```powershell
.\DebloatAndroid.ps1
```
