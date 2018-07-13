#Add Store to Windows 10 Enterprise LTSB
For Windows 10 Enterprise 2015 / 2016 LTSB or Windows Enterprise 2015 / 2016 LTSB N
##To install, run Add-Store.cmd as Administrator  
If you do not want App Installer / Purchase App / Xbox identity, delete each one appxbundle before running to install. However, if you plan on installing games or any app with in-purchase options, you should include everything.  
If the store still will not function, reboot. If still not working, open the command prompt as the administrator and run the following command, then reboot once more.  
```PowerShell -ExecutionPolicy Unrestricted -Command "& {$manifest = (Get-AppxPackage Microsoft.WindowsStore).InstallLocation + '\AppxManifest.xml' ; Add-AppxPackage -DisableDevelopmentMode -Register $manifest}"```  
##Addition troubleshooting:  
>Right click start  
Select Run  
Type in: WSReset.exe  
This will clear the cache if needed.  
  
#为Windows 10 Enterprise LTSB增加应用商店
适用于Windows 10 Enterprise 2015 / 2016 LTSB or Windows Enterprise 2015 / 2016 LTSB N
##要开始安装, 请打包下载后用右键管理员运行 Add-Store.cmd 
如果您不想安装App Installer / Purchase App / Xbox，请在运行安装之前删除对应的.appxbundle后缀的文件。但是，如果您计划安装游戏，或带有购买选项的应用，则不要删除。  
如果装完之后商店仍然打不开，请先重启试试。如果仍然不行，请以管理员身份打开命令提示符并运行以下命令之后，然后再重启试试。
```PowerShell -ExecutionPolicy Unrestricted -Command "& {$manifest = (Get-AppxPackage Microsoft.WindowsStore).InstallLocation + '\AppxManifest.xml' ; Add-AppxPackage -DisableDevelopmentMode -Register $manifest}"```  
##商店修复:  
Win+R打开运行，输入WSReset.exe回车。  
该命令会清空并重置Windows Store商店的所有缓存。  

该脚本由abbodi1406贡献：  
https://forums.mydigitallife.net/threads/add-store-to-windows-10-enterprise-ltsc-ltsb.70741/page-22#post-1419464
