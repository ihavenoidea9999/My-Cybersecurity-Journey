apt  
===
Advanced Package Tool  
---
#不確定是不是每個命令都需要 sudo 的前綴（有些命令好像不加 sudo 也可以跑？）
---
# 簡介
- apt（Advanced Package Tool）是 Debian、Ubuntu 中的 Shell 前端軟體套件管理工具，
- apt 命令提供了查找、安裝、升級、刪除某一個、一組、甚至全部軟體套件的命令
- apt 命令執行需要 super user 權限

# 語法  
apt [options] [command] [package ...]  
> [options]  
> > 可選。選項包括  
> > -h（幫助)  
> > -y（安裝過程全部選 yes ）   
> > -q（不顯示安裝過程)
> 
> [command]  
> > 要進行的操作
> 
> [package]  
> > 安裝的套件名

# 常見用法
- sudo apt update  
  > 列出所有可更新的軟體清單指令
- sudo apt upgrade 
  > 升級軟體套件  
  - apt list --upgradable  
  > 列出可更新的軟體套件版本資訊  
  - sudo apt full-upgrade  
  > 升級軟體套件，升級前先刪除需要更新的軟體包  
  - sudo apt list --installed  
  > 列出所有已安裝的套件  
  - sudo apt list --all-versions  
  > 列出所有已安裝的套件的版本資訊  
- sudo apt install <package_name>  
  > 安裝指定的軟體  
  - sudo apt install <package_1> <package_2> <package_3>  
  > 安裝多個軟體  
  - sudo apt install <package_name> --no-upgrade  
  > 安裝某個軟體，但如果該軟體已經存在，則不要升級它  
  - sudo apt install <package_name> --only-upgrade  
  > 升級某個軟體，但如果該軟體不存在，則不要安裝它  
  - sudo apt install <package_name>=<version_number>  
  > 安裝某個軟體的特定版本。  
    注意 <package_name>是軟體名，<version_number>是版本 *號*  
- sudo apt update <package_name>   
  > 更新指定的軟體  
- sudo apt show <package_name>  
  > 顯示軟體套件具體資訊。例如：版本號，安裝大小，依賴關係等等   
- sudo apt remove <package_name>   
  > 刪除軟體   
  - sudo apt autoremove  
  > 清理不再使用的依賴和庫檔案  
- sudo apt purge <package_name>  
  > 移除軟體套件及設定檔  
- sudo apt search <keyword>  
  > 尋找關鍵字相關的軟體套件
---
[菜鳥教程：Linux apt 命令](https://www.runoob.com/linux/linux-comm-apt.html)
