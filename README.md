<p align="center">
<a href="https://t.me/rktechnoindians"><img title="Made in INDIA" src="https://img.shields.io/badge/MADE%20IN-INDIA-SCRIPT?colorA=%23ff8100&colorB=%23017e40&colorC=%23ff0000&style=for-the-badge"></a>
</p>

<a name="readme-top"></a>


# RK_Pairip


<p align="center"> 
<a href="https://t.me/rktechnoindians"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=800&size=35&pause=1000&color=F74848&center=true&vCenter=true&random=false&width=435&lines=RK_Pairip" /></a>
 </p>

Install
-------

**RK_Pairip Method 1**

    curl -L -o RKPairip.sh https://github.com/TechnoIndian/setup/releases/download/RKPairip/RKPairip.sh && chmod +x RKPairip.sh && ./RKPairip.sh

**RK_Pairip Method 2**

    pkg install python git && pip install git+https://github.com/TechnoIndian/RK_Pairip.git


Usage
-----

**RK_Pairip**

**Mode -i ➸ Default APKEditor (Input Your Apk Path)**

    RKPairip -i YourApkPath.apk

**Mode -a ➸ Decompile With ApkTool / Mode -b ➸ Decompile With Bak_Smali**

`For ApkTool ( -a )`

    RKPairip -i YourApkPath.apk -a

`For Bak_Smali ( -b )`

    RKPairip -i YourApkPath.apk -b

**Mode -d ➸ Delete SignatureCheck & LicenseClientV3 .smali (Default Is Set, Just Bypass)**

    RKPairip -i YourApkPath.apk -d
    
`For ApkTool ( -a -d ) / For Bak_Smali ( -b -d )`

    RKPairip -i YourApkPath.apk -a -d

**Mode -s ➸ Merge Skip (Do U Want Last Dex Add Seprate)**

    RKPairip -i YourApkPath.apk -s
    
`For ApkTool ( -a -s ) / For Bak_Smali ( -b -s )`

    RKPairip -i YourApkPath.apk -a -s
    
**Mode -r ➸ Pairip Dex Fix ( Try After Translate String to MT )**

    RKPairip -i YourApkPath.apk -r

**If Failed SigCopy Use Another Method ( Default apksigcopier, Use only with -a & -b ) -a -s2 / -b -s2**

    RKPairip -i YourApkPath.apk -a -s2

**Mode -m ➸ Anti-Split ( Only Merge Apk )**

    RKPairip -m YourApkPath.apk
    
**Mode -C ➸ Show Instructions & Credits**

    RKPairip -C

Fix Dex Regex
-------------

**Some time Not works Script -r (Repair_Dex) Flag, Because Script Delete Pairip Classes Folder, When some time important classes here in pairip folder so manually use Regex & Don't Delete Pairip Folder when in here important classes**


**Patch 1**

`regex`

    (# direct methods\n.method public static )FuckUByRK\(\)V([\s\S]*?.end method)[\w\W]*
    
`Replace`

    $1constructor <clinit>()V$2

**Patch 2**

`regex`

    sget-object.*\s+.*const-string v1,(.*\s+).*.line.*\n+.+.*\n.*invoke-static \{v0\}, LRK_TECHNO_INDIA/ObjectLogger;->logstring\(Ljava/lang/Object;\)V
    
`Replace`

    const-string v0,$1

**Patch 3**

`regex`

    invoke-static \{\}, .*;->callobjects\(\)V\n
    
`Replace`

    # Nothing(Means Empty) 

**Patch 4**

`regex`

    (\.method public.*onReceive\(Landroid/content/Context;Landroid/content/Intent;\)V\s+\.(registers|locals) \d+)[\s\S]*?const-string/jumbo[\s\S]*?(\s+return-void\n.end method)
    
`Replace`

    $1$3


**Patch 5**

`Search 1st without regex`

    pairip
    
`Search regex in Current Results`

    invoke.*pairip/(?!licensecheck/).*

`Replace`

    # Nothing(Means Empty) 


Note
----

## 🇮🇳 Welcome By Techno India 🇮🇳

[![Telegram](https://img.shields.io/badge/TELEGRAM-CHANNEL-red?style=for-the-badge&logo=telegram)](https://t.me/rktechnoindians)
  </a><p>
[![Telegram](https://img.shields.io/badge/TELEGRAM-OWNER-red?style=for-the-badge&logo=telegram)](https://t.me/RK_TECHNO_INDIA)
</p>
