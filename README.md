# 团队web项目开发

## 要点

- 每个开发者有自己的dev分支
- 代码测试无误后，push到各自的分支再合并到主分支
- 前后端分离，迭代式开发

## tips

1. 多个人分别用以下命令克隆项目到本地
> $ git clone [https://github.com/RyanUaa/Web.git](https://github.com/RyanUaa/Web.git) 

2. 创建远程origin的dev分支到本地，于是可以用
> $ git checkout -b **dev origin/**dev

3. 在各自分支上继续修改，然后，把修改的内容push到远程
> git push origin **dev

4. 如果推送失败，因为你试图提交的跟你小伙伴推送的提交有冲突，解决办法很简单。Git提示告诉我们，先用git pull把最新的提交从origin/dev上抓下来，然后在本地合并，解决冲突后，再推送：
> $ git pull

5. 如果 git pull失败了，原因是没有指定本地的dev和远程origin/dev上的链接
>$ git branch --set-upstream **dev origin/**dev 再pull

6. 如果git pull是成功的，但是合并出现冲突，需要手动解决，解决的方法和分支管理中的解决冲突完全一样，解决后，提交，再push.
