[toc]

# svn FAQ

## 更新时发生错误，提示"xxx locked"
clean up即可解决

# svn 命令技巧

非递归更新当前目录下的所有文件和目录
```
svn update --set-depth immediates
```

因为--set-depth对所有子目录生效，因此在当前目录或者进入子目录再更新，无法更新出新的文件或目录。
进入子目录重新设置depth为无限即可，从而达到只更新某个子目录的效果。
```
cd subdir
svn update --set-depth infinity
```
