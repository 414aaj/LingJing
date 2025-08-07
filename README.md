# LingJing(灵境)  

## 免责声明
该平台仅供网络安全研究与教育用途，旨在提供给具备专业技能的白帽渗透测试人员进行合法的渗透测试和安全评估。非相关人员切勿随意使用或滥用。任何未经授权的网络渗透、入侵或对他人网络的破坏行为均违反法律规定，使用者应对自身行为负责。该平台开发者及分享者不对用户滥用或非法使用平台导致的任何后果承担责任。请务必遵循当地相关法律法规。

<p align="center">
  <img src="https://github.com/user-attachments/assets/10a89330-aab8-42a1-a2ba-eb698b31f77d" alt="image" width="30%" />
</p>

<br>

***

<br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/25a66fbb-c5d3-4ed7-994c-1be57998006f" alt="image" width="95%" />
</p>

## 简介

***LingJing*** 是一款专为复杂网络环境渗透测试量身打造的桌面级本地网络安全靶场平台。支持在线下载和免配置一键部署靶机环境，**平台内置路由**管理、监控打靶流量，快速启动靶机，满足从入门学习到红蓝队实战的流程攻防训练需求。后续版本将更新内置 Attacker 机器，进一步完善渗透测试打靶训练的完整流程，显著提升用户的训练体验和效率。该平台基于 Go+Fyne 构建图形界面，底层采用 QEMU 虚拟化技术，支持跨架构靶机启动。并且**能在 Mac M 系列芯片设备上启动 AMD64 架构靶机**，确保在不同硬件环境下无缝开展测试与训练。

LingJing 平台的靶场资源丰富多样，涵盖开源靶场靶机以及后续原创平台的原创靶机。（正在尝试创新设计一种打靶模式：以 **2D RTS 游戏风格实现互联网侧和近源渗透实景模拟**，为用户带来全新的训练体验（若感兴趣，请予以支持，为创作提供动力））。这些靶场资源覆盖广泛的安全技术方向，满足教育教学、专业培训与实战演练的需求，**包括但不仅限于**：

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

其强大的跨架构兼容性、丰富的靶场资源以及灵活的配置能力，LingJing平台为网络安全学习者和从业者提供了一个高效、真实的实战训练环境，助力每一位用户在网络安全领域快速成长。

  **注：因涉及用户本地与云端靶机镜像下载，为保障用户侧和服务端安全性，平台项目代码不开源。平台相关技术的实现可在脱敏前提下进行讨论分享。**

<br>

***


<p align="center">
  <img src="https://github.com/user-attachments/assets/d383a8ba-e856-4825-9544-7dd606b33eaa" alt="image" width="50%" />
</p>
<br>

<div align="center">
  <strong><font size="28">关注公众号,后台加入灵境测试群聊</font></strong>
</div>

<br>


<div align="center">
  ⚠️⚠️⚠️合作项见文末⚠️⚠️⚠️
</div>
<br>

<br>

***


## 靶场靶机环境

外部靶机:集成开源渗透靶场靶机环境或合作方定制靶场

LingJing靶机:自制原创或实战渗透测试脱敏靶机环境

已部署靶机环境44套:
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

***


<br>
<p align="center">
  【内置Attacker预告】
</p>
由于平台上传限制,视频压缩了画质

https://github.com/user-attachments/assets/0ce4c0fe-0062-446e-9eff-17ec1a9a0ed7

  <p align="center">
<img src="https://github.com/user-attachments/assets/547f3ba0-8d80-4323-b1bc-ab51e67e3d25" width="45%"/> | <img src="https://github.com/user-attachments/assets/5185db8c-5fd0-445a-843a-c8658c0c07ed" width="45%"/>
 </p>
<br><br>

<br>

***

<br>

## 平台已支持系统

- MacOS (Arm64)：已成功测试并兼容 M1、M2 和 M4 芯片的 Mac 设备，M3芯片暂未测试。
- Windows (AMD64)：支持 Windows 10 和 Windows 11 系统，为 Windows 用户提供了稳定的运行环境。Windows 7 不在支持范围内，服务器版本尚未进行测试。

## 下载安装

<details>
  <summary>👈详情</summary>

  
<img src="https://github.com/user-attachments/assets/03611d91-1da3-4dd6-8e6e-372dfb84e8d5" width="45%"/> | <img src="https://github.com/user-attachments/assets/5f02b083-73fb-4ffc-85a7-a627bd0a5e5d" width="45%"/>

  <details>
  <summary>Mac</summary>
把app移动到应用程序里面,在其他路径下运行可能会出错

<p align="center">
  <img src="https://github.com/user-attachments/assets/9d963f63-f2e9-477d-abf1-c854c008427f" alt="image" width="70%" />
</p>



遇到 "LingJing”已损坏，无法打开。你应该将它移到废纸篓。" 执行下面命令

```bash
sudo xattr -rd com.apple.quarantine /Applications/LingJing.app
```

安装依赖

```bash
brew install capstone gnutls pixman jpeg-turbo snappy lzo dtc glib zstd libslirp vde ncurses libusb libssh libpng
```
  </details>

  <details>
  <summary>Windows</summary>
<br>

