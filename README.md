# Bright Data ISP 代理

[![Promo](https://github.com/bright-cn/ISP-Proxies/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://bright.cn/proxy-types/isp-proxies?promo=github15)

## 概览
利用 Bright Data 广泛的 [ISP 代理网络](https://bright.cn/proxy-types/isp-proxies)，实现安全、稳定和高速的数据采集，IP 地址直接由 ISP 提供。

- **700,000+ ISP IP 地址**
- **静态住宅 IP**，长期稳定性
- **99.9% 成功率**
- **支持 HTTP(S) 和 SOCKS5**
- **免费国家级定位**

## 主要功能
- **全球覆盖**：通过 [多个国家](https://bright.cn/locations) 访问 ISP IP。
- **高成功率**：访问网站的成功率高达 99.9%。
- **快速稳定**：低延迟和 99.99% 的网络可用性确保可靠性。
- **独享 IP 访问**：专属 IP 提供稳定的连接。
- **伦理合规**：所有 ISP 代理均直接由 ISP 获取，符合 GDPR 和 CCPA 规定。

## 价格计划
- **按需付费**：$15/GB，无月度承诺。
- **月度订阅 - 共享**：
  - **10 个 IP**：$1.80/IP，$18/月 + 增值税。
  - **100 个 IP**：$1.45/IP，$145/月 + 增值税。
  - **500 个 IP**：$1.40/IP，$700/月 + 增值税。
  - **1,000 个 IP**：$1.30/IP，$1300/月 + 增值税。
  - **企业计划**：为大规模数据采集需求提供定制解决方案。
 
- **月度订阅 - 专属**：
  - **10 个 IP**：$3.50/IP，$35/月 + 增值税。
  - **100 个 IP**：$2.75/IP，$275/月 + 增值税。
  - **500 个 IP**：$2.60/IP，$1300/月 + 增值税。
  - **1,000 个 IP**：$2.50/IP，$2500/月 + 增值税。
  - **企业计划**：为大规模数据采集需求提供定制解决方案。
 
- **月度订阅 - 按流量计费**：
  - $12.75/GB，$499/月 + 增值税。
  - $11.25/GB，$999/月 + 增值税。
  - $10.50/GB，$1999/月 + 增值税。
  - **企业计划**：为大规模数据采集需求提供定制解决方案。

注册并首次充值可享受 1:1 返现奖励，最高达 $500！

## 开始使用 ISP 代理
1. **免费试用**：无需信用卡。
2. **集成**：通过 Bright Data 的控制面板或 API 管理 IP 和配置。
3. **支持的语言**：提供适用于 Python、Java、C#、Node.js 和 Shell 的快速入门指南。

## 代码示例

### Python

```python
import sys

# Replace '[your customerID]', 'isp', and '[your password]' with your actual Bright Data customer ID, zone, and password
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
             'https': 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        HttpHost proxy = new HttpHost("brd.superproxy.io", 22225);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-isp", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // Replace '[your customerID]' and '[your password]' with your actual credentials
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:22225");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-isp", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-isp:"[your password]"@brd.superproxy.io:22225',
})
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# Replace '[your customerID]' and '[your password]' with your actual credentials
curl --proxy brd.superproxy.io:22225 --proxy-user brd-customer-[your customerID]-zone-isp:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## 集成
我们的 ISP 代理兼容广泛使用的自动化工具，包括：

- [**Puppeteer**](https://bright.cn/integration/puppeteer)
- [**Selenium**](https://bright.cn/integration/selenium)
- [**Playwright**](https://bright.cn/integration/playwright)
- [**AdsPower**](https://bright.cn/integration/adspower)
- [**MultiLogin**](https://bright.cn/integration/multilogin)

## 用例
ISP 代理的常见应用：

- [**电子商务**](https://bright.cn/use-cases/ecommerce)：追踪价格和产品库存。
- [**社交媒体**](https://bright.cn/use-cases/social-media-for-marketing)：监控趋势和互动。
- [**房地产**](https://bright.cn/use-cases/real-estate)：收集房产列表数据。
- [**旅游**](https://bright.cn/use-cases/travel)：比较不同地点的旅游报价。

## 常见问题解答

### 什么是 ISP 代理？
ISP 代理是分配给服务器的静态住宅 IP，允许您以普通住宅 IP 的身份访问内容，但速度和稳定性更高。

### ISP 代理如何工作？
ISP 代理使用直接来自 ISP 的 IP，提供住宅视角的快速可靠访问，同时具有数据中心连接的速度。

### 使用 ISP 代理有什么好处？
ISP 代理结合了 [住宅 IP](https://bright.cn/proxy-types/residential-proxies) 的稳定性和匿名性，以及数据中心 IP 的速度，非常适合网页抓取、广告验证和 SEO 监控等任务。

### 企业如何使用 Bright Data 的 ISP 代理？
ISP 代理广泛用于访问受限内容、验证广告、监控竞争对手网站以及质量保证测试等任务。

### Bright Data 的 ISP 代理是否合规？
是的，所有 ISP 代理均通过合乎伦理的方式获取，并符合包括 GDPR 和 CCPA 在内的数据保护法律，确保负责任的数据实践。
