1 . Windows Commands
======

## Windows + R or Cmd
* 命令提示字元 \
```cmd```
* powershell \
```powershell```
* 控制台 \
```control```
* 關於Windows \
```winver```
* 新增或移除程式 \
```appwiz.cpl```
* 元件服務 \
```dcomcnfg```
* DirectX診斷工具 \
```dxdiag```
* 磁碟管理 \
```diskmgmt.msc```
* diskpart \
```diskpart```
* Downlaods資料夾 \
```downloads```
* Documents資料夾 \
```documents```
* 防火牆 \
```firewall.cpl```
* 檔案總管選項 \
```control folders```
* 本機群組原則編輯器 \
```gpedit.msc```
* 安裝或解除顯示語言 \
```lpksetup```
* 本機安全性原則 \
```secpol.msc```
* 本機使用者和群組 \
```lusrmgr.msc```
* 網路連線 \
```ncpa.cpl```
* 電源選項 \
```powercfg.cpl```
* 地區 \
```intl.cpl```
* 登陸編輯程式(註冊表) \
```regedit```
* 遠端桌面連線 \
```mstsc```
* 服務 \
```services.msc```
* 登出 \
```logoff```
* 關機 \
```shutdown -s -t 1```
* 重新啟動 \
```shutdown -r -t 1```
* 系統設定(開機導入) \
```msconfig```
* 工作管理員 \
```taskmgr```
* 工作排程器 \
```taskschd.msc```
* 檔案總管(Windows+E) \
```explorer.exe```

參考網址:<https://ss64.com/nt/run.html>


## Command Line
* 使用者名稱 \
```whoami```
* 查看網路設定 \
```ipconfig /all```
* 目前路徑及切換路徑 \
```cd```
* 列出所有檔案和路徑 \
```dir```
* 創建資料夾 \
```mkdir```
* 刪除資料夾 \
```rmdir```
* 複製檔案 \
```copy```
* 移動檔案 \
```move```
* 刪除檔案 \
```del```
* 重新命名 \
```ren```
* 複製全部資料夾 \
```xcopy```
* 部署映像服務和管理工具 \
```Dism```
* 在CMD上顯示或隱藏 \
```echo```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/echo>
* 搜尋文字 \
```find```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/find>
* 搜尋多個文字 \
```findstr```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/findstr>
* 迴圈 \
```for```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/for>
* 條件式 \
```if```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/if>
* 暫停 \
```pause```
* 測試網路 \
```ping```
* 註解 \
```REM```
* 關機或重新啟動指令 \
```shutdown```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/shutdown>
* 看文字文件資料 \
```type```
* 設置環境變數 \
```set```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/set_1>
* 腳本暫停 \
 ```timeout```
* 腳本跳行 \
```goto```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/goto>
* 顯示網路相關數據 \
```netstat```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/netstat>
* 尋找檔案 \
```where ```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/where>
* 顯示時間 \
```time```
* Regedit應用 \
```reg```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/reg>
* 創建A使用者 \
```net user /add A```
* 將A使用者加入Administrators群組 \
```net localgroup Administrators A /add```
* 設定高效能模式 \
```powercfg /setactive 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c```\
<https://docs.microsoft.com/zh-tw/windows/win32/power/power-policy-settings>

參考網址:
* <https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/windows-commands>
* <https://home.gamer.com.tw/creationDetail.php?sn=3960761>



2 . Diskpart Commands
======
* 查看所有硬碟 \
```list disk```\
```lis dis```
* 選擇第一顆硬碟 \
```select disk 0```\
```sel dis 0```
* 將指定的硬碟清除 \
```clean```
* 轉換硬碟類型 \
```convert gpt```\
```convert mbr```
* 查看所有磁區 \
```list volume```\
```lis vol```
* 選擇第一個磁區 \
```select volume 0```\
```sel vol 0```
* 建立1GB的一般磁區 \
```create partition primary size=1024```
* 建立EFI磁區 \
```create partition efi size=100```
* 建立MSR磁區(GPT專用) \
```create partition msr```
* 刪除磁碟分區 \
```delete partition```
* 磁區轉成NTFS格式並命名為Disk1 \
```format quick fs=ntfs label=Disk1```
* 磁區轉成fat32格式並命名為System \
```format quick fs=fat32 label="System"```
* 指派硬碟代號E槽 \
```assign letter=e```
* 移除磁區代號 \
```remove letter=e```
* 將硬碟離線 \
```offline disk```
* 將硬碟上線 \
```online disk```
* 啟用磁區(MBR專用) \
```Active```
* 查看硬碟或磁區資訊 \
```detail disk```\
```detail vol```
* 縮減500MB磁區大小 \
```shrink desired=500```
* 增加500MB磁區大小 \
```extend size=500```

