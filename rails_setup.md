## windowsPC準備手順

※前提条件  
windows10 Pro

1. 仮想環境の設定を有効にする(以下 ThinkPadの手順, Macの場合は必要なし)
 - shiftを押しながら再起動をかける
 - トラブルシューティングをクリック
 - 詳細オプションをクリック
 - UEFI フォームウェアの設定をクリック
 - 再起動をクリック
 - SecurityタブのVirtualizationを選択
 - Intel (R) Virtualization TechnologyをEnableにする
 - F10で設定を保存して再起動  

2. chromeをインストール

3. docker for windows をインストール

4. docker を起動する

5. docker のファイル共有を許可する
 - タスクトレイ(メニューバー)に表示されているdockerアイコンを右クリック
 - Settingを開く
 - Shared Drivesにチェックを入れてApplyする

6. railsのイメージを落としてくる
 - docker pull rails

7. イメージを起動する
 - docker run --privileged -it -p 3000:3000 -v C:\Users\ユーザー名\Documents\1day_intern:/1day_intern --name rails rails:latest

8. コンテナにアクセスする
 - docker exec -it rails /bin/bash
