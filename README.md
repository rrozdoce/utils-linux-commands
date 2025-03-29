# One of the best linux commands i know

## 📂 File and Directory Management
```sh
man # view command manual ex: man ls  
touch # create a file ex: touch file.txt  
mkdir -p # create directory ex: mkdir -p folder/subfolder  
rm -f # permanently delete file/directory ex: rm -f file.txt  
trash # requires "trash" package – moves file/directory to trash ex: trash file.txt  
cp -r # copy file to directory ex: cp -r source/ destination/  
mv    # move or rename files/directories ex: mv old.txt new.txt  
ls -l # list files in detailed format  
find  # search for files/directories ex: find /path -name "*.txt"  
```

## 🔍 Search and View

```sh
grep # search for patterns in files ex: grep "text" file.txt  
cat  # display file content ex: cat file.txt  
less # view files with pagination (better than `cat` for large files) ex: less file.log  
head -n # show first lines of file ex: tail -n 10 file.log  
tail -n # show last lines of file  
```

## ⚙️  System and Processes

```sh
ps aux # list running processes ex: ps aux | grep "nginx"  
kill   # terminate a process ex: kill -9 PID  
top    # monitor processes and resource usage ex: htop  
htop   # ''''''''  
df -h # show disk space ex: df -h  
du -sh # display directory size ex: du -sh /folder/  
```

## 🌐 Network and Internet

```sh
ping # test connectivity to a host ex: ping google.com  
curl # download files from the internet ex: curl -O URL  
wget  
ssh  # connect to a remote server ex: ssh user@host  
ip a # show network info (replaces ifconfig) ex: ip a  
```

## 🛠️ Useful Utilities
```sh
chmod # change file permissions ex: chmod +x script.sh  
chown # change file owner ex: chown user:group file  
tar   # compress/extract files ex: tar -xzvf file.tar.gz  
alias # create command shortcuts ex: alias ll='ls -la'  
```

## 📌 Extra Tips
- Use `Ctrl + C` to interrupt a command
- Use `Ctrl + R` to search command history
-  Always check the manual with `man comando` before using unfamiliar flags

## 🔗 Useful References
- [ExplainShell](https://explainshell.com/) - Explains each part of a command
- [TLDR Pages](https://tldr.sh/) - Simplified version of `man`

## Extras: Windows 11 commands

### Useful Command Prompt (CMD) Commands

```sh
ipconfig # Show network info (IP, gateway, DNS, etc.)  
ipconfig /release # release IP  
ipconfig /renew   # renew IP  
ipconfig /flushdns # Clear DNS cache  
ping # Test connection to server or website  
tracert # Trace route packets take to destination  
netstat # Show active network connections  
netstat -ano # List all connections with PIDs  
tasklist # list running processes  
taskkill /im process_name.exe /if # force close a program  
chkdsk # check and repair disk errors ex: chdsk C: /f  
sfc /scannow # scan and repair corrupted system files  
diskpart # advanced disk management tool (partitioning, formatting)  
shutdown /s /t 0 # Shut down PC immediately  
shutdown /r /t 0 # Restart PC  
shutdown /h      # Hibernate  
```

### PowerShell Commands (More powerful than CMD)
```sh
Get-Process # List running processes  
Stop-Process -Name "process_name" -Force # terminate process  
Get-NetAdapter # Show network adapter info  
Test-NetConnection # Test connectivity to host (similar to `ping`)  
Get-WindowsUpdateLog # Generate Windows update log  
Get-Disk             # Show disk info  
Get-Partition        # Show partition info  
Set-ExecutionPolicy  # Allow script execution in PowerShell (useful for automation)  
```

### Windows 11 Keyboard Shortcuts
- `Win + A` → Open Action Center.
- `Win + E` → Open File Explorer.
- `Win + I` → Open Windows Settings.
- `Win + X` → Advanced context menu (quick access to tools).
- `Win + V` → Clipboard History.
- `Win + Ctrl + D` →  Create new virtual desktop.
- `Win + .` ou `Win + ;` → Open emoji/symbol menu.
- `Win + Shift + S` → Screenshot tool.
- `Win + Ctrl + Shift + B` → Restart video driver (useful if screen freezes).

### Ferramentas avançadas Windows 11
- `msconfig` → System Configuration (startup, services).
- `devmgmt.msc` → Device Manager.
- `diskmgmt.msc` → Disk Management.
- `services.msc` → Windows Services.
- `eventvwr.msc` → Event Viewer (system logs).
- `gpedit.msc` → Group Policy Editor (Pro/Enterprise only).
- `taskmgr` → Task Manager.
- `control` → Traditional Control Panel.

# Windows Package Manager (Winget)
Winget is the official Windows package manager, introduced by Microsoft to simplify installing, updating, and removing apps via command line (CMD or PowerShell). It comes built into Windows 11 (and is also available for Windows 10 starting with version 1809 with updates).

```sh
winget search <package> # ex: chrome  
winget install <package_name/app> # ex: Google.Chrome/Mozilla.Firefox/Microsoft.VisualStudioCode  
winget install --d=<package_name> # id specifies exact app  
# ex:  
winget install --id=Notepad++.Notepad++ --version 8.6.2  

winget list --name <package_name> # ex: chrome  
winget upgrade                   # List apps with available updates  
winget upgrade --id <package_name> # Update specific app  
winget upgrade --all              # Update all apps  
winget uninstall <app_name>    # Uninstall a program  
# ex:  
winget uninstall Google.Chrome  
winget uninstall --id=Adobe.Acrobat.Reader.64-bit  

# Export and Import App Lists  
winget export -o apps.json  
winget import -i apps.json  

# Show App Info  
winget show <app_name>  
# ex:  
winget show Microsoft.PowerToys  

# Clear Winget Cache  
winget cache clean # Remove temporary files from installations.  
```

## Advantages of Using Winget
- ✅ Silent installation (great for scripts and automation).
- ✅ Batch updates (avoids outdated versions).
- ✅ Integration with Microsoft's official repository (also supports external sources).
- ✅ More secure (avoids downloading from untrusted sites).

## Common Issues and Solutions
- ❌ "Winget not recognized" → Update Windows or install App Installer from Microsoft Store.
- ❌ Installation failure → Run terminal as Admin or use --force.
- ❌ App not found → Verify exact name with winget search.

### Practical Example (Install Useful Tools at Once)

```sh
winget install Microsoft.PowerToys
winget install Telegram.TelegramDesktop
winget install VideoLAN.VLC
winget install 7zip.7zip
winget install ObsProject.OBSStudio
```
