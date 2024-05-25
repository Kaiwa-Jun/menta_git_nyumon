# menta_git_nyumon

事前準備
SSH の設定
以下、SSH・GitHub の接続設定の資料になります。 接続設定ができ次第、SSH でクローンしてください。

ローカルと GitHub の接続設定
自分のローカル PC と GitHub を SSH で接続できるように設定を行います。 ローカル PC で SSH で利用する鍵を作成し、作成した鍵を GitHub に登録してください。

ssh 鍵作成
ssh ディレクトリに移動します(※ない場合は$ mkdir ~/.ssh で作成ししてください)。

※Windows を使っている人で Desktop に.ssh を作ってしまう人をちらほら見かけます。必ず WSL のルートディレクトリ(cd で移動できる箇所)に作るように注意してください。

$ cd ~/.ssh

鍵作成のコマンドを打ちます。 $ ssh-keygen -t rsa

下記内容を聞かれるので、全て enter を打ってください。

Enter file in which to save the key (/Users/(username)/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
下記コマンドで作成した鍵を確認しましょう。（id_rsa と id_rsa.pub があれば ok です） $ ls

GitHub に登録
先ほど作成した鍵を GitHub に登録してください。

$ cat id_rsa.pub で内容を表示してコピーします。

ssh-rsa abcxyz....
GitHub の右上のアイコンから「Settings」を開き、左メニューの「SSH and GPG keys」をクリックしてください。

Image from Gyazo

Image from Gyazo

「New SSH key」をクリックし、コピーした内容を「key」のところにペーストして登録してください。（「title」は任意のもので大丈夫です） Image from Gyazo

接続確認
ローカル PC から GitHub に接続できるかこちらのコマンドで確認してください。 $ ssh -T git@github.com

下記が返ってくれば ok です。

Hi アカウント名! You've successfully authenticated, but GitHub does not provide shell access.

脱出ゲームの説明
事前準備が終わりましたら、好きなディレクトリに移動して、ターミナルで 
git clone https://github.com/Kaiwa-Jun/menta_git_nyumon.git
を実行してリポジトリをcloneしてください。

以下は menta_git_nyumon ディレクトリ内に移動して行ってください。
全て読んで実行してください！

git fetch を打ってください。

git checkout -b search_for_keyword origin/search_for_keyword を打ってください。

次に、cat README.md を打ち込み README を表示させて、指示に従ってください！
