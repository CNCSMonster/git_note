### 使用github提供的远程存储仓库。配合git可以实现在远程存储本地代码，以及从远程拉取远程最新的代码

### 前置问题，解决这些问题才能正式开始这10min.

```javascript
如何创建一个github账号？
如何创建github中的远程仓库（repository)？
如何在github中创建具有指定权限的令牌（token）？
```

#### 配置本地git的全局账号

获取全局账号邮箱和密码

```javascript
git config --global user.name
git config --global user.email
git config --global user.password
```

设置全局账号邮箱和密码

```c
git config --global user.name "用户账号名"
git config --global user.email "用户邮箱"
git config --global user.password "xxxx"
```

em.

```javascript
git config --global user.name "cncsmonster"
设置全局账号为cncsmonster.这是笔者的github账号名
git config --global user.email "xxx@xxx.com"
设置账号邮箱为xxx@xxx.com,注:该邮箱应该是你用来注册github账号的邮箱
git config --global user.password "yyy-xxx"
设置账号密码为yyy-xxx。密码应该为你在github上面申请的令牌
```

#### 为该项目添加远程仓库

查看远程仓库

```javascript
git remote -v
查看当前远程仓库。
返回结果左侧为远程仓库的简称（自定义的），右侧为远程仓库实际路径名称
```

删除远程仓库

```javascript
git remote rm 远程仓库简称
```

添加远程仓库

```javascript
git remote add 自定义的远程仓库简称 远程仓库网络路径（全名）
```

em.

```javascript
git remote add git_study https://github.com/cncsmonster/git_note
该行命令就添加了一个地址为https://github.com/cncsmonster/git_note的远程仓库，并命名为git_study
在之后的使用中就可以使用简称git_study代指这个远程仓库
git remote rm git_study
之后使用该行命令会把该仓库删去
```

#### 从远程拉取最新的更新

(如果没有创建分支(branch)的话，可以直接使用下面命令，创建分支的情况另外讲)

```javascript
git pull 仓库简称 master
该行命令会把对应远程仓库的内容拉取到本地
```

#### 把本地代码推送到远程

```javascript
git push 仓库简称 master
```