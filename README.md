# LingJing(灵境)  

## 免责声明
本平台仅供网络安全研究与教育用途，旨在提供给具备专业技能的白帽渗透测试人员进行合法的渗透测试和安全评估。非相关人员切勿随意使用或滥用。任何未经授权的网络渗透、入侵或对他人网络的破坏行为均违反法律规定，使用者应对自身行为负责。该平台开发者及分享者不对用户滥用或非法使用平台导致的任何后果承担责任。请务必遵循当地相关法律法规。



<p align="center">
  <img src="https://github.com/user-attachments/assets/10a89330-aab8-42a1-a2ba-eb698b31f77d" alt="image" width="30%" />
</p>



<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/25a66fbb-c5d3-4ed7-994c-1be57998006f" alt="image" width="95%" />
</p>
<br>

<details>
  <summary>👈👈👈【更多】</summary>
<p align="center">
<img src="https://github.com/user-attachments/assets/ba3f45d3-627f-426e-8768-b365238ac846" alt="image" width="90%" />
<br>
<img src="https://github.com/user-attachments/assets/835f6d16-0feb-43ab-845c-10a132b970a5" alt="image" width="90%" />
</details>



***
## 简介

***LingJing*** 是一款专为复杂网络环境渗透测试量身打造的桌面级本地网络安全靶场平台。支持在线下载和**免配置一键部署**靶机环境，**平台内置路由**管理、监控打靶流量，快速启动靶机，满足从入门学习到红蓝队攻防实战的训练需求。后续版本将更新内置 Attacker 机器，进一步完善渗透测试打靶训练的完整流程，显著提升用户的训练体验和效率。本平台基于 Go+Fyne 构建图形界面，底层采用 QEMU 虚拟化技术，支持跨架构靶机启动。并且**能在 Mac M 系列芯片设备上启动 AMD64 架构靶机**，确保在不同硬件环境下无缝开展测试与训练。

LingJing 平台的靶场资源丰富多样，涵盖开源靶场靶机以及本平台后续上线的原创靶机。（正在尝试创新设计一种打靶模式：以 **2D RTS 游戏风格实现互联网侧和近源渗透实景模拟**，为用户带来全新的训练体验（如蒙支持，将为创作提供持续动力））。这些靶场资源覆盖广泛的安全技术方向，满足教育教学、专业培训与实战演练的需求，**包括但不仅限于**：

- Web 安全测试：涵盖 SQL 注入（包括盲注、报错注入、联合查询）、跨站脚本（XSS）、文件上传漏洞、CSRF、命令执行、信息泄露等常见攻击面；
- 内网渗透与域环境攻击：支持多层网络与域控环境部署，适用于横向移动、权限提升、Kerberos 票据滥用、NTLM 中继、域信任攻击等高阶内网技术；
- 中间件与框架漏洞复现：包括 Apache、Nginx、Tomcat、Struts2、Spring 等主流组件的漏洞验证与环境搭建；
- Java 应用安全：集成 Java Web 漏洞、反序列化链分析、安全编码误区等内容；
- 业务逻辑与客户端安全：适用于身份认证绕过、权限控制缺陷、弱加密机制等漏洞的演练和教学；
- 红队攻防与实战演练：支持多跳通信、端口转发、代理链、隧道技术等对抗场景的战术部署与验证。

***平台特点***：

- 高效部署：靶机环境可通过平台一键下载、**免配置安装**，实现高效部署，大大节省时间和精力。
- 秒级启动：单靶机启动时间在 5 至 30 秒（域环境——域成员和域控启动后需要时间建立通信，因此启动速度相对较慢），具体耗时与物理机性能密切相关。
- 严格网络控制：靶机通信由平台内部路由进行严格控制，禁止出网访问，保障网络环境的安全与稳定。
- 在线更新功能：平台具备在线更新功能，可及时同步最新版本，确保用户始终使用最新功能和安全修复。
- 轻量级镜像：镜像压缩体积更小，节省存储空间，便于快速下载和部署。
- 高速下载：靶机镜像采用云端分布式多节点部署，支持断点续传高速下载，进一步提升用户体验。

LingJing平台旨在提升跨架构兼容性、提供丰富的靶场资源以及灵活的配置能力，为网络安全学习者和从业者提供一个高效、真实的实战训练环境，助力每一位用户在网络安全领域快速成长。

  **注：因涉及用户本地与云端靶机镜像下载，为保障用户侧和服务端安全性，平台项目代码暂不开源。如有需求，平台相关技术的实现可在脱敏前提下进行讨论分享。**

<br>

***


<p align="center">
  <img src="https://github.com/user-attachments/assets/d383a8ba-e856-4825-9544-7dd606b33eaa" alt="image" width="50%" />
</p>
<br>

<div align="center">
  <strong><font size="28">关注公众号，加入灵境测试群聊</font></strong>
</div>

<br>


<div align="center">
  ⚠️⚠️⚠️合作项见文末⚠️⚠️⚠️
</div>
<br>

<br>

***


## 靶场靶机环境

外部靶机:集成开源渗透靶场、靶机环境或合作方定制靶场

LingJing靶机:自制原创靶机环境或渗透测试实战脱敏靶机环境

LingJing平台目前已部署靶机环境44套:
  <details>
  <summary>👈👈👈【🔎详情】</summary>
    
- VulnStack 6套
- vulhub 10套
- vulnhub 10套
- vulntarget 7套
- VulNyx 2套
- DVWA 1套
- sqli-labs 1套
- upload-labs 1套
- xss-labs 1套
- pikachu 1套
- WebGoat 1套
- JavaSecLab 1套
- webug 1套
- DVGA 1套
</details>

***


