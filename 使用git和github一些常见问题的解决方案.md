### 内容来源：

csdn博客：

[git忽略了SSL认证](https://blog.csdn.net/qq_32907195/article/details/112292369?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165354896316782388066153%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165354896316782388066153&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-3-112292369-null-null.142%5Ev10%5Epc_search_result_control_group,157%5Ev12%5Econtrol&utm_term=git%E4%B8%ADSSL&spm=1018.2226.3001.4187)

简书博客：

[github无法连接-解决](https://www.jianshu.com/p/8bec38c94fe6)

### 内容：

### 一.连接不上github或者请求超时

1. 可以在控制台输入下面命令检查连接是否通畅

   ```javascript
   ping github.com
   ```

   如果没有连通的话ping结果就是四个数据包全部没有传输成功

2. 如果连接不通畅试着修改一下host文件

   修改默认win10下默认路径如下的host文件

   ```javascript
   C:\Windows\System32\drivers\etc\host
   ```

   到解析ip查询网站搜索github.com当前的解析ip，在host文件最下方增加一块内容

   ```javascript
   #github
   解析ip名    github.com
   ```

   如果一个ip没有效就换一个试一试

   推荐ip查询网站：<https://tools.ipip.net/dns.php>

   注意！一般电脑默认不提供用户修改host权限的，需要用户右键文件属性去修改访问权限

   [点此到原文链接](https://www.jianshu.com/p/8bec38c94fe6)

### 二.使用了SSL认证没有通过

1. 使用下面命令忽略认证

   ```javascript
   git config http.sslVerify "false"
   ```

### 三.拉取远程失败

1. 查看当前是否有未提交的更新，防止更新顺时

2. git remote -vv查看远程仓库是否配置正确

3. 查看与github的连接是否通畅.见一

4. 判断拉取的远程分支是否和本地分支同名，或者说两个分支是否匹配

### 3.分支合并失败