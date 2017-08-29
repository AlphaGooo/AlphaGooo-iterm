# alphagooo-iterm
记录iterm的一些使用技巧。

## 怎么连接远程服务器？
1. 首先写一个sh脚本，比如命名为 item.sh

```
#!/usr/bin/expect -f
set user alphagooo
set host 10.2.0.3
set password 123456
set timeout -1
spawn ssh $user@$host
expect "*assword:*"
send "$password:\r"
interact
expect eof
```

2. 然后保存脚本，比如保存在 ~/.ssh 目录下，打开iTerm，ctrl + o 打开配置，添加profile，选择 Command - Command，写入

```
expect ~/.ssh/item.sh
```

3. 保存后执行就可以了。

## 怎么玩转iterm？

1. 垂直分屏：command + d
2. 水平分屏：command + shift + d
3. 切换屏幕：command + option + 方向键 command + [ 或 command + ]
4. 查看历史命令：command + ;
5. 查看剪贴板历史：command + shift + h
7. 新建标签：command + t
8. 关闭标签：command + w
9. 切换标签：command + 数字 command + 左右方向键
10. 切换全屏：command + enter
11. 查找：command + f
13. 清除当前行：ctrl + u
14. 到行首：ctrl + a
15. 到行尾：ctrl + e
16. 前进后退：ctrl + f/b (相当于左右方向键)
17. 上一条命令：ctrl + p
18. 搜索命令历史：ctrl + r
19. 删除当前光标的字符：ctrl + d
20. 删除光标之前的字符：ctrl + h
21. 删除光标之前的单词：ctrl + w
22. 删除到文本末尾：ctrl + k
23. 交换光标处文本：ctrl + t
24. 清屏1：command + r
25. 清屏2：ctrl + l
26. ⌘ + f 所查找的内容会被自动复制
27. ⌘ + r = clear，而且只是换到新一屏，不会想 clear 一样创建一个空屏
28. ctrl + u 清空当前行，无论光标在什么位置
29. 输入开头命令后 按 ⌘ + ; 会自动列出输入过的命令
30. ⌘ + shift + h 会列出剪切板历史


