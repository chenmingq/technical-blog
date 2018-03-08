# idea 上传项目到github

## 一、在你的创建github 仓库

---
## 二、创建本地项目

- 在你本地使用idea创建项目
--- 
## 三、提交至github

```
    git init
```
```
   git add .
```
```
   git commit -m "提交信息备注"
```
```
   git remote add origin https://github.com/xxx/xxx.git
   -- https://github.com/xxx/xxx.git 为远程分支地址
```
```
    git push -u origin master

    -- 这一步会要求输入你的github用户名称(不是登陆的邮箱) 和密码
```
