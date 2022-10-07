| Open Registry Editor | Description |
| ------ | ------ |
| win + r | Run |
| regedit | Registry Editor |
| Computer\HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Lxss\ | WSL Distributions |

<br><br>


#### Find ext4.vhdx file path of WSL distribution e.g. Ubuntu 22, or Docker Desktop <br>

![grafik](https://user-images.githubusercontent.com/100385444/194547507-7a8a04d6-0095-4d82-88eb-df213c796d6a.png)

<br><br>


#### Shrink ext4.vhdx file

| Using Hyper-V / PowerShell | Description |
| ------ | ------ |
| wsl --shutdown | Shutdown WSL distribution |
| Optimize-VHD -Path <path/to/ext4.vhdx> -Mode Full | Shrink ext4.vhdx file |



| Using DiskPart | Description |
| ------ | ------ |
| diskpart | Start DiskPart |
| select vdisk file="<path/to/ext4.vhdx" | Select vdisk file |
| compact vdisk | Shrink vdisk |
| exit | exit DiskPart |
