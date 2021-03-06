# Weak Password

## 0x01 漏洞描述

网站管理、运营人员由于安全意识不足，为了方便、避免忘记密码等，使用了非常容易记住的密码，或者是直接采用了系统的默认密码等。

## 0x02 常见应用场景

弱口令没有严格的标准和准确的定义，通常认为容易被别人猜测到或被破解工具破解的口令均为弱口令。

通常以下情况会被定为弱口令：

* 连续的数字
* 连续的字母
* 连续的（数字+字母）
* 公司（全称or简称）+连续的（字母or数字）
* 个人姓名（全称or简称）+连续的（字母or数字）
* 网站域名+连续的（字母or数字）
* 任意（上+下 or 左+右 or shift）连续的键盘密码
* 包含上述情况任意位置的特殊字符
* 包含上述情况任意位置的年份的数字
* 包含上述情况任意位置的首字母大写
* 包含上述情况任意位置的常见单词
* 。。。

## 0x03 漏洞危害

攻击者利用此漏洞可直接进入应用系统或者管理系统，从而进行系统、网页、数据的篡改与删除，非法获取系统、用户的数据，甚至可能导致服务器沦陷。

## 0x04 修复建议

### 4.1 用户层面

* 不要使用常见的弱口令作为密码
* 不要多个系统或者社交账号使用同一套密码
* 定期修改密码
* 建议使用包含随机值的或者随机生成的字符串作为系统密码

### 4.2 系统层面

* 用户首次登录后强制用户修改默认密码
* 修改密码、添加账号等涉及密码策略处强制用户使用强密码策略（大小写字母+数字+特殊字符+8位以上）
* 服务端对登录处增加图形验证码并保证使用一次即销毁
* 服务端对登录接口进行限制，单个IP单位时间内请求超过阈值，封禁30分钟
* 服务端对登录接口进行限制，单个用户密码单位时间内错误次数超过阈值，封禁20分钟 