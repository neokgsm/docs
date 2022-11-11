# HTB: Starting Point Tier 0 Meow

## Task 解答

1. 頭文字VMは何の意か？  
virtual machine  
<br>

2. VPN接続を開始するときなど、コマンドラインを通してOSに対するコマンドを実行するために使われるツールとは何か？コンソールやシェルともいわれる。  
terminal
<br>

3. HTBのラボにVPN接続する際に使うサービスは何か?  
openvpn
<br>

4. VPN接続開始時の出力において、tunnel interfaceを指す略語は何か？  
tun
<br>

5. ICMPエコーリクエストを用いてターゲットとの接続をテストするツールは何か？  
ping
<br>

6. ターゲット上の開いているポートを見つけるための最も一般的なツールは何か？  
nmap
<br>

7. ポート23/tcp上のサービスは何か？  
telnet  
<how to>$ nmap -T4 -sVC -Pn -v (ターゲットIP) -oA (ファイル名)  
  - T4: スキャン間隔指定  
  - sVC: sV(バージョン確認) + sC(デフォルトのスクリプトを用いてスキャン)  
  - Pn: 事前のping確認をスキップ  
  - v: 詳細を出力
<br>
  
8. パスワードなしでターゲットにログインできるユーザーネームは何か？  
root
<br>
  
9. flag.txt の取得  
9-1. $ telnet (ターゲットIP)  
9-2. Meow login: に root と入れてログイン  
9-3. root@Meow:~# と表示されターゲットを操作できるので  
9-4. ls で何のファイルがあるか見てみるとflag.txtが見つかる。  
9-5. catでflag.txtの内容を出力。以上。
