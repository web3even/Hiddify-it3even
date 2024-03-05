# Hiddify-it3even
**𝙏𝙃𝙀 𝘽𝙀𝙎𝙏 𝙎𝙐𝘽𝙇𝙄𝙉𝙆𝙎 𝙁𝙊𝙍 𝙃𝙄𝘿𝘿𝙄𝙁𝙔 𝙉𝙀𝙓𝙏 𝘼𝙋𝙋**

`𝚁𝚎𝚙𝚕𝚜𝚎𝚍 𝚈𝚘𝚞𝚛 𝙲𝚕𝚎𝚊𝚗 𝙸𝚙 𝚆𝚒𝚝𝚑 𝙸𝚗 𝙲𝚘𝚍𝚎.𝚝𝚡𝚝`

```
{  
"route": {
    "geoip": {
      "path": "geo-assets\\sagernet-sing-geoip-geoip.db"
    },
    "geosite": {
      "path": "geo-assets\\sagernet-sing-geosite-geosite.db"
    },
    "rules": [
      {
        "inbound": "dns-in",
        "outbound": "dns-out"
      },
      {
        "port": 53,
        "outbound": "dns-out"
      },
      {
        "clash_mode": "Direct",
        "outbound": "direct"
      },
      {
        "clash_mode": "Global",
        "outbound": "select"
      }
    ],
    "auto_detect_interface": true,
    "override_android_vpn": true
  },
  "outbounds": [
    {
      "type": "selector",
      "tag": "select",
      "outbounds": [
        "auto",
        "IP->Iran, Yotube:MisaHiro",
        "IP->Main, Yotube:MisaHiro"
      ],
      "default": "auto"
    },
    {
      "type": "urltest",
      "tag": "auto",
      "outbounds": [
        "IP->Iran, Yotube:MisaHiro",
        "IP->Main, Yotube:MisaHiro"
      ],
      "url": "http://cp.cloudflare.com/",
      "interval": "10m0s"
    },
    {
      "type": "wireguard",
      "tag": "IP->Iran, Yotube:MisaHiro",
      "local_address": [
        "172.16.0.2/32",
        "2606:4700:110:8c91:4063:21d0:7dd5:f218/128"
      ],
      "private_key": "CBVIIWvXdLr4PbSrnm11ZJJ300IiPudRD4R62/IxV1g=",
      "server": "162.159.192.117",
      "server_port": 8886,
      "peer_public_key": "bmXOC+F1FxEMF9dyiK2H5/1SUtzH0JuVo51h2wPfgyo=",
      "reserved": "AAAA",
      "mtu": 1280,
      "fake_packets": "5-10"
    },
    {
      "type": "wireguard",
      "tag": "IP->Main, Yotube:MisaHiro",
      "detour": "IP->Iran, Yotube:MisaHiro",
      "local_address": [
        "172.16.0.2/32",
        "2606:4700:110:8c15:3f90:ad2d:8810:77f3/128"
      ],
      "private_key": "CCC/TQTc82ub9i8f37Rpix2v425Sv/mxTzvE/iKRMkw=",
      "server": "162.159.192.117",
      "server_port": 8886,
      "peer_public_key": "bmXOC+F1FxEMF9dyiK2H5/1SUtzH0JuVo51h2wPfgyo=",
      "reserved": "AAAA",
      "mtu": 1280,
      "fake_packets": "5-10"
    },
    {
      "type": "dns",
      "tag": "dns-out"
    },
    {
      "type": "direct",
      "tag": "direct"
    },
    {
      "type": "direct",
      "tag": "bypass"
    },
    {
      "type": "block",
      "tag": "block"
    }
  ]  
}
```

آی پی تمیز مربوط به اپراتور خود را با ای پی های موحود در این کد جابجا کرده و آدرس آن را در هیدیفای بارگزاری کنید.!

[Contact Me](https://t.me/titanzeusbot)