參考網址:<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/diskpart>



3 . Deploy Commands(Windows底下可直接使用)
======
* 新增開機引導 \
```bcdboot```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/bcdboot-command-line-options-techref-di?view=windows-11>
* 編輯開機引導 \
```bcdedit```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/bcdedit-command-line-options?view=windows-11>
* 擷取C槽資料放在D槽 \
```Dism /Capture-Image /ImageFile:"D:\install.wim" /CaptureDir:C:\ /Name:install```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/iot-ent-sysprep-capture-deploy?view=windows-11>
* 套用install.wim資料到W槽 \
```dism /Apply-Image /ImageFile:D:\install.wim /Index:1 /ApplyDir:W:\```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/iot-ent-sysprep-capture-deploy?view=windows-11>
* 顯示當前系統的安裝包 \
```dism /online /Get-Packages /Format:Table```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/add-language-packs-to-windows?view=windows-11>
* 安裝當前系統的安裝包(語言包) \
```Dism /online /Add-Package /PackagePath:C:\packages\XXX```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/add-language-packs-to-windows?view=windows-11>
* 移除當前系統的安裝包(語言包) \
```Dism /online /Remove-Package /PackageName:XXX```\
<https://docs.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/add-language-packs-to-windows?view=windows-11>
* 修改硬碟類型欄位 \
```set id```\
<https://docs.microsoft.com/zh-tw/windows-server/administration/windows-commands/set-id>



4 . Deploy Image Tool Commands
======
### 1. WinPE前置部署
* 複製WinPE檔案 \
```Copype amd64 C:\WinPE_amd64\```
* 將WinPE 做成USB開機碟Create a bootable WinPE USB drive:\
```MakeWinPEMedia /UFD C:\WinPE_amd64_with_RST P:```


* 將WinPE 做成ISO檔Create a WinPE ISO, DVD, or CD:\
```MakeWinPEMedia /ISO C:\WinPE_amd64 C:\WinPE_amd64\WinPE_amd64.iso```

* 將Boot展開:Mount-Image:\
```Dism /Mount-Image /ImageFile:"C:\WinPE_amd64\media\sources\boot.wim" /index:1 /MountDir:"C:\WinPE_amd64\mount"```

* 查看index \
```dism /Get-WimInfo /WimFile:"C:\WinPE_amd64\media\sources\boot.wim"```\
```dism /Get-WimInfo /WimFile:"C:\WinPE_amd64\media\sources\install.wim"```

*  卸載修改過後的 WinPE 開機資料:Unmount-Image:\
```Dism /Unmount-Image /MountDir:"C:\WinPE_amd64\mount" /commit```


### 2. 因WinPE開啟會預設load startnet.cmd檔,所以可修改該檔script製作成可自動執行檔案的WinPE 
(路徑為C:\WinPE_amd64\mount\Windows\System32\startnet.cmd)


### 3. Add Driver to WinPE:

* Add Driver folder.\
```Dism /Add-Driver /Image:"C:\WinPE_amd64\mount" /Driver:"C:\WinPE_amd64\x64" /recurse```

* Check Driver has in WinPE\
```Dism /Get-Drivers /Image:"C:\WinPE_amd64\mount"```

* 確認key和sysprep\
```slmgr /dlv```

### 4. 如何清除mount 殘留檔案及掛載失敗問題

```DISM /Cleanup-Wim```\
```Imagex /Cleanup```


### 5. Capture Image 
* diskpart:  list vol (看磁區)
* 把 C 槽的系统備份到 D 槽中，備份文件名為 install.wim\
```Dism /Capture-Image /ImageFile:D:\install.wim /CaptureDir:C:\ /Name:Win10 /Description:0000-00-00```

### 6. Apply Image 
* 把 D槽install.wim 中的備份還原到 W槽
```dism /Apply-Image /ImageFile:D:\sources\install.wim /Index:1 /ApplyDir:W:\```


* .FFU是把整顆硬碟所有磁區都抓出來:Capture .FFU file\
```DISM /capture-ffu /imagefile=e:\WinOEM.ffu /capturedrive=\\.\PhysicalDrive0 /name:disk0 /description:"Windows 10 FFU"```

* Apply .FFU file\
```DISM /apply-ffu /ImageFile=N:\WinOEM.ffu /ApplyDrive:\\.\PhysicalDrive0```\
```DISM /apply-image /imagefile:d:\flash.ffu /applydrive:\\.\PhysicalDrive0 /skipplatformcheck```

