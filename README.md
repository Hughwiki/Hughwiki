# 渗透测试框架 POCSUITE3-pocs编写
<img width="851" alt="image" src="https://user-images.githubusercontent.com/118670924/202905360-f8860ffc-7024-4999-8aa6-5dfbb01a185d.png">



## 一切都在进行中，明天会更好！


# Pocsuite3 是什么？

# 简介
Pocsuite3 是由知道创宇 404 实验室打造的一款基于 GPLv2 许可证开源的远程漏洞测试框架。它是知道创宇安全研究团队发展的基石，是团队发展至今一直维护的一个项目，自 2015 年开源以来，不断更新迭代，保障了我们的 Web 安全研究能力的领先。

你可以直接使用 Pocsuite3 进行漏洞的验证与利用，也可以基于 Pocsuite3 进行 PoC/Exp 的开发，因为它也是一个 PoC 开发框架；同时，还可以在你的漏洞测试工具里直接集成 Pocsuite3，它也提供标准的调用类。


# 功能介绍
#漏洞测试框架
Pocsuite3 采用 Python3 编写，支持验证，利用及 shell 三种模式，你可以指定单个目标或者从文件导入多个目标，使用单个 PoC 或者 PoC 集合进行漏洞的验证或利用。可以使用命令行模式进行调用，也支持类似 Metasploit 的交互模式进行处理，除此之外，还包含了一些基本的如输出结果报告等功能。


# PoC/Exp 开发包
Pocsuite3 也是一个 PoC/Exp 的 SDK，也就是开发包，我们封装了基础的 PoC 类，以及一些常用的方法，比如 Webshell 的相关方法，基于 Pocsuite3 进行 PoC/Exp 的开发，你可以只要编写最核心的漏洞验证部分代码，而不用去关心整体的结果输出等其他一些处理。基于 Pocsuite3 编写的 PoC/Exp 可以直接被 Pocsuite3 使用，Seebug 网站也有几千个基于 Pocsuite3 的 PoC/Exp。

# 可被集成模块
Pocsuite3 除了本身直接就是一个安全工具外，也可以作为一个 Python 包被集成进漏洞测试模块。你还可以基于 Pocsuite3 开发你自己的应用，我们在 Pocsuite3 里封装了可以被其他程序 import 的 PoC 调用类，你可以基于 Pocsuite3 进行二次开发，调用 Pocsuite3 开发你自己的漏洞验证工具。

# 集成 ZoomEye、Seebug、Ceye、Shodan 等
Pocsuite3 还集成了 ZoomEye、Seebug、Ceye 、Shodan 等众多安全服务的 API，通过该功能，你可以通过 ZoomEye API 批量获取指定条件的测试目标（通过 ZoomEye 的 Dork 进行搜索），同时通过 Seebug API 读取指定组件或者类型的漏洞的 PoC 或者本地 PoC，进行自动化的批量测试，利用 Ceye 验证盲打的 DNS 和 HTTP 请求。

# 一些特性
* 支持 verify、attack、shell 三种模式，不仅为扫描而生，也可用于其他场景，比如漏洞利用、获取目标的交互式 shell
* 从任何地方动态加载 PoC 脚本（本地文件、redis、数据库、Seebug...）
* 从任何地方加载目标（CIDR、本地文件、redis、数据库、ZoomEye...）
* 结果可以轻松导出
* 插件系统，用户可自定义 TARGETS、POCS、RESULTS 类型插件，可拓展性强
* 动态 hook urllib3、requests，方便 PoC 编写及全局控制
* 既可以当成一个命令行工具使用，也可以当成 Python 模块导入
* IPv4/IPv6 支持
* 全局 HTTP/HTTPS/SOCKS 代理支持
* 支持 YAML 格式 PoC，与 nuclei 的 PoC 模版兼容
* 集成 Seebug (通过 Seebug API 读取指定组件或者类型的漏洞的 PoC)
* 集成 ZoomEye、Shodan 等网络空间搜索引擎 (通过 API 批量获取测试目标)
* 集成 Ceye、Interactsh (DNSLog 盲打平台)
* 业界良心，代码全开源
* 更多

和 Metasploit 相比，Pocsuite3 目前不具有后渗透阶段的能力，比较轻量级。而相比于 YAML 格式的 PoC 框架，Pocsuite3 更加灵活，可以直接使用大量的第三方库，用户只要会写 Python，就能快速上手。

从 2.0.0 版本开始，Pocsuite3 支持 YAML 格式的 PoC，兼容 nuclei，可以直接使用 nuclei template。


