<h2 align="center">
   Context Menu Registries    
</h2>

<h3 style="font-size: 15px font-weight: italics; text-shadow: 2px 2px darkred; color: white;"> Tools: </h3>

<h4>

User Account Control [UAC](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/user-account-control/): </h4>

<div style="font-size: 13px;">
<b>Recommended:</b> <i>Secure dimmed desktop highest privileges.</i></div>
<div style="font-size: 10px;">

<Details open> <Summary> <h6>UAC options:</h6> </Summary>
   </ul>
   <div class="small-padding" style="font-size: 10px;"> 
   <ul>
      <li><b>0</b>: No prompt.</li>
      <li><b>1</b>: Windows settings changes .</li>
      <li><b>2</b>: Secure dimmed desktop.</li>
      <li><b>3</b>: Sys settings <i>not related</i> to Windows</li>
      <li><b>4</b>: Sys settings <i>not related</i> to Windows (no pw).</li>
   </ul></div>
</Details>

Switch <b>TrustedInstaller <b>Full Control Permissions to</b> &rarr; <b>Admin</b>.<br>

[``UAC.bat``](https://github.com/EstebanMqz/Registries/blob/main/.bat/UAC.bat) 

```CMD
@echo on
rem Windows Registries Admin Consent behavior.
reg add HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System /v ConsentPromptBehaviorAdmin /t REG_DWORD /d 2 /f &
runas /user:Administrator "rundll32.exe keymgr.dll,KRShowKeyMgr"
```

[ConsentPromptBehaviorAdmin](https://docs.microsoft.com/en-us/windows/security/identity-protection/user-account-control/user-account-control-group-policy-and-registry-key-settings/ConsentPromptBehaviorAdmin)


[``services.ps1``](https://github.com/EstebanMqz/Registries/blob/main/.ps1/services.ps1) 

<div style="font-size: 12px;">

<h2 div style="font-size: 15px"> 
&#x1F4C1; Context Menus & Commands</h2>  
 
[Environment Variables](https://docs.microsoft.com/en-us/windows/deployment/usmt/usmt-recognized-environment-variables) </b>  
<br>


1. [![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)](https://git-scm.com/) &nbsp; <b>Bash, GUI & gitk. <br>
   [``Bash.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/bash.reg) &emsp; [``Git-Gui.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/bash.reg) &emsp; [``gitk.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/bash.reg) <br><br>

<div style="height: 2px; background: linear-gradient(to right, darkblue, blue);"></div>
<br>

2.  [![CMD logo](https://img.shields.io/badge/CMD-000000.svg?style=flat&logo=windows-terminal&logoColor=white)](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/cmd) <br>
    [``CMD.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/CMD.reg)

<div style="height: 2px; background: linear-gradient(to right, darkblue, blue);"></div>
<br>

<b>3. &nbsp; &nbsp; PowerShell & PowerShell GUI @ &#x1F4C1;</b>&emsp;

Icon's registry [Powershell.exe](https://github.com/PowerShell/PowerShell) <i>double-back-slashed <b></i>.reg</b></i> <b>PATH:</b></span>

```powershell
Write-Output(([System.Diagnostics.Process]::GetCurrentProcess().MainModule.FileName)).replace('\', '\\') #PowerShell terminal
```

<br>

<div style="height: 2px; background: linear-gradient(to right, darkblue, blue);"></div>

<b>4. &nbsp;   &nbsp; [``PowerShell.reg``](https://github.com/EstebanMqz/Registries/blob/main/PowerShell.reg)
   &nbsp; [<img width="18px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/PowerShell_5.0_icon.png/18px-PowerShell_5.0_icon.png">](https://docs.microsoft.com/en-us/powershell/) <br>

<b>5. &nbsp; &nbsp; [``VSCode.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/VSCode.reg) 
   &nbsp; [<img width="18px" src="https://www.svgrepo.com/show/374171/vscode.svg">](https://docs.microsoft.com/en-us/powershell/)</b><br>

<b>6. &nbsp; &nbsp; [``PyCharm.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/PyCharm.reg) 
   &nbsp; [<img width="18px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/PyCharm_Icon.svg/512px-PyCharm_Icon.svg.png">](https://www.jetbrains.com/pycharm/)</b><br>

<b>7. &nbsp; &nbsp; [``Anaconda.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/Anaconda.reg)
&nbsp; [<img width="18px" src="https://www.dataquest.io/wp-content/uploads/2022/01/anaconda-icon.webp">](https://www.anaconda.org)</b><br>

<b>8. &nbsp; &nbsp; [``Notepad.reg``](https://github.com/EstebanMqz/Registries/blob/main/.reg/Notepad.reg) &nbsp; [<img width="18px" src="https://img.icons8.com/?size=48&id=82ixf4KHn6za&format=png">](https://icons8.com/icon/82ixf4KHn6za/notepad)</b><br>

   </span>

---

<div align= "center"> 
   <h2>Automatic Linux & Windows Config.</h2>
</div> 
 
<section id="config">

Have User &amp; <b>[System Environment Variables](https://docs.microsoft.com/en-us/windows/win32/procthread/environment-variables)</b> &amp; <b>[PATHs](https://docs.microsoft.com/en-us/windows/win32/procthread/environment-variables#searching-for-directories)</b> at Startup automatically:

<div style="font-size: 15px;">

> **Note:** Only create/edit [`.profile`](https://github.com/EstebanMqz/Registries/blob/main/$HOME/.profile) &amp; [`.bashrc`](https://github.com/EstebanMqz/Registries/blob/main/$HOME/.profile) with a previous &nbsp; <a href="https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.management/checkpoint-computer?view=powershell-5.1"><img src="https://img.shields.io/badge/CMD-Restore_Point-000000.svg?style=flat&amp;logo=powershell&amp;logoColor=blue" alt="CMD-Restore_Point"></a> or [![CMD-xcopy](https://img.shields.io/badge/xcopy-000000.svg?style=flat&logo=windows-terminal&logoColor=white)](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/xcopy) <br>

<div style="font-size: 12px;">
<i>Backup subdir hidden (rm read-only) C: to D:, output.</i>

```bash
cd D: & label D: SSD_ext  #Rename Drive
./external.bat #Backup C in D with /E /H /K /C options.
```

Registry <b>Regex</b> &rarr; <i>Ctrl+Shift+F</i>

<a href="https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/reg-query"><img src="https://img.shields.io/badge/reg_query-000000.svg?style=flat&amp;logo=windows-terminal&amp;logoColor=blue" alt="reg_query"></a> searches in the registry, use the following CMD command:

```CMD
:: CMD Registry Regex
reg query HKEY_CLASSES_ROOT /f "<regex_search>" /s /e
```

```CMD
:: CMD User / System Environment Variables
runas /user:Administrator "%PATH%\System_Environment.bat"

rem Make sure to have the admin password for the admin found in your .crd file (encrypted or not)
rundll32.exe keymgr.dll,KRShowKeyMgr "%PATH%\file.crd"
```

[![.bashrc](https://img.shields.io/badge/~/.bashrc_&_~/.profile-000000.svg?style=flat&logo=git&logoColor=orange)](https://www.gnu.org/software/bash/manual/bash.html#Bash-Startup-Files)

```bash
#Create .bashrc & .profile files in $HOME
cd $HOME
code ~/.bashrc
code ~/.profile

#Load them automatically.
source ~/.profile & ~/.bashrc

#Finished.

#Note that the .sh: .profile & .bashrc loads automatically what the .bat & .ps1 would do in every execution.
#.bashrc & .profile must be in $HOME for them to be loaded,  won't in remote/local repos.
```

</div>

Remotely Loadable Result (.bashrc/.profile):<br>

![Profile Bashrc](images/.bashrc.jpg)

<h3 style="color: ; text-align:left; padding:10px"> 
Author: <br>

[<img width="40px" src="https://img.icons8.com/ios/50/0e55b3/resume-website.png">](https://tinyurl.com/Esteban-Profile)
[<img width="40px" src="https://img.icons8.com/?size=512&id=MR3dZdlA53te&format=png">](https://www.linkedin.com/in/esteban-m-653817205/)
<a href="https://tinyurl.com/2y86e2wa"><img width="35px" src="https://img.icons8.com/color/452/whatsapp--v1.png" alt="WhatsApp"></a>
[<img width="40px" src="https://img.icons8.com/color/452/gmail-new.png">](mailto:emarquez1895@gmail.com)
[<img width="40px" src="https://cdn3d.iconscout.com/3d/free/thumb/free-github-6343501-5220956.png?f=webp">](https://github.com/EstebanMqz?tab=repositories)
[<img width="40px" src="https://img.icons8.com/color/452/gitlab.png">](https://gitlab.com/EstebanMqz) </h3>

<h6 style><i> References:</h6></i>

<div class="centered-content"><p>

<a href="https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/reg">
   <img width="30px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Logo_windows_simples.svg/2280px-Logo_windows_simples.svg.png?f=webp">
</a> &nbsp;
<a href="https://docs.kernel.org">
<img width="30px" src="https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg">
</a>
<a href="https://git-scm.com"><img src = "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Git_icon.svg/25px-Git_icon.svg.png"></a>
&nbsp; <br> <br>

<a href="https://www.gnu.org/software/bash/manual/bash.html" ><img src="https://img.shields.io/badge/Bash-5.1.4-F05032.svg?style=flat&amp;logo=gnu-bash" alt="Windows_Bash">
&nbsp;
<a href="https://docs.microsoft.com/en-us/windows/wsl/">
<img src="https://img.shields.io/badge/WSL-2.0-0078D6.svg?style=flat&amp;logo=windows" alt="WSL">
</a>
<a href="https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/xcopy"><img src="https://img.shields.io/badge/xcopy-000000.svg?style=flat&amp;logo=windows-terminal" alt="xcopy">
</a> &ensp; <a href="https://www.gnu.org/software/bash/manual/bash.html#Bash-Startup-Files">
<a href="https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/reg"><img src="https://img.shields.io/badge/Registry-reg-000000.svg?style=flat&amp;logo=powershell" alt="reg"></a>
<a href="https://docs.microsoft.com/en-us/windows/win32/procthread/environment-variables">
<img src="https://img.shields.io/badge/PATHs-black" alt="PATHs">
</a>
<a href="https://docs.microsoft.com/en-us/windows/win32/procthread/environment-variables">
<img src="https://img.shields.io/badge/User-Environment-black" alt="User Env Variables">
</a>
<a href="https://docs.microsoft.com/en-us/windows/win32/procthread/environment-variables">
<img src="https://img.shields.io/badge/System-%20Environment-black" alt="System Env Variables">
</a>
</a>

</div>

<i> Verification </i> <br>

```bash
printenv #Environment Variables that define the behavior of OS processes.
$PATH #Directories related to every executable. 
```

<br><br>

See also: [GPG-RSA 4096 bits Encryption](https://github.com/EstebanMqz/GPG-RSA-Git-encryption-1026-4096bits#references)
