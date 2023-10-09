![[Pasted image 20231001084943.png]]git reset HEAD 檔名
git checkout 檔名
#詢問ChatGDP
如果您想退出 `git log` 并返回到命令行提示符，您可以按下键盘上的 `q` 键。这会关闭 `git log` 视图，然后您将能够继续使用命令行。
先在主資料夾中建立 .gitignore檔(需在git bash執行): touch .gitignore
用文字編輯器鍵入取消追蹤的檔名，包含.gitignore檔
![[Pasted image 20231001185343.png]]
如果停止追蹤的資料夾在某個被追蹤資料夾中的語法: git rm --cached -r parent_folder/nested_folder
![[Pasted image 20231001185642.png]]
# git commit --amend
	`git commit --amend`命令用于修改最新的提交记录。它通常用于以下情况：
	1. 修改提交消息：你可以使用`--amend`来更改最新提交的提交消息。	    
	1. 添加漏掉的文件：如果你在最新的提交中忘记了添加文件，你可以使用`--amend`来将这些文件添加到最新的提交中，而不需要创建一个新的提交。
	下面是`git commit --amend`的基本用法：
	bashCopy code
`git commit --amend`

	这将打开文本编辑器，允许你编辑最新提交的提交消息。你可以修改提交消息，保存并关闭编辑器。

	如果要添加漏掉的文件到最新的提交中，可以执行以下步骤：

	1. 将漏掉的文件添加到暂存区（使用`git add`命令）。
    
	1. 运行`git commit --amend`。
    

	这将会将暂存区中的文件添加到最新的提交中，而不会创建新的提交。请注意，只有最新的提交会被修改。

==请小心使用`git commit --amend`，因为它会改变提交历史。如果你已经将提交推送到远程仓库，那么不要修改已经共享的提交，因为这可能会引发问题。只有在本地工作时才应该使用`--amend`来进行修改。==