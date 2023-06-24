# github練習

## 参考資料
[サル先生のGit入門](https://backlog.com/ja/git-tutorial/)  
[ドットインストール git入門](https://dotinstall.com/lessons/basic_git)  
[LearnGitBranching](http://k.swd.cc/learnGitBranching-ja/)  
[誰かのGitHub練習](https://github.com/mollifier/github-practice)

## 秘密鍵の生成
ssh-keygen -t rsa -b 2048 -f ~/.ssh/directory_a/id_rsa  
cat ~/.ssh/directory_a/id_rsa.pub | pbcopy # 公開鍵をクリップボードにコピー(mac)  
vim ~/.ssh/config
```
Host directory_a
  HostName github.com
  User git
  IdentityFile ~/.ssh/directory_a/id_rsa
```
ssh -T git@directory_a # 接続確認 通常は「ssh -T git@github.com」 である。鍵を使い分けている為、こちらの方法 
git clone git@direcotry_a:user/repository.git # git clone 
