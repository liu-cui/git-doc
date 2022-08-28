## 关于关联远端仓库
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


