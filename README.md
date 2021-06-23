### 简单的测试一下github的ci/cd功能###

``` 
将本地项目或者远程项目进行操作并更新
git add *
git commit -m "init..."
git remote add origin git@github.com:z1421012325/ci_cd_demo.git
git push origin master

在github上进行下列按钮操作 
actions > set up this workflow > start commit > commit new file .

git项目中会多出一个 .githuv/workflows/build语言.yml 文件,该文件作用为在分支合时进行检测冲突

将远程项目pull到本地
git pull origin master

~
假设:
    git checkout -b ci           # 本地创建ci分支
    # 任意添加文件
    git add * 
    ...
    git push origin ci
    # master分支将对提交分支进行合并请求,项目管理人员将对该分支检查,自动进行文件检测,无问题管理人员允许合并

    注意其中,每次push成功之后必须切换本地master并分支pull拉取最新远程master分支,如果需要显眼推送请求请在创建一个新的分支修改并push,push之后会github界面上高亮显示
        ```
            如果操作的是共享仓库型号，建议对拉取请求使用主题分支。 从任何分支或提交都可发送拉取请求，但如果需要更新提议的更改，则可使用主题分支推送跟进提交。
        ```



```

### 来源
    github:https://github.com/bydmm/golang-github-action-demo 
    bilibili:https://www.bilibili.com/video/BV1244y1r7Yg
    https://docs.github.com/cn/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
###