# DebloatAndroid V.1.0
Welcome!
**If you want to remove apps that come pre-installed** on your Android and you couldn't make it from the device, **this is your place**.

## PreDebloat
### Linux
1. Install ADB
```bash
sudo apt install adb
```

### Windows
The commands used here must be executed in a powershell terminal as administrator.

1. First, we are going to install Chocolatey  
```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

2. We use Chocolatey for install ADB (Android Debug Bridge - https://developer.android.com/studio/command-line/adb)  
```powershell
choco install adb
```

### All users
1. Enable developer options in your mobile phone
> Settings -> About phone -> Software Information -> x8 taps/clicks on "Compilation Number"

2. Enable "USB Debugging"
> Settings -> Developer options -> USB Debugging :white_check_mark:

3. Check if ADB recognizes your device
```powershell
adb devices
```

4. That's all, now you can execute ADB commands

## Debloat
You will find two folders, one for ps1 files (powershell) and one for sh files (linux shell)

1. Execute DebloatAndroidGlobal

**PowerShell**
```powershell
.\DebloatAndroidGlobal.ps1
```

**Linux Shell**
```bash
./DebloatAndroidGlobal.sh
```

2. Execute DebloatAndroidUser

**PowerShell**
```powershell
.\DebloatAndroidUser.ps1
```

**Linux Shell**
```bash
./DebloatAndroidUser.sh
```

3. That's all, Android optimized!