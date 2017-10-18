#gitErr

1. [GIT] warning: LF will be replaced by CRLF问题解决方法

   * 原因:windows中广泛使用CRLF来表示一行结束，而在Linux/Unix系统中只有LF。

   * 解决：

     ```shell
     $ rm -rf .git  
     $ git config --global core.autocrlf false  
     ```

     ​

2. git签出远程分支问题解决


   * 问题：当使用如下命令：

     * ```shell
       $ git checkout -b develop origin/develop  
       ```

     * ```shell
       $ git checkout --track origin/develop  
       ```

     签出远程分支，出现一下错误：

     ```shell
     fatal: Cannot update paths and switch to branch 'develop' at the same time.  
     Did you intend to checkout 'origin/develop' which can not be resolved as commit?  
     ```

   * 解决：

     先：

     ```shell
     $ git fetch 
     ```

     再：

     ```shell
     $ git checkout -b develop origin/develop  
     ```