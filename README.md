# LingJing(灵境)  

## 免责声明
该平台仅供网络安全研究与教育用途，旨在提供给具备专业技能的白帽渗透测试人员进行合法的渗透测试和安全评估。非相关人员切勿随意使用或滥用。任何未经授权的网络渗透、入侵或对他人网络的破坏行为均违反法律规定，使用者应对自身行为负责。该平台开发者及分享者不对用户滥用或非法使用平台导致的任何后果承担责任。请务必遵循当地相关法律法规。


## 简介

<p align="center">
  <img src="https://github.com/user-attachments/assets/10a89330-aab8-42a1-a2ba-eb698b31f77d" alt="image" width="30%" />
</p>



LingJing 是一款专为复杂网络环境渗透测试需求打造的本地网络安全靶场平台。该平台基于 Go+fyne 开发，支持单靶机、多层内网以及域环境等多种场景。旨在为网络安全研究人员、渗透测试人员以及相关专业学生提供一个高度灵活且功能强大的实战演练环境，助力用户全方位提升网络安全攻防能力。

- 特点1:靶机环境可通过平台一键下载 免配置 安装,实现高效部署。
- 特点2:靶机启动时间控制在 5 至 30 秒,具体耗时与物理机性能密切相关。
- 特点3:靶机通信由平台内部路由进行严格控制,禁止出网访问,保障网络环境安全稳定。
- 特点4:平台具备在线更新功能，可及时同步最新版本。
<br><br><br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/d383a8ba-e856-4825-9544-7dd606b33eaa" alt="image" width="50%" />
</p>

<br>

<div align="center">
  ⚠️⚠️⚠️合作项见文末⚠️⚠️⚠️
</div>

<br><br>

<details>
  <summary>👈👈👈👈👈👈👈👈视频演示</p>
  </summary>
<details>
  <summary>Mac</summary>
  
  待更...
  
</details>

<details>
  <summary>Windows</summary>
    
  待更...
  
</details>

</details>

<br><br><br>

## 平台支持系统
MacOs Arm 64(已测试M1 M2 M4)、Windows Amd 64(已测试win10 win11)

## 安装

<details>
  <summary>👈详情</summary>

  <details>
  <summary>Mac</summary>
把app移动到应用程序里面,在其他路径下运行可能会出错
<p align="center">
  <img src="https://github.com/user-attachments/assets/8ce36fd2-ea34-4c5f-8787-f778f8e2da30" alt="image" width="70%" />
</p>


遇到 "LingJing”已损坏，无法打开。你应该将它移到度纸篓。" 执行下面命令

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
  初次需要管理员授权安装网卡。
<br>
 <p align="center">
<img src="https://github.com/user-attachments/assets/10c8e5c0-75b2-44c3-8e4c-6c7af63046db" width="45%"/> | <img src="https://github.com/user-attachments/assets/a2be711b-3c1b-41a0-8089-10bc11dedf95" width="45%"/>
 </p>
 <br>
  网卡安装成功后会看到一张名为LingJing的tap网卡,且路由状态为非红色(若网卡安装成功,但路由状态为红色则尝试重启路由)。
<br><br>
<p align="center">
< <img src="https://github.com/user-attachments/assets/bb891ff2-26a2-45af-8e36-bf9342a3e3f0" width="45%"/> |<img src="https://github.com/user-attachments/assets/589af388-e29a-40bf-a9aa-2cdca3b42707" width="45%"/>
 </p>
  </details>


</details>

## 使用方法

<details>
  <summary>👈详情</summary>

下载完靶机后启动需要路由为非红色状态且获取到IP地址
 <p align="center">
<img src="https://github.com/user-attachments/assets/74fbb298-e240-478e-84af-cee4188d9d9a" width="45%"/> | <img src="https://github.com/user-attachments/assets/4b46c75c-34fa-4531-a46b-d6c2591b3350" width="45%"/> 
 </p>

靶机启动后通过IP访问相应服务(mac版暂时无法通过平台复制按钮对IP进行复制)
<p align="center">
  <img src="https://github.com/user-attachments/assets/f20ffafe-8c1f-4641-a870-3062766efb60" alt="image" width="50%" />
</p>

卸载:mac直接删除掉app即可,windows需要从平台卸载网卡(或其他方式手动卸载)

<p align="center">
  <img src="https://github.com/user-attachments/assets/08754866-49ff-48f6-9b38-ad24cb2af925" alt="image" width="50%" />
</p>

  </details>

  
</details>



## 靶机
外部靶机:集成开源渗透靶机环境或合作方定制靶场

LingJing靶机:自制或原创渗透测试靶机环境

## 外部虚拟机软件联动

Mac Parallels Desktop中虚拟机若使用桥接网络则可以直接对靶机进行访问,若使用内部网络则需要添加路由(路由从平台复制到PD虚拟机中执行命令,mac暂时无法从复制按钮获取内容),若PD虚拟机使用PD内部网络无法反弹Shell

<p align="center">
  <img src="https://github.com/user-attachments/assets/30cd8785-d52d-433b-a942-b63fde55fe42" alt="image" width="50%" />
</p>

Windows VM虚拟机可添加网卡桥接LingJing网卡(若虚拟机未能从LingJing网卡获取到DHCP的IP地址可在虚拟机内对桥接的网卡先禁用再启用网卡，若依旧无法获取IP可尝试手动配置与平台路由通网段的IP地址)



<br>
<p align="center">
<img src="https://github.com/user-attachments/assets/0e34c573-89f8-41bb-857e-69d6fd1a4775" width="50%"/>
<br>

## 权限问题

Mac每次运行需要管理员授权(使平台路由桥接到物理网卡),Windows只在通过平台安装或卸载网卡时需要管理员授权。

## 异常情况
若遇Bug可通过LingJing平台上的公众号(相对看到消息更快些)或github进行反馈
<details>
  <summary>👈详情</summary>
  若平台因为Bug问题异常退出需要手动清理后台所有进程(若不手动清理进程会后台持续运行,并且再次启动平台后路由无法正常运行,在结束掉进程后通过平台重启路由或重启平台)
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
  <img src="https://github.com/user-attachments/assets/973c5823-395d-47f4-a2dd-72eb8db288c4" width="50%"/>
  </p>
</details>

## 合作项

<details>
  <summary>👈详情</summary>
    1. Writeup:在你的Writeup文章中包含LingJing平台项目地址(https://github.com/414aaj/LingJing) 以及平台的使用,将你的文章的链接发送到LingJing平台上的公众号,经验证后引入到平台相应的靶机Writeup中
    <br><br>
    2. 可在平台存放合作方定制的靶机环境(细节通过LingJing平台上的公众号进行沟通)
    <br><br>
    3. 待续...
  
</details>








