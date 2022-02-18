# Day1

バイナリエディタでフロッピーディスクの起動イメージファイルを作る。

`!cons_nt.bat` は、単にcmd.exeを起動しているだけなので無視してコマンドプロンプトを起動すればいい。98系はcommand、NT系はcmdとなっているだけ。

## qemu での起動

rub.bat ファイルに以下を記述
```
copy helloos.img ..\z_tools\qemu\fdimage0.bin
..\z_tools\make.exe -C ..\z_tools\qemu
```

## フロッピーディスクでの起動

本に指示のある `imgtol.com` は16bitプログラムなので、Windows10では動かない。そのためWindowsXPの古いマシンを持ってきて、XP上で動かした。なおWindowsXPは、SP2までの場合USBメモリ4GB以上は扱えない。このためUSBメモリで持って行く場合は注意。1GBくらいの小容量のUSBメモリを用意しておくと良い。

`imgtol.com` でのイメージ書き込みの際、フロッピーディスクは事前にFATでフォーマットしておく必要がある。アンフォーマット状態のディスクでは書き込みエラーになる。

正常に書き込みが完了した後に、PCを再起動してFDから起動するとhello, worldが出た。機種はLenovo X220 + Windows XP Pro。

