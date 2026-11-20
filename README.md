# egern-cmcc-direct · 移动云盘直连规则集

中国移动云盘（和彩云）直连规则，让云盘上传/下载/在线播放不走代理。

## 文件

- `direct.list` — 规则条目，不含策略列，引用处指定 `DIRECT`

## 用法

Egern → 规则集 → 新建远程规则集 → 策略 DIRECT：

```
https://cdn.jsdelivr.net/gh/wukris1106/egern-cmcc-direct@main/direct.list
```

Raw 备用：

```
https://raw.githubusercontent.com/wukris1106/egern-cmcc-direct/main/direct.list
```

Surge：

```
RULE-SET,https://cdn.jsdelivr.net/gh/wukris1106/egern-cmcc-direct@main/direct.list,DIRECT
```

## 覆盖

`139.com`（含 yun / caiyun / m.mcloud 等子域）、`mcloud.139.com`、`chinamobile.com`（云盘 CDN 走移动自建 CDN）、`cmecloud.cn`、`ecpan.cn`、咪咕系播放域名。

## 来源与校验

- 移动系域名取自 `blackmatrix7/ios_rule_script` ChinaMobile 表，筛出云盘/存储相关
- 关键域名（yun.139.com、caiyun.139.com、yun.mcloud.139.com、m.mcloud.139.com）逐个 dig 实测解析后收录
- 重建于 2026-11-21

## 备注

原仓库另含一条 yusen Emby 反代直连。反代域名未在历史文件里留存 —— 需要的话把域名发来，加一行 `DOMAIN-SUFFIX,<域名>` 就行。
