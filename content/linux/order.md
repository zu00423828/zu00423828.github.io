+++
date = '2025-02-03T20:23:19+08:00'
draft = false
title = 'Order'
+++

# 常用的 Linux 指令

Linux 是一個強大的操作系統，擁有眾多命令來進行系統管理和日常操作。以下是一些常用的 Linux 指令及其簡要說明。

---

## 系統相關

### 1. `uname`
顯示系統信息。
- `uname -r`：顯示內核版本。
- `uname -a`：顯示全部系統信息（內核、主機名、處理器架構等）。

### 2. `top`
顯示系統的當前運行狀況，包括 CPU 使用率、內存使用量等。

### 3. `df`
顯示文件系統的磁碟空間使用情況。
- `df -h`：以人類可讀格式（例如 GB）顯示磁碟空間。

### 4. `free`
顯示內存使用情況。
- `free -h`：以人類可讀格式顯示內存使用情況。

### 5. `uptime`
顯示系統已運行的時間、用戶數量及負載平均值。

---

## 文件和目錄操作

### 1. `ls`
列出目錄中的文件和子目錄。
- `ls -l`：列出詳細信息。
- `ls -a`：列出所有文件（包括隱藏文件）。

### 2. `cd`
更改當前目錄。
- `cd /path/to/directory`：切換到指定目錄。

### 3. `pwd`
顯示當前工作目錄的完整路徑。

### 4. `mkdir`
創建一個新目錄。
- `mkdir new_directory`：創建名為 `new_directory` 的目錄。

### 5. `rmdir`
刪除一個空目錄。

### 6. `rm`
刪除文件或目錄。
- `rm file.txt`：刪除文件。
- `rm -r directory`：遞歸刪除目錄及其內容。

### 7. `cp`
複製文件或目錄。
- `cp source.txt destination.txt`：複製文件。
- `cp -r source_dir destination_dir`：複製目錄。

### 8. `mv`
移動或重命名文件/目錄。
- `mv old_name.txt new_name.txt`：重命名文件。
- `mv file.txt /path/to/destination/`：將文件移動到新目錄。

---

## 檔案內容查看和編輯

### 1. `cat`
查看文件內容。
- `cat file.txt`：顯示 `file.txt` 的內容。

### 2. `more` 和 `less`
逐頁顯示文件內容。
- `more file.txt`：逐頁顯示文件內容，按空格鍵翻頁。
- `less file.txt`：逐頁顯示文件內容，支持向上滾動。

### 3. `head`
顯示文件的前幾行。
- `head -n 10 file.txt`：顯示文件的前 10 行。

### 4. `tail`
顯示文件的最後幾行。
- `tail -n 10 file.txt`：顯示文件的最後 10 行。
- `tail -f file.txt`：實時顯示文件的新內容（用於查看日志文件）。

### 5. `nano`
文本編輯器，允許在終端內編輯文件。
- `nano file.txt`：編輯 `file.txt`。

---

## 用戶和權限管理

### 1. `whoami`
顯示當前登錄的用戶名。

### 2. `id`
顯示當前用戶的 UID、GID 及所屬組信息。

### 3. `chmod`
更改文件或目錄的權限。
- `chmod 755 file.txt`：設置文件為可讀、可寫和可執行。

### 4. `chown`
更改文件或目錄的所有者和所屬組。
- `chown user:group file.txt`：將 `file.txt` 的擁有者設為 `user`，所屬組設為 `group`。

### 5. `passwd`
更改用戶的密碼。

---

## 網絡相關

### 1. `ping`
檢查網絡連通性。
- `ping www.example.com`：檢查與 `www.example.com` 的連通性。

### 2. `ifconfig`
顯示或配置網絡接口。
- `ifconfig`：顯示當前網絡配置。

### 3. `netstat`
顯示網絡連接、路由表、接口統計等信息。
- `netstat -tuln`：顯示當前的 TCP 和 UDP 端口。

### 4. `ssh`
遠程登錄到另一台計算機。
- `ssh user@hostname`：通過 SSH 連接到遠程計算機。

### 5. `scp`
安全地複製文件到遠程主機。
- `scp file.txt user@remote:/path/to/destination`：將 `file.txt` 複製到遠程主機。

---

## 搜索和查找

### 1. `find`
在指定目錄中查找文件。
- `find /path/to/search -name "*.txt"`：查找 `.txt` 文件。

### 2. `grep`
在文件中查找匹配的行。
- `grep "search_string" file.txt`：查找包含 `search_string` 的行。

### 3. `locate`
快速查找文件（需要事先構建索引）。
- `locate file.txt`：查找名為 `file.txt` 的文件。

---

## 壓縮和解壓

### 1. `tar`
創建或解壓 `.tar` 存檔。
- `tar -cvf archive.tar file1 file2`：創建 `.tar` 壓縮檔案。
- `tar -xvf archive.tar`：解壓 `.tar` 壓縮檔案。

### 2. `gzip` 和 `gunzip`
壓縮和解壓 `.gz` 文件。
- `gzip file.txt`：壓縮文件。
- `gunzip file.txt.gz`：解壓文件。

### 3. `zip` 和 `unzip`
壓縮和解壓 `.zip` 文件。
- `zip archive.zip file1 file2`：創建 `.zip` 壓縮檔案。
- `unzip archive.zip`：解壓 `.zip` 檔案。

---

## 程序管理

### 1. `ps`
顯示當前運行的進程。
- `ps aux`：顯示所有運行的進程。

### 2. `top`
顯示實時的進程信息，並顯示 CPU 和內存的使用情況。

### 3. `kill`
終止進程。
- `kill PID`：終止進程 ID 為 `PID` 的進程。

### 4. `htop`
比 `top` 更加直觀的進程管理工具（需要安裝）。
- `htop`：啟動 `htop` 進程監控。

---

## 系統更新和安裝

### 1. `apt-get`（Debian/Ubuntu）
安裝、更新和卸載軟件包。
- `sudo apt-get update`：更新軟件包索引。
- `sudo apt-get install package_name`：安裝軟件包。
- `sudo apt-get remove package_name`：卸載軟件包。

### 2. `yum`（CentOS/RHEL）
安裝、更新和卸載軟件包。
- `sudo yum update`：更新軟件包。
- `sudo yum install package_name`：安裝軟件包。
- `sudo yum remove package_name`：卸載軟件包。

---

## 日誌和排錯

### 1. `dmesg`
顯示內核環境信息和錯誤。

### 2. `tail -f /var/log/syslog`
實時查看系統日誌。

---

## 其他實用命令

### 1. `alias`
創建命令別名。
- `alias ll='ls -l'`：創建一個 `ll` 別名，等效於 `ls -l`。

### 2. `history`
顯示命令歷史。

---
