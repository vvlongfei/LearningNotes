#gitErr

1. [GIT] warning: LF will be replaced by CRLF问题解决方法

   * 原因:windows中广泛使用CRLF来表示一行结束，而在Linux/Unix系统中只有LF。

   * 解决：

     ```shell
     $ rm -rf .git  
     $ git config --global core.autocrlf false  
     ```

     ​

