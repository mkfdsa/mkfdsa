## Powershell コマンドまとめ

- `sudo firewall-cmd --list-all --permanent`  
Firewall設定を確認してHTTPポートが解放されているか

## cmd コマンドまとめ
- windows内のアプリケーションによって開放されているポート確認方法  
 1. 現在開放されているポートの確認  
    `netstat -nao | find "目的のポート番号"`
 2. 1で出てきたリストからPIDを調べる
  
```
  C:\>netstat -nao | find "8080"  
  プロトコル   ローカル アドレス       外部アドレス            状態             PID
  TCP         0.0.0.0:8080           0.0.0.0:0              LISTENING       13776  
  TCP         [::]:8080              [::]:0                 LISTENING       13776
```
  3. 2で見つけたPIDをタスクマネージャーから探して、アプリケーションを調べる

- ポートが開いているか確認  
`Test-NetConnection -ComputerName 相手のIPアドレス -Port 確認するポート番号` 

- 

## Linux コマンドまとめ
- traceroute google.com
- ネットワーク経路をリスト表示する
`tracert グローバルIP or URL`

https://www.bioerrorlog.work/entry/install-nmap-on-windows

## Network 系 コマンドまとめ

- __nmap__ 特定のローカルIPアドレスの開放されているポートの確認  
    - インストール方法  
        - Windows
        [windows側のインストール手順](https://www.bioerrorlog.work/entry/install-nmap-on-windows)  
        - Linux (ubuntu)
        `sudo apt-get install nmap`
        - Centos
        `sudo yum install nmap`
    - バージョン確認  
    `nmap --version`
    - 特定のIPアドレスへのポートスキャン  
    `nmap 特定のIPアドレス`
    - その他コマンド  
    [外部URL](https://www.itbook.info/web/2015/06/nmap%E3%81%AE%E5%AE%9F%E7%94%A8%E7%9A%84%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%8910%E9%81%B8.html)

## その他 有用サイト
- グローバルIPのどのポートが開放されているか確認できる
[shodan](https://www.shodan.io/)

## ネットワーク系　知識全般
- localhost = 127.0.0.1 ほぼ同意味  
- docker 内でサーバー立てている場合 localhost = host.docker.internal も一緒
