# git 相关参考资料

-廖雪峰 git 教程 https://www.liaoxuefeng.com/wiki/896043488029600

# git 初始配置

- git config --global user.name 用户名
- git config --global user.email 邮箱
- git config --global push.default simple
- git config --global core.quotepath false
- git config --global core.editor "code --wait"
- git config --global core.autocrlf input

# git 基本命令

1. git init 创建 git 文件
2. git add 将文件提交至暂存区
3. git commit -m "内容" 提交至版本库
4. git commit -v
5. git log 查看上传历史 --pretty=oneline 查看缩略提交
6. git reset --hard xxxxxx 提交号前 6 位 回到对应版本
7. git reflog 查看所有历史
8. git branch x 创建分支
9. git checkout x 切换分支
10. git merge xxx 合并 xxx 分支
11. git status -sb 查看冲突
12. git branch -D xx 删除无用分支
13. git status 查看状态
14. git diff xx.xx 查看文件未上传修改内容
15. git diff head --xx.xx 查看工作区和版本库不同
16. git checkout --xx.xx 丢弃工作区修改 回到最近一次 add 或 commit 的状态
17. git remove --xx.xx 从版本库中删除文件
18. ssh-keygen -t rsa -C "xxx@xxx" 创建 ssh key
19. git branch -m xxx aaa 修改分支名称
20. git push 上传
21. git remote rm xxx 解除关系
22. git clone 下载
23. git checkout -b xxx 创建并切换分支
24. git branch 查看分支
25. git switch -c xxx 创建并切换分支
26. git switch xxx 切换分支
27. git log --graph 查看分支合并图
28. git merge --no-ff -m "merge with no-ff" dev 使用 No-FF 模式合并 dev 分支并提交 commit，从分支历史可以看到分支信息
29. https://www.liaoxuefeng.com/wiki/896043488029600/900388704535136 bug 分支等
