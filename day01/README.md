# Day1

バイナリエディタでフロッピーディスクの起動イメージファイルを作る。

`!cons_nt.bat` は、単にcmd.exeを起動しているだけなので無視してコマンドプロンプトを起動すればいい。

## qemu

rub.bat ファイルに以下を記述
```
copy helloos.img ..\z_tools\qemu\fdimage0.bin
..\z_tools\make.exe -C ..\z_tools\qemu
```


