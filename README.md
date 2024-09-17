# aleo-fish-proxy

鱼池中转代理提升收益原理：
鱼池的锄头做了抽成，改造过的中转是为了将锄头抽走的那部分拦截，返给自己的账户，进行反抽，提高收益

## 运行

1. 下载软件

[windows]()

[ubuntu]()

2. 配置
   在下载好的同级目录下，创建一个`config.json`文件，填入以下内容：

```json
{
    "host": "aleo-asia.f2pool.com", // 鱼池源地址
    "port": 4400, // 鱼池端口
    "localPort": 3333, // 本地监听端口
    "commissionAccounts": ["your_fish_account1", "your_fish_account2"],
    "commissionRates": [0.9, 0.1]
}
```

`commissionAccounts` 和 `commissionRates` 是配对使用的，`commissionAccounts` 的数量和 `commissionRates` 的数量需要保持一致。
`commissionRates` 表示对应账号的佣金比例，例如 `0.9` 表示 `commissionAccounts` 的第一个账号的佣金为 `90%`，第二个账号的佣金为 `10%`。·`commissionRates` 相加不能超过 1。
