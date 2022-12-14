## Docker 使用したコマンドまとめ

- `docker ps`  
  起動中のコンテナの一覧を出力  
`-a`のオプションを追加することで、すべてのコンテナの一覧が出力される  
 
 - `docker container run`  
  「イメージの取得」「コンテナの作成」「コンテナの起動」を連続して行う
  
 - `docker start <コンテナ名 or コンテナID>`  
  	コンテナを起動
    
 - `docker stop <コンテナ名 or コンテナID>`  
  	コンテナを停止
    
 - `docker exec -it コンテナ名 bash`  
  	動作しているコンテナに入る
 
 - `docker port コンテナ名`  
  コンテナ内で、公開されているポート番号がホスト側のどのポート番号にマッピングされているか確認  
 
 - `docker run --name コンテナ名 -d -p 8080:80 イメージ名`  
  イメージからポート設定して、コンテナを作成  
  `8080:80`は、[外部からアクセスされるポート番号]：[コンテナ側のポート番号]という意味。  
  
  `docker logs -f --tail=100 <container-name>`
  
 - ローカルからコンテナへ CP  
 `docker cp [オプション] ローカル・パス コンテナ:パス`  
 - コンテナからローカルへ CP  
 `docker cp [オプション]  コンテナ:パス ローカル・パス`
 
 ### Windows版Docker 種類
 - DockerDeskTop(WSL2版)  
 仮想化:Hyper-V
 - DockerDeskTop(Hyper-V版)  
 仮想化:Hyper-V(OSエディションが制限される)
 - Docker Toolbox  
 仮想化:VirtualBox
 
 
