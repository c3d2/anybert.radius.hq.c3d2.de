
Usage
=====
```
   # sudo su
   $ cd /etc/wpa_supplicant; mkdir certs; cd certs
   $ wget --no-check-certificate https://gitlab.hq.c3d2.de/daniel.plominski/anybert.radius.hq.c3d2.de/raw/master/certs/anybert.radius.hq.c3d2.de
   $ wget --no-check-certificate https://gitlab.hq.c3d2.de/daniel.plominski/anybert.radius.hq.c3d2.de/raw/master/certs/radius.hq.c3d2.de
```
* vi /etc/wpa_supplicant/wpa_supplicant.conf

```
### C3D2 Wireless Network // ###

network={
        ssid="C3D2.anybert"
        key_mgmt=WPA-EAP
        eap=TTLS
        phase2="auth=PAP"
        identity="anonymous"
        password="anonymous"
        ca_cert="/etc/wpa_supplicant/certs/radius.hq.c3d2.de"
        # priority=25
}

network={
        ssid="C3D2.anybert 5"
        key_mgmt=WPA-EAP
        eap=TTLS
        phase2="auth=PAP"
        identity="anonymous"
        password="anonymous"
        ca_cert="/etc/wpa_supplicant/certs/radius.hq.c3d2.de"
        # priority=26
}

### // C3D2 Wireless Network ###
```

