# security_memo
セキュリティのメモ

## 不審なファイル
```
leanp.exe
nvsvcv.exe
vmatam.exe
vmwere.exe
leassap.exe
nvvscv.exe
vmatap.exe
windump.exe
leassaq.exe
slwga.exe
vmater.exe
leassnp.exe
upsl.dll
vmmat.exe
mdm.exe
vmat.exe
vmnatam.exe
ct.exe
msver.exe
yrar.exe
ss.exe
csvde.exe
mailfinal.exe
GetPassword.exe
mail_noArgv_final.exe
mimikatz.exe
result.log
mimikatzx64.exe
14068.rar
mimikatz1.exe
ms14-068.exe
gp.exe
Gp64.exe
ps.txt
kptl.doc
kenpo.doc

```

## 不審な存在ファイルのチェック
```
dir /a /r /s /b "%TEMP%" "%SystemDrive%\Users\%USERNAME%\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Startup\" "%SystemDrive%\Users\All Users\Microsoft\Windows\Start Menu\Programs\StartUp\" |findstr /I /R "\\leanp\.exe \\nvsvcv\.exe \\vmatam\.exe \\vmwere\.exe \\leassap\.exe \\nvvscv\.exe \\vmatap\.exe \\windump\.exe \\leassaq\.exe \\slwga\.exe \\vmater\.exe \\leassnp\.exe \\upsl\.dll \\vmmat\.exe \\mdm\.exe \\vmat\.exe \\vmnatam\.exe \\ct\.exe \\msver\.exe \\yrar\.exe \\ss\.exe \\csvde\.exe \\mailfinal\.exe \\GetPassword\.exe \\mail_noArgv_final\.exe \\mimikatz\.exe \\result\.log \\mimikatzx64\.exe \\14068\.rar \\mimikatz1\.exe \\ms14-068\.exe \\gp\.exe \\Gp64\.exe \\ps\.txt \\kptl\.doc \\kenpo\.doc"
```


## 自動起動チェック
```
reg query "HKLM\Software\Microsoft\Windows\CurrentVersion\Run" /s |findstr /I /R "\\leanp\.exe \\nvsvcv\.exe \\vmatam\.exe \\vmwere\.exe \\leassap\.exe \\nvvscv\.exe \\vmatap\.exe \\windump\.exe \\leassaq\.exe \\slwga\.exe \\vmater\.exe \\leassnp\.exe \\upsl\.dll \\vmmat\.exe \\mdm\.exe \\vmat\.exe \\vmnatam\.exe \\ct\.exe \\msver\.exe \\yrar\.exe \\ss\.exe \\csvde\.exe \\mailfinal\.exe \\GetPassword\.exe \\mail_noArgv_final\.exe \\mimikatz\.exe \\result\.log \\mimikatzx64\.exe \\14068\.rar \\mimikatz1\.exe \\ms14-068\.exe \\gp\.exe \\Gp64\.exe \\ps\.txt \\kptl\.doc \\kenpo\.doc"
```


## 通信チェック
```
netstat /nao
```


## タスクリストよりプログラムを確認
```
tasklist /FI "PID eq 5348"
```

↓

```
C:\Users\m_shi_000>tasklist /FI "PID eq 2240"

イメージ名                     PID セッション名     セッション# メモリ使用量
========================= ======== ================ =========== ============
Dropbox.exe                   2240 Console                    1    106,992 K

C:\>
```




