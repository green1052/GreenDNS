# GreenDNS
광고 차단 DNS

## 서버 목록

### 1번 서버

|  종류 |                       주소                       |   업스트림 DNS 서버  |            소재지           |
|:-----:|:------------------------------------------------:|:--------------------:|:---------------------------:|
| Plain |                   152.70.248.32                  | Cloudflare DNS (DoH) | Oracle Cloud Infrastructure |
|  DoT  |       tls://server1.greendns.green1052.com       | Cloudflare DNS (DoH) | Oracle Cloud Infrastructure |
|  DoH  | https://server1.greendns.green1052.com/dns-query | Cloudflare DNS (DoH) | Oracle Cloud Infrastructure |
|  DoQ  |       quic://server1.greendns.green1052.com      | Cloudflare DNS (DoH) | Oracle Cloud Infrastructure |

#### Apple Profile

DoT: https://raw.githubusercontent.com/green1052/GreenDNS/main/config/server1/dot.mobileconfig

DoH: https://raw.githubusercontent.com/green1052/GreenDNS/main/config/server1/doh.mobileconfig

## DNS 차단 목록

```
# filter list: https://github.com/hagezi/dns-blocklists/blob/main/usedsources.md#proplus
https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/pro.plus.txt

https://raw.githubusercontent.com/green1052/GreenList/master/dns.txt
```

## 기능

1. 광고, 추적, 피싱, 멀웨어 같은 불필요한 사이트를 차단합니다.

2. 망 사용료 문제로 Cloudflare Enterprise 요금제를 사용하지 않는 웹사이트가 대한민국 서버가 아닌 곳을 경유하는 걸 방지합니다.[^1][^2]
- 2-1. 만약 해당 사이트가 대한민국 정부의 인터넷 검열 대상이라면 우회 프로그램 없이도 접속이 가능합니다.

## 정책

쿼리 로그는 익명으로 저장되며
24시간 마다 삭제됩니다.

## On-promiss

개인정보등 여러 이유로 GreenDNS를 신뢰할 수 없다면

[AdGuardHome](https://github.com/AdguardTeam/AdGuardHome)에
위 DNS 차단 목록을 적용하면 똑같이 작동하는 개인 DNS 서버를 만들 수 있습니다.

[^1]: 해당 필터는 [GreenList](https://github.com/green1052/GreenList)에서 관리됩니다.
[^2]: https://namu.wiki/w/Cloudflare#s-4
