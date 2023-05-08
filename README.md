# VpnHood Configuratoin : نصب و کانفیگ وی پی ان هود


###### لینک ویدیو : 
```
https://www.youtube.com/watch?v=miO9ic2D-YQ
```

###### خرید دامنه از نیم چیپ: 
```
https://namecheap.pxf.io/BX7m6W
```
###### خرید دامنه سایت ایرانی: 
```
https://dashboard.azaronline.com/order/?aff=790&p=domain
```
###### خرید سرور از دیجیتال اوشن : 
```
https://m.do.co/c/0fb522deafa4
```
###### خرید سرور از سایت ایرانی : 
```
https://dashboard.azaronline.com/order/?aff=790&p=vps
```

**If you think this project is helpful to you, you may wish to give a** 🌟

**Feel Free To Donation :** ❤️

>TRC20: ```TGTyqv2MH7dZztMvaP5PKuS9Bma8RY5Pk8```

>ETH: ```0x5b5202a54e5ce4fb25f0d886254eeb07bb088614```

###### Update & Upgrade : آپدیت و آپگرید سرور
```
sudo apt-get update && sudo apt-get upgrade -y && sudo apt-get autoremove -y 
```
###### Install VpnHood :  نصب وی پی ان هود
```
sudo su -c "bash <( wget -qO- https://github.com/vpnhood/VpnHood/releases/latest/download/install-linux.sh)"
```
###### During the installation, the script will ask to Install DotNet and ask to enable autostart of VpnHood, Press Y in both.
###### درحین نصب اسکریپت ازتون میخواد که دات نت رو نصب کنه، بهش اجازه نصب بدید، و شروع با استارت آپ رو هم براش فعال کنید.
###### Start and Stop Server : شروع و استاپ سرور وی پی ان
```
sudo systemctl stop VpnHoodServer
sudo systemctl start VpnHoodServer
```
###### Create users Key : ساخت کلید برای نرم افزار 
```
sudo dotnet /opt/VpnHoodServer/launcher/run.dll gen
```

###### Default port in VpnHood is 443 : پورت دیفالت توی وی پی ان هود 443 هستش.
###### Change Port if needed : تغییر پورت در صورت نیاز

###### Check for appsettings.json : چک کنید که فایل سیتینگ موجوده یا نه
```
cd /opt/VpnHoodServer && ls
```
###### Edit the appsettings.json file : فایل سیتینگ رو ویرایش کنید و پورت رو تغییر بدید.
```
sudo nano /opt/VpnHoodServer/appsettings.json
```
###### Copy & past the following lines : کدای زیر رو کپی پیست کنید توی فایل سیتینگ، بجای 443 میتونید پورت دلخواه وارد کنید.
appsettings.json

```
{
  "RestAccessServer": null,
  "FileAccessServer": {
    "TcpEndPoints": [ "0.0.0.0:443", "[::]:443" ],
    "SslCertificatesPassword": null,
    "TrackingOptions": {
      "LogLocalPort": false,
      "LogClientIp": false
    },
    "SessionOptions": {
      "Timeout": 600,
      "UdpTimeout": 60,
      "TcpTimeout": 900,
      "IcmpTimeout": 30,
      "MaxDatagramChannelCount": 8,
      "MaxUdpPortCount": 0,
      "TcpBufferSize": 8192
    }
  },
  "IsDiagnoseMode": false
}
```

###### Install VpnHood Using UI WebSite: نصب وی پی ان هود از طریق سایت

```
https://console.vpnhood.com/
```
###### If you Install VpnHood using setting you should paste the given code into "appsettings.json" file that located here.
###### اگه از طریق فایل تنظیمات یوآی تصمیم دارید وی پی ان هود رو نصب میکنید، باید کدای دریافتی از سایت رو توی سیتینگ ذخیره کنید، که مسیرش اینجاست
```
cd /opt/VpnHoodServer && ls
```
