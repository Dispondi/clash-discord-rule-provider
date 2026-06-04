# clash-discord-rule-provider

Домены и CIDR взял [здесь](https://github.com/AJleKcAHgP68/host-list-ru)

---

## Ссылки

[discord-domain.yaml](https://raw.githubusercontent.com/Dispondi/clash-discord-rule-provider/main/discord-domain.yaml)

[discord-ip-cidr.yaml](https://raw.githubusercontent.com/Dispondi/clash-discord-rule-provider/main/discord-ip-cidr.yaml)

## Конфиг

```yaml
rule-providers:
  discord-dispondi-domain:
    behavior: classical
    type: http
    url: "https://raw.githubusercontent.com/Dispondi/clash-discord-rule-provider/main/discord-domain.yaml"
    interval: 86400
    path: ./ruleset/discord-dispondi-domain.yaml
    
  discord-dispondi-cidr:
    behavior: classical
    type: http
    url: "https://raw.githubusercontent.com/Dispondi/clash-discord-rule-provider/main/discord-ip-cidr.yaml"
    interval: 86400
    path: ./ruleset/discord-dispondi-cidr.yaml

rules:
  - RULE-SET,discord-dispondi-domain,Proxy
  - RULE-SET,discord-dispondi-cidr,Proxy
```
