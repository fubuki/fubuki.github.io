---
layout: post
title: "git 偏好設定"
date: 2014-04-20 10:22:01 +0800
comments: true
categories: ["git"]
---

記錄從網路上看到關於git有用的設定。
<!-- more -->
#### 1. git 加上顏色
		git config --global color.ui true
#### 2. git 自動補完指令和分支名
下載[git-completion.bash ]，然後在.bashrc 加入下面這段程式碼然後讓新的Bash生效就可以了。  

		if [ -f ~/.git-completion.bash ]; then
  			. ~/.git-completion.bash
		fi

#### 3. 顯示目前在哪個分支

下載[git-prompt.sh]，然後在.bashrc加上下面指令，

		source ~/.git-prompt.sh
		export PS1='$(__git_ps1 "(%s)") \W $'
之後就可以在git專案底下看到Bash顯示在哪個專案和分支。

		(master) Lucene $

#### 4. git alias
		git config --global alias.check checkout
		git config --global alias.cmt commit
#### 5. 設定git使用的編輯器和diff工具
下面的設定可以在~/.gitconfig修改。

		git config --global core.editor
		git config --global diff.tool 
		git config --global merge.tool 


[git-completion.bash ]: https://github.com/git/git/blob/master/contrib/completion/git-completion.bash 
[git-prompt.sh]: https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh