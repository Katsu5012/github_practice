//新規ファイル作成
mkdir new_file

//作成したファイルに移動
cd new_file

//ローカルリポジトリの作成
git init

//ローカルリポジトリをファイルを指定して作成
git init new_file

//ステージングエリアに追加(git add)
//全てのファイルを追加（カレントディレクトリ以下を実行）
git add .

//全てのファイルを追加(どこにいても実行)

git add -A

//前回から変更があったファイルを追加（どこにいても実行、新しいファイルは実行されない）
git add -u

//ステージングエリアからローカルリポジトリに反映
git commit -m 'message'

//add と commit を同時にする
git commit -a -m 'message what i do'
git commit -am 'message what i do'

//変更した差分をみる（詳細に出る）
//ワーキングディレクトリとステージングエリアの差分
git diff

//ステージングエリアとローカルリポジトリの差分
git diff --staged

//ワーキングディレクトリの変更をステージングエリアのものに戻す(ファイル名でも可能、コード色々書いたけど前回のに戻したい)
git restore .

//ステージングエリアの変更をローカルリポジトリのものに戻す(git add 間違ってした時)
git restore --staged .

//ワーキングディレクトリ、ステージングエリアからファイルの削除
git rm file_name

//ステージングエリアのみからファイルの削除
git rm --cached file_name

//ファイル名の変更
git mv pre_file_name new_file_name

//commit の確認(日時、コミットした人)
git log
https://atmarkit.itmedia.co.jp/ait/articles/2004/09/news018.html

//commit 単位でログや差分,ファイルを表示
git show
https://atmarkit.itmedia.co.jp/ait/articles/2004/17/news021.html

//ファイル内の行を誰が変更したか
git blame

//tag を追加(version、commit_id を省略すると最新の参照)
git tag tag_name commit_id
git tag tag_name commit_id -m 'message'

//tag の一覧
git tag

//branch の作成
git branch branch_name

//branch の切り替え
git switch branch_name

//branch の作成と切り替えを同時にする
git switch -C branch_name

//branch の削除
git branch -d branch_name

//branch の確認
git branch

//master と branch の差分をみる
git diff master..branch_name

//merge する
git merge branch_name

//ファストフォワードマージについて
https://yu8mada.com/2018/08/15/what-is-a-fast-forward-merge-in-git/

//3 ウェイマージについて
//どっちを merge するか決めて,add,commit で終わり
https://kz-ike.hatenablog.com/entry/2021/01/04/175259

//スカッシュマージについて
https://backlog.com/ja/git-tutorial/stepup/34/
