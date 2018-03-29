# 分支操作

- 查看分支

- git branch 查看当前分支情况
```
$ git branch 
```

```
* master
```

- 新建分支
```
$ git branch branch-name
```
```
$ git branch 
```
```
* master
branch-name
```
- 切换分支
```
$ git checkout branch-name
```
```
切换到分支 'branch-name'
```
- 提交
```
$ git commit -m "test01"
```
- 推送到新分支
```
$ git push -u origin branch-name
```

- 删除分支
```
$ git branch -r -d origin/branch-name  
```
```
$ git push origin :branch-name
```
# Merge Requests操作
```
进入项目
左侧导航找到 Merge Requests 菜单点击
找到 New merge request(不是中间就是右上角) 点击 
Source branch 选择要合并的分支 （Select source branch）
选择好后 点击 Compare branches and continue
```