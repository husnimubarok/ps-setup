# ps-setup
1. install eza
2. install starship

## Eza setup
Install menggunakan Winget
winget install eza-community.eza

LLanjutkan dengan setting alias di PowerShell

Di terminal, eksekusi perintah berikut untuk membuat Powershell profile:
New-Item -Path $PROFILE -Type File -Force

Edit profile tersebut dengan menjalankan perintah berikut di terminal
notepad .$PROFILE

Kemudian, masukkan alias berikut ke dalam file profile tersebut:
```powershell
function lll { eza --color=always --group-directories-first --icons @args }
function ll { eza -la --icons --octal-permissions --group-directories-first @args }
function l { eza -bGF --header --git --color=always --group-directories-first --icons @args }
function llm { eza -lbGd --header --git --sort=modified --color=always --group-directories-first --icons @args }
function la { eza --long --all --group --group-directories-first @args }
function lx { eza -lbhHigUmuSa@ --time-style=long-iso --git --color-scale --color=always --group-directories-first --icons @args }
function lS { eza -1 --color=always --group-directories-first --icons @args }
function lt { eza --tree --level=2 --color=always --group-directories-first --icons @args }
function l. { eza -a | Select-String -Pattern '^\.' }
```
agar settingan bisa dicoba, jalankan profile yang sudah diupdate tersebut dari terminal
.$PROFILE
