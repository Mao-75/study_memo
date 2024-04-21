### git log --stat
→各コミットによって変更された各ファイルの挿入,削除の数を表示。

行の修正は、1 insertion (挿入) ,1 deletion (削除) のように表現。

### git log --oneline
→コミットメッセージの最初の１行だけ表示。

コミット名は省略形。

要点だけ表示したいときに使用する。

### git log -p
### git log -p ファイル名
→ファイルの変更差分または、指定したファイルの変更差分を表示する。

### git log -n コミット数
→表示するコミット数を制限する。

最近の変更履歴だけ見たい時に使う。
```
[例] git log -n 3 もしくは git log -3 でも同じ挙動。
```

### git log --reverse
→コミットを古い順から表示する。

### git log --graph
→コミット履歴をグラフで表示する。

コミットの流れを把握できる。

### git log --name-status
→変更・追加したファイル名を表示。

　A : addのこと、ファイルが追加された場合に表示される。
 
　M : modifyのこと、ファイルに変更があった場合に表示される。
 
　D : deleteのこと、ファイルが削除された場合に表示される。

### git log --author=ユーザー名
→コミットしたユーザーを絞って検索。

### git shortlog
→作成者別に各コミットを分類し、各コミットメッセージの最初の行を表示。

誰がどんな作業をしているかについて確認する簡単な方法。

### git log --pretty=short
→コミット、著者、タイトルを表示。

日付は表示されない。

### git log --pretty=full
→コミット、著者、タイトル、コミッタを表示。

日付は表示されない。

### git log --pretty=format:
→独自フォーマットを設定する。


### formatで使用できるプレスフォルダー
```
%H	      コミットのハッシュ
%h	      コミットのハッシュ(短縮系)
%an	      authorの名前
%ae	      authorのメールアドレス
%ad	      authorの日付(--date= オプションに従った形式)
%ar	      authorの相対日付
%cn	      committerの名前
%ce	      committerのメールアドレス
%cd	      committerの日付(--date= オプションに従った形式)
%cr	      committerの相対日付
%s	      コミットメッセージ
%d	      ブランチやタグの名前
%Cred	    文字を赤くする
%Cgreen	  文字を緑色にする
%Cblue	  文字を青くする
%Creset	  文字の色を戻す
%C(auto)	文字の色をgitが用意している色にする
%C( )	    色、属性の指定
```

**色**
```
normal
black
red
green
yellow
blue
magent
cyan
white
#ff0ab3のような8bitカラー
```

**属性**
```
bold:太字
dim:減光
ul:アンダーライン
blink:点滅
```


### 個人的に見やすいgit logカスタマイズ
```
git log --pretty=format:'[%ad %Cgreen%ar%Creset] %C(yellow)%h %C(auto)%d  %s %C(bold cyan)<%an>' --date=format:'%Y-%m-%d %H:%M' --graph
```

### エイリアス編集
```
vim ~/.gitconfig
```
