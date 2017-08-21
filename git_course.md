# 本講義の目的
 - gitの概念の理解
 - gitハンズオン
 - gitを使ったチーム開発をするために... 


## gitとは
 - 配布資料をつかって説明(内容下記)
	- 随時質問受付ます
 1. git(使用時の注意)
 2. branch
 3. team開発
 4. どうしたら慣れて行くのか？

## git HandsOn

git clone http://github.com/fumihumi/git_course_repo.git
	//githubにsshkeyを登録している場合はっsshを使ってください
browserにてリポジトリの作成

git remote add  "alias" URL
~git remote add origin git@github.com:fumihumi/"repo_name"~

git remote -v

git init #ローカルのgitリポジトリ作成
	vim git_course_test.txt #管理下にfile作成
	"edit"

	vim readme.md "what"s this repo? why make this?"
	vim .gitignore (oinfig git setting)
	vim ignored_file.txt (ignored file setting)
git status (states of this directory-tree )
	vim ignoredfile (change this file)

git add  git_course_test.txt (adding staging area)
git commit -m'test message' (commiting file && message)

git push (to pushiing remote repos)

1. gitのlocalrepo && remoterepo 
2. workingTree , stagingArea(index),gitDirectory ,Stash,Local&Remote Repository 


vim git_course_test.txt (cahges file)
```
git status 
	#ここでの結果は編集したファイル
git diff (file_name)
	# git diff git_course_test.txt
	#ファイル内の編集内容を表示

git add ~~
git commit -m "commit message"
git push
```


基本的には上記のような
add -> commit -> push 
が基本原則。


git branch make_indexPage (create new branch "make_indexPage")
git checkout make_indexPage(chenge local branch "master TO make_indexPage")

3. branchの考え方

4. conflict 
git checkout -b test_conflict(create && checkout branch)
echo hey > hello.txt (edit this file)
git add hello.txt (staging )
git commit -m "commit on test_conflict branch" (commit ) 
git checkout master(checkout master)
echo hi!!!!!!!! > hello.txt (edit file)
git commit -am"commit on master branch"
git marge test_conflict
vim hello.txt
git commit -am "fix conflict"





その時他のコマンドを知っているともっとgitが便利に使えます。
git log
git status
git stash 
git reset
git rm 
git revert
git rebase
git show
git branch
git checkout
ここら辺はよく使いますね
必要なものは随時紹介します。

