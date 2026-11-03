# Bright Data ISP 代理

[![推广](https://github.com/bright-cn/Awesome-Web-Scraping/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/proxy-types/isp-proxies?promo=github15)

## 概述
利用 Bright Data 庞大的 [ISP 代理网络](https://www.bright.cn/proxy-types/isp-proxies)，通过直接来自 ISP 的 IP，安全、稳定且高速地采集数据。

- **超过 700,000 个 ISP IP**
- 具备长期稳定性的**静态住宅 IP**
- **99.9% 的成功率**
- **支持 HTTP(S) 和 SOCKS5**
- **免费国家/地区级定位**

## 主要功能
- **全球覆盖**：访问[多个国家/地区](https://www.bright.cn/locations)的 ISP IP。
- **高成功率**：网站访问成功率高达 99.9%。
- **快速稳定**：低延迟、运行可靠，网络可用率达 99.99%。
- **专属 IP 访问**：使用独享 IP，确保连接始终稳定。
- **合乎道德的来源**：所有 ISP 代理均直接从 ISP 获取，并符合 GDPR 和 CCPA 要求。

## 定价方案
- **按量付费**：无需月度承诺，用量价格为 $8/GB。
- **月度订阅 - 共享**：
  - **10 个 IP**：$1.80/IP，每月 $18 + 增值税。
  - **100 个 IP**：$1.45/IP，每月 $145 + 增值税。
  - **500 个 IP**：$1.40/IP，每月 $700 + 增值税。
  - **1,000 个 IP**：$1.30/IP，每月 $1300 + 增值税。
  - **企业方案**：为大规模数据采集需求提供定制解决方案。
 
- **月度订阅 - 独享**：
  - **10 个 IP**：$3.50/IP，每月 $35 + 增值税。
  - **100 个 IP**：$2.75/IP，每月 $275 + 增值税。
  - **500 个 IP**：$2.60/IP，每月 $1300 + 增值税。
  - **1,000 个 IP**：$2.50/IP，每月 $2500 + 增值税。
  - **企业方案**：为大规模数据采集需求提供定制解决方案。
 
- **月度订阅 - 按流量付费**：
  - $7/GB，每月 $499 + 增值税。
  - $6/GB，每月 $999 + 增值税。
  - $5/GB，每月 $1999 + 增值税。
  - **企业方案**：为大规模数据采集需求提供定制解决方案。


注册后，首笔充值可获等额赠金，最高 $500！

## 开始使用 ISP 代理
1. **开始免费试用**：无需信用卡。
2. **集成**：通过 Bright Data 控制面板或 API 管理 IP 和配置。
3. **支持的语言**：提供 Python、Java、C#、Node.js 和 Shell 快速入门指南。

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
我们的 ISP 代理兼容多种广泛使用的自动化工具，包括：

- [**Puppeteer**](https://www.bright.cn/integration/puppeteer)
- [**Selenium**](https://www.bright.cn/integration/selenium)
- [**Playwright**](https://www.bright.cn/integration/playwright)
- [**AdsPower**](https://www.bright.cn/integration/adspower)
- [**MultiLogin**](https://www.bright.cn/integration/multilogin)

## 使用场景
ISP 代理的常见应用：

- [**电子商务**](https://www.bright.cn/use-cases/ecommerce)：跟踪价格和商品库存情况。
- [**社交媒体**](https://www.bright.cn/use-cases/social-media-for-marketing)：监测趋势和互动情况。
- [**房地产**](https://www.bright.cn/use-cases/real-estate)：采集房源信息数据。
- [**旅游**](https://www.bright.cn/use-cases/travel)：比较不同地区的旅游优惠。

## 常见问题

### 什么是 ISP 代理？
ISP 代理是分配给服务器的静态住宅 IP，让你能够像使用普通住宅 IP 一样访问内容，同时获得更高的速度和稳定性。

### ISP 代理如何工作？
ISP 代理使用直接来自 ISP 的 IP，让你能够以住宅用户的身份快速、可靠地访问内容，同时享受数据中心连接的速度。

### 使用 ISP 代理有哪些优势？
ISP 代理兼具[住宅 IP](https://www.bright.cn/proxy-types/residential-proxies) 的稳定性和匿名性，以及数据中心 IP 的速度，非常适合网页爬虫、广告验证和 SEO 监测等任务。

### 企业如何使用 ISP 代理？
ISP 代理常用于访问受限内容、验证广告、监测竞争对手网站和执行质量保证测试等任务。

### Bright Data 的 ISP 代理是否合规？
是的，所有 ISP 代理均以合乎道德的方式获取，并遵守包括 GDPR 和 CCPA 在内的数据保护法律，确保负责任的数据实践。
