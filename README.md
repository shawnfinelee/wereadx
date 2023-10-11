# wereadx

微信读书增强版，基于微信读书网页版开发的额外增强功能

## 增强内容

1. 下载书架上的书到本地，目前仅支持下载 html 格式
2. 自动更新阅读时长，可用于刷“读书排行榜”或者“阅读挑战赛”
3. 每周日晚 23:30 自动领取“时长兑福利”中的免费体验卡(暂未对外开放)
4. 支持下载用户上传的 pdf 格式的书

> 如果需要更多功能，可以在issue区讨论

## 项目说明

### 关于数据
数据大部分来自于微信读书网页版，一小部分来自于APP，该项目主要解决了数据加密的问题。

数据获取及解密部分的代码目前不打算开源，但可以交流技术实现。

项目托管在 Deno Deploy 上面，由于资源有限(查看[免费计划](https://deno.com/deploy/pricing))，所以每个账号每月暂定只能下载20本书，月初会重置次数。

> 注意：同一本书重复下载会重复计次，毕竟重复下载也消耗了服务器资源。


## 特别注意

### 1. 关于付费内容
本项目不支持下载 **需要付费才能查看** 的内容，该内容通常表现为每章只有开头的一段内容，后面跟着省略号，如下图所示：

![需要付费才能查看的内容](incomplete.png)

### 2. 关于双重验证码

扫码登录时会提示下面的二次确认，但实际上并不需要输入这个验证码也可以登录成功。

![登录时二次确认](login.png)

这个应该是属于微信读书的bug，后续如果微信读书调整的话，我会跟进处理这个问题。


## 后续计划

- 修复部分图片无法加载的问题；
- 美化网站样式；
- 添加更多微信读书API，比如导出笔记、书评等；
- 支持下载更多电子书格式，比如 epub/azw3 等，[可以关注这个issue。](https://github.com/champkeh/wereadx/issues/2)
- 加入搜索功能，方便下载非书架上的书（因为[技术限制](https://github.com/champkeh/wereadx/issues/3)，并不保证能搜索到所有的书）。