下载解压后将LingJing文件夹放置合适的盘符位置即可（PS:避开中文目录,否则路由可能无法启动）

    
  初次需要管理员授权安装网卡。
<br>

 <p align="center">
<img src="https://github.com/user-attachments/assets/c86ce993-adaf-43cb-98df-3bfc2e875fc8" width="45%"/> | <img src="https://github.com/user-attachments/assets/7aa3d7f2-137c-40a8-8f35-ece4fcd7fef7" width="45%"/>
<img src="https://github.com/user-attachments/assets/15f0d6d7-22e3-466a-8713-1df3dd148daa" width="45%"/> | <img src="https://github.com/user-attachments/assets/10c8e5c0-75b2-44c3-8e4c-6c7af63046db" width="45%"/>
 </p>
 <br>
  网卡安装成功会弹出是否重启物理机弹框(不重启的话联动外部虚拟机软件时,可能无法找到LingJing网卡)，重启后会看到一张名为LingJing的tap网卡,且路由状态为非红色(若网卡安装成功,但路由状态为红色则尝试重启路由)。
<br><br>
<p align="center">
<img src="https://github.com/user-attachments/assets/d1f5514e-b324-4e14-b23c-5b8f299120fd" width="45%"/> | <img src="https://github.com/user-attachments/assets/a76366ab-50a4-4d72-86dc-77bb9d09c1d0" width="50%"/> 
 </p>
 <br>
  点击托盘设置好路径
<br><br>
<p align="center">
  <img src="https://github.com/user-attachments/assets/e1685adb-059b-42b8-8c14-060fb6650c96" width="45%"/> | <img src="https://github.com/user-attachments/assets/162449fd-631a-4022-9198-1f8843b8cffc" width="45%"/>
 </p>
  </details>


</details>

## 使用方法

<details>
  <summary>👈详情</summary>
下载完靶机后启动需要路由为非红色状态且获取到IP地址
 <p align="center">
<img src="https://github.com/user-attachments/assets/ac5a0071-18af-49ce-a3d2-869c591c96d8" width="45%"/> | <img src="https://github.com/user-attachments/assets/2637ac97-bccf-4a2e-9336-4f9a93de524d" width="45%"/> 
 </p>

 

靶机启动后通过IP访问相应服务
<p align="center">
  <img src="https://github.com/user-attachments/assets/6d631812-f24a-456b-a028-be27a6f09cd8" alt="image" width="70%" />
</p>


卸载:Mac直接删除掉app即可,Windows需要从平台卸载网卡(或其他方式手动卸载)


<p align="center">
  <img src="https://github.com/user-attachments/assets/045cd6c6-d7c1-43e4-b922-187021aafb4e" alt="image" width="70%" />
</p>

  </details>

  
</details>




## 外部虚拟机软件联动

<details>
  <summary>👈详情</summary>
Mac Parallels Desktop中虚拟机若使用桥接网络则可以直接对靶机进行访问,若使用内部网络则需要添加路由(路由从平台复制到PD虚拟机中执行命令),若PD虚拟机使用PD内部网络无法反弹Shell

<p align="center">
  <img src="https://github.com/user-attachments/assets/6095ec11-1533-4ec5-bec6-0416317d036f" alt="image" width="70%" />
</p>

Windows VMware虚拟机可添加网卡桥接LingJing网卡(若VMware在添加桥接网卡时未找到LingJing这张网卡则需要重启一下物理机;若虚拟机未能从LingJing网卡获取到DHCP的IP地址可在虚拟机内对桥接的网卡先禁用再启用网卡，若依旧无法获取IP可尝试手动配置与平台路由通网段的IP地址)
<br>
 <p align="center">
<img src="https://github.com/user-attachments/assets/46614d7c-494d-4d8b-b826-2ff1d0a160aa" width="45%"/> | <img src="https://github.com/user-attachments/assets/36759cb2-00bb-49f9-adc8-a969730f3982" width="45%"/>
<img src="https://github.com/user-attachments/assets/1311dc70-69f9-41c1-b07b-792e9f673b6f" width="45%"/> | <img src="https://github.com/user-attachments/assets/5881b53f-06bc-464e-bd1b-f2383efd360e" width="45%"/>
 </p>
  </p>
</details>

## 平台权限
- Mac每次运行平台时需管理员授权(使平台路由桥接到物理网卡)
- Windows只在通过平台安装或卸载网卡时需要管理员授权。

## 异常情况
若遇Bug可通过LingJing平台上的公众号(相对看到消息更快些)或github进行反馈
<details>
  <summary>👈详情</summary>
  若平台因为Bug问题异常退出需要手动清理后台所有进程(若不手动清理进程,进程会持续运行导致再次启动平台后路由无法正常运行或相应靶机无法启动,在结束掉进程后通过平台重启路由或重启平台)
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
  <summary>👈详情</summary>
    1. Writeup:在你的文章中包含LingJing平台项目地址(https://github.com/414aaj/LingJing) 以及平台的使用,将你的文章链接发送到LingJing平台上的公众号,经验证后引入到平台相应的靶机Writeup
    <br><br>
    2. 可在平台存放合作方定制的靶机环境(细节通过LingJing平台上的公众号进行沟通)
    <br><br>
    3. 待续...
  
</details>








