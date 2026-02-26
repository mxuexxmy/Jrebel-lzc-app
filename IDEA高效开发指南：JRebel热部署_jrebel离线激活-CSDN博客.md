Python3.11

Python 是一种高级、解释型、通用的编程语言，以其简洁易读的语法而闻名，适用于广泛的应用，包括Web开发、数据分析、人工智能和自动化脚本

<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983508192-62a67e0b-1c79-42b4-bb0e-5a732b43994d.png)

#### 背景：
作者也为每次改完代码都要重新编译后再重启项目的问题苦恼，之前使用的2022版本IDEA和[JRebel](https://so.csdn.net/so/search?q=JRebel&spm=1001.2101.3001.7020)，但最近更新IDEA版本后发现网上并没有或者说并不好找对应的新版的JRebel的使用方法，而原来的2022的方法也没办法使用JRebel了，为此特意将在网上搜罗到的千奇百怪的使用方法尝试完成之后，整理了这个可行的新版JRebel使用方法。

### 一、简介
#### JRebel是什么？
JRebel是一款**高效的Java热部署插件**，允许开发者在修改代码后无需重启应用即可实时生效。它直接作用于JVM层，支持绝大多数框架（Spring、Tomcat、Hibernate等），显著提升开发效率。

#### 相似插件对比
| 插件名称 | 支持范围 | 热部署能力 | 易用性 |
| --- | --- | --- | --- |
| **JRebel** | 全栈支持 | 类/方法级实时更新 | ⭐⭐⭐⭐⭐ |
| Spring Boot DevTools | 仅Spring Boot | 有限支持(不含静态资源) | ⭐⭐⭐⭐ |
| HotSwapAgent | 基础Java | 配置复杂 | ⭐⭐ |


#### 为什么推荐JRebel
+ **全栈支持**：覆盖Java/Kotlin/资源文件/主流框架
+ **0重启耗时**：增量更新节省90%重启时间
+ **企业级稳定性**：无社区版兼容性问题
+ **实时可视化**：IDE内更新状态实时监控

### 二、如何安装JRebel插件
#### 方法1：IDEA插件市场安装
1. 打开IDEA → `File` → `Settings` (Windows) / `Preferences` (macOS)
2. 选择 `Plugins` → `Marketplace`
3. 搜索 `JRebel`→ 点击 `Install`  
这里我已经下载过了，你们直接下载就行  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983508728-dd0b2697-d4b7-4dec-b233-4c54b99a6b5d.png)
4. 下载完成后重启IDEA生效

#### 方法2：手动下载安装
1. 访问 [IDEA官网插件JRebel下载页](https://plugins.jetbrains.com/plugin/4441-jrebel-and-xrebel/versions)选择需要的版本下载  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983508699-e7b22131-adef-4467-b2d4-df4af0f0f810.png)
2. 在IDEA中 `Settings` → `Plugins` → ⚙️图标 → `Install Plugin from Disk...`  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983508717-027c9171-7313-45cc-a915-89632c2d8b7a.png)
3. 选择刚才下载的JRebel插件版本安装
4. 重启IDEA

> ⚠️ 推荐使用**方法1**避免版本兼容问题
>

### 三、激活JRebel
新版本的JRebel需要用点新的手段(使用软件)，2022版本的仅使用uuid的方式已经不太适用了，下面就跟着我一步一步慢慢来

#### 激活步骤
##### `老激活版本`：(已废弃，留做纪念，请跳转到下面新激活版本查看)
1. 访问[Github地址](https://github.com/ilanyu/ReverseProxy/releases/tag/v1.4)选择对应的版本下载  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983508798-6324560f-4507-42b3-a979-2fa233dc6c0a.png)
2. 下载完成后运行exe程序
3. 运行成功后是这样的，注意：**在操作完成之前命令框不能关闭，否则无法成功**  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983508811-2b64f7b1-3ed0-466d-81cb-b0a93826e43c.png)

##### `新激活版本`
1. 访问[最新Github地址](https://github.com/yu-xiaoyao/jrebel-license-active-server/releases/tag/v-20251111)选择对应的版本下载  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509570-4fec05c6-534a-4736-91b0-ca0c49daa257.png)
2. 选择jrebel-license-active-server-windows_amd64.exe下载
3. 下载后双击运行，运行成功后是这样的，注意：**在操作完成之前命令框不能关闭，否则无法成功**  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509298-b84be9b1-04e6-4eff-9310-a4b50fa639e4.png)
4. 访问[随机生成GUID地址](https://www.guidgen.com/)随机生成一个GUID，或者自己使用UUID生成一个随机数  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509370-3eeb86c3-ea49-4cf7-9c56-edaaaa228a9a.png)
5. 打开IDEA，找到Jrebel插件，第一个框填写http://127.0.0.1:12345/{GUID} guid为第四步生成的随机数，第二个框随便填写邮箱（随便乱填也行，只要格式正确即可），**注意：** 激活时，cmd命令行一定不能关闭，且一定要将jrebel设置为在线模式  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509431-f78e331b-f620-4410-b10f-6f5ffebd563a.png)  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509781-17b7f20a-0036-40c8-9c85-b1f67f801b44.png)
6. 点击激活即可，激活成功是这样的  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509595-8e0af17f-7238-444e-97c4-d3f281543a17.png)
7. 完成后设置离线模式  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983509836-9c2c1cd6-4e52-47ec-a9fa-96022d833e5c.png)

> 到这里就完全完成了，cmd运行的命令框也可以关闭了
>

### 四、如何使用JRebel热编译
1.在settings中，打开IDEA的自动编译  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983510022-a58fd698-82df-4b3d-8bba-166b84ef024e.png)  
2.设置热编译间隔时间，即：编写完成后间隔多久自动进行编译，按需设置  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983510104-3ddf3507-0dd6-4474-8163-0c8dc2f84acd.png)  
2.在IDEA左下角（或者正下方，根据IDEA版本不同位置可能不同，作者使用的是IDEA2025）选择需要使用JRebel[热部署](https://so.csdn.net/so/search?q=%E7%83%AD%E9%83%A8%E7%BD%B2&spm=1001.2101.3001.7020)的包，这样以后在对应包下编写的类，在间隔时间到后都会自动进行编译  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983510204-fa2750f9-a449-4d0a-bf62-4a0cdcce5d85.png)  
3.最后使用JRebel运行项目即可体验到热部署的魅力  
<!-- 这是一张图片，ocr 内容为： -->
![](https://cdn.nlark.com/yuque/0/2026/png/266778/1771983510467-4a2dda66-42b0-4783-80ac-98204963b4ad.png)



> 来自: [IDEA高效开发指南：JRebel热部署_jrebel离线激活-CSDN博客](https://blog.csdn.net/MrBInsomnia/article/details/148899208)
>





