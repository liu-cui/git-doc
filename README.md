## 关于关联远端仓库

如果关联远端仓库失败，则1；否则跳转至3。	

1、查看远端关联仓库
`$ git remote -v`

2、删除远端关联仓库
`$ git remote remove main(master)`

3、重新关联远端仓库
`$ git remote add origin git@github.com:liu-cui/git-command.git`

4、将当前分支设置为主分支（由于github主分支为main故需要将本地的master分支更换为main分支）
`$ git branch -M main`

5、推送到远端分支
`$ git push -u origin main`
- 推送失败，出现`fatal: refusing to merge unrelated histories`
`$ git pull origin main --allow-unrelated-histories`
并重新推送

## 操作分支
1、建立分支
`$ git branch <branch1>`

2、查看所有分支
`$ git branch -a` 带*为当前分支

3、切换分支到branch1
`$ git checkout <branch1>`
- 也可以-b，直接建立分支并进行切换操作
`$ git checkout -b <branch2>`

4、删除分支
`$ git branch -d <branch1>`

5、分支合并
`$ git reset --hard HEAD~`

6、冲突合并,rebase的使用
rebase的时候，解决冲突后的提交不是使用commit。
- 提交
`$ git rebase --continue`
- 取消rebase
`$ git rebase --abort`