<details>
  <summary>👈👈👈【内置Attacker预告】</summary>
由于平台上传限制，视频压缩了画质

https://github.com/user-attachments/assets/0ce4c0fe-0062-446e-9eff-17ec1a9a0ed7

  <p align="center">
<img src="https://github.com/user-attachments/assets/547f3ba0-8d80-4323-b1bc-ab51e67e3d25" width="45%"/> | <img src="https://github.com/user-attachments/assets/5185db8c-5fd0-445a-843a-c8658c0c07ed" width="45%"/>
 </p>
<br>
</details>

## 平台已适配的物理机系统

- MacOS (Arm64)：已兼容基于M系列芯片的 Mac 设备，但未测试M系列的Mini设备。
- Windows (AMD64)： 已适配 Windows 10/11 家庭版、专业版及英文版；Windows 7 不在支持范围内，服务器版本尚未测试。
 
## 下载安装
 点击👉 <a href="https://mp.weixin.qq.com/s/Z358T7VhKJ18ywTOpRDE7g">Mac安装教程</a>
 <br>
 点击👉 <a href="https://mp.weixin.qq.com/s/Z358T7VhKJ18ywTOpRDE7g">Windows安装教程</a>
## 使用方法



### 外部适配靶机导入

点击👉 <a href="https://mp.weixin.qq.com/s/WJQ9GPaG4FqzGc7pA2LhbQ">外部适配靶机导入教程</a>
  


### 外部虚拟机软件联动
点击👉 <a href="https://mp.weixin.qq.com/s/dlymJ-laE1maBIGVr4pcIw">外部虚拟机软件联动教程</a>

## 平台权限
- Mac物理机每次运行平台时需管理员授权(使平台路由桥接到物理网卡)
- Windows物理机仅在通过平台安装或卸载网卡时需要管理员授权。

## 异常情况

由于不同用户的 Windows 物理机网络环境配置差异较大，某些特殊网络设置可能导致 LingJing 平台运行异常。若在Windows物理机上可以 ping 通 LingJing 平台启动的靶机，却无法访问靶机的任何服务（例如 HTTP、SSH 等端口均无响应），请首先确认 LingJing 虚拟网卡已获取到与 LingJing平台内置路由同网段的合法 IP 地址；若发现LingJing虚拟网卡未获取正常IP地址，请在 LingJing 虚拟网卡的网络适配器上手动配置一个静态 IP 地址（仅保证与虚拟网卡 IP 处于同一网段即可，无需设置网关和 DNS）。

如果遇到问题，您可以通过LingJing平台公众号加入群聊或在GitHub上进行反馈，我们将尽快核查修复。感谢您的支持与宝贵意见。



    
报错:【WGL: The driver does not appear to supportOpenGL】点击👉👉👉 <a href="https://mp.weixin.qq.com/s/GzB0oq5wuKmdMbvKtXBEow?scene=1&click_id=78">解决办法</a>

<details>
  <summary>【🔎👈详情】</summary>
  如果平台因为Bug问题异常退出需要手动清理后台所有进程(若不手动清理进程，进程会持续运行导致再次启动平台后，路由无法正常运行或相应靶机无法启动，请结束进程后通过平台重启路由或重启平台)。
  <br>
  Mac
  <br>
  <p align="center">
  <img src="https://github.com/user-attachments/assets/280c0124-b447-4483-a5ec-694950f8250d" width="45%"/> | <img src="https://github.com/user-attachments/assets/8b5b9275-c679-4fec-b9ea-af2fb5fa7586" width="45%"/> 
  </p>
  <br>
  Winodws
  <br>
  <p align="center">
  <img src="https://github.com/user-attachments/assets/973c5823-395d-47f4-a2dd-72eb8db288c4" width="70%"/>
  </p>
</details>

## 合作项

<details>
  <summary>【🔎👈详情】</summary>
    1. Writeup:在您的文章中包含LingJing平台项目地址(https://github.com/414aaj/LingJing) 以及平台的使用，将您的文章链接发送到LingJing平台上的公众号，经验证后引入到平台相应的靶机Writeup
    <br><br>
    2. 若您有其他合作方式需探讨，敬请与我们联系，共商合作事宜。
    <br><br>
  
</details>

***

 ***<p align="center">
 本项目由个人独立开发维护。若您认可本项目的工作，可通过给GitHub项目加星标或微信公众号文章打赏的方式支持项目持续发展***
</p> 
<br>

***💌 致谢：***

***谨向以下为LingJing平台提供帮助的博主及个人致以诚挚谢意（排名不分先后）：***

  【组织】
<br>
<p align="center">
  红客联盟（弘客数据）
</p> 
【微信公众号】
<br>
<p align="center">
潇湘信安、乌鸦安全、船山信安、破晓实验室、知攻善防实验室、SGY安全、LingJing灵境、Hack分享吧、神农Sec、安全处女座、阿乐你好、白安全组
</p> 
【B站】
<p align="center">
疯狂杨CC
</p> 
【个人】
<br>
<p align="center">
3had0w、crow、ziansd、Cream、疯狂杨CC(ycc77.cn、ycc77.com)、洛晨、vampireC-hhh、Xuds、跃迁、名前のない怪物、pulsar、Du、小机灵、newWRLDcat、钟沐、以后的以后ᯤ⁶ᴳ、Nul1W2y、Smrtni1
</p> 
<br>

***同时向灵境平台所集成的所有开源靶场项目及其贡献者致敬：***

Vulntarget 系列｜VulnStack 红日靶场｜VulNyx｜VulnHub｜vulhub｜DVGA｜DVWA｜JavaSecLab｜WebGoat｜Pikachu｜SQLi-Labs｜Upload-Labs｜xss-labs






