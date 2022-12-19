# GreenDNS
광고 차단 DNS

## 주소

|  종류 |                   주소                   | 업스트림 DNS 서버 |            소재지           |
|:-----:|:----------------------------------------:|:-----------------:|:---------------------------:|
| Plain |               152.70.248.32              |   Cloudflare DNS  | Oracle Cloud Infrastructure |
|  DoT  |       tls://greendns.green1052.com       |   Cloudflare DNS  | Oracle Cloud Infrastructure |
|  DoH  | https://greendns.green1052.com/dns-query |   Cloudflare DNS  | Oracle Cloud Infrastructure |
|  DoQ  |       quic://greendns.green1052.com      |   Cloudflare DNS  | Oracle Cloud Infrastructure |

## DNS 차단 목록

```
# filter list: https://github.com/hagezi/dns-blocklists/blob/main/usedsources.md#proplus
https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/pro.plus.txt

https://raw.githubusercontent.com/green1052/GreenList/master/dns.txt
```

## 기능

1. 광고, 추척, 피싱, 멀웨어 같은 사이트 불필요한 사이트를 차단합니다.

2. 망 사용료 문제로 Cloudflare Enterprise 요금제를 사용하지 않는 웹사이트가 대한한국 서버가 아닌 곳을 경유하는 걸 방지합니다.[^1][^2]
  - 2-1. 만약 해당 사이트가 대한민국 정부의 인터넷 검열 대상이라면 우회 프로그램 없이도 접속이 가능합니다.

## 정책

쿼리 로그는 익명으로 저장되며
24시간 마다 삭제됩니다.

[^1]: 해당 필터는 [GreenList](https://github.com/green1052/GreenList)에서 관리됩니다.
[^2]: https://namu.wiki/w/Cloudflare#s-4
