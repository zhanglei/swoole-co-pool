# PaySDK

[![Latest Version](https://img.shields.io/packagist/v/yurunsoft/swoole-co-pool.svg)](https://packagist.org/packages/yurunsoft/swoole-co-pool)
[![License](https://img.shields.io/github/license/Yurunsoft/swoole-co-pool.svg)](https://github.com/Yurunsoft/swoole-co-pool/blob/master/LICENSE)

## 介绍

Swoole 协程工作池，它可以限定你的同时工作协程数量，并且减少协程频繁创建销毁的损耗。

宇润PHP全家桶群：17916227 [![点击加群](https://pub.idqqimg.com/wpa/images/group.png "点击加群")](https://jq.qq.com/?_wv=1027&k=5wXf4Zq)，如有问题会有人解答和修复。

程序员日常划水群：74401592 [![点击加群](https://pub.idqqimg.com/wpa/images/group.png "点击加群")](https://shang.qq.com/wpa/qunwpa?idkey=e2e6b49e9a648aae5285b3aba155d59107bb66fde02e229e078bd7359cac8ac3)。

## 原理

事先定好协程数量和工作队列长度，将所有工作协程事先创建好。

使用 `Swoole\Coroutine\Channel` 实现工作队列。

在每个工作协程中，`Swoole\Coroutine\Channel->pop()`。一旦有新的任务 `push` 进队列，就会有一个工作协程被唤醒。

## 安装

在您的composer.json中加入配置：

```json
{
    "require": {
        "yurunsoft/swoole-co-pool": "~1.0"
    }
}
```

然后执行`composer update`命令。

## 代码示例

详见 `test/test.php`

## 捐赠

<img src="https://raw.githubusercontent.com/Yurunsoft/swoole-co-pool/master/res/pay.png"/>

开源不求盈利，多少都是心意，生活不易，随缘随缘……
