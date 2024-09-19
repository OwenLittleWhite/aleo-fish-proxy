# aleo-fish-proxy

鱼池中转代理提升收益原理：
鱼池的锄头做了抽成，改造过的中转是为了将锄头抽走的那部分拦截，返给自己的账户，进行反抽，提高收益

软件抽成规则：

只对反抽部分进行 **10%** 的算力抽成，原收益部分不变

### 运行

1. 下载软件


[windows 下载地址](http://82.156.172.63:8080/s/7YmyT8R53REsLm5)

[ubuntu 下载地址](http://82.156.172.63:8080/s/ZpDX26DqRE5KZGF)

2. 配置

在下载好的同级目录下，创建一个`config.json`文件，填入以下内容：

```json
{
    "host": "aleo-asia.f2pool.com",
    "port": 4400,
    "localPort": 3333,
    "commissionAccounts": ["your_fish_account1", "your_fish_account2"],
    "commissionRates": [0.9, 0.1]
}
```

`host`为鱼池源地址

`port`为鱼池端口

`localPort`为本地监听端口

`commissionAccounts` 和 `commissionRates` 是配对使用的，`commissionAccounts` 的数量和 `commissionRates` 的数量需要保持一致。

如果是自用则只需配置一个:

```json
{
    "host": "aleo-asia.f2pool.com",
    "port": 4400,
    "localPort": 3333,
    "commissionAccounts": ["your_fish_account1"],
    "commissionRates": [1]
}
```

如果帮助别人部署想获得点额外收益则可以配置多个

`commissionRates` 表示对应账号的佣金比例，例如 `0.9` 表示 `commissionAccounts` 的第一个账号的佣金为 `90%`，第二个账号的佣金为 `10%`。·`commissionRates` 相加不能超过 1。


3. 运行

```
nohup ./aleo-proxy-v1.2 2>&1 &
```

日志文件位于`logs`目录下

4. 兼容性

兼容2.11.49、3.0.3、3.0.4锄头版本

> 建议使用新加坡或者香港的云服务器进行部署，开通对应端口的防火墙规则


### 社交账号

[X](https://x.com/web3Speculator)

[Telegram](https://t.me/+96K0euqJY-U2Mzc1)
