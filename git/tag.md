# Tag

1. 查看tag

    列出所有tag:

    > git tag
  
    这样列出的tag是按字母排序的，和创建时间没关系。如果只是想查看某些tag的话，可以加限定：

    > git tag -l v1.*

    这样就只会列出1.几的版本。
  
2. 创建tag

    创建轻量级tag：

    > git tag v1.0

    这样创建的tag没有附带其他信息，与之相应的是带信息的tag：

    > git tag -a v1.0 -m "first version"

    -m后面带的就是注释信息，这样在日后查看的时候会很有用，这种是普通tag，还有一种有签名的tag：

    > git tag -s v1.0 -m "first version"

    前提是你有GPG私钥，把上面的a换成s就行了。除了可以为当前的进度添加tag，我们还可以为以前的commit添加tag：

  - 首先查看以前的commit

    > git log --oneline

  - 假如有这样一个commit：8a5cbc2 updated readme, 这样为他添加tag
  
    > git tag -a v1.18a5cbc2


