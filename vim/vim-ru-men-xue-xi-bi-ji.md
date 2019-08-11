# Vim入门学习笔记

## 参考资料

\[vim-cheat-sheet01\][https://vim.rtorr.com/lang/zh\_cn](https://vim.rtorr.com/lang/zh_cn)

\[vim-cheat-sheet02\][https://vimsheet.com/](https://vimsheet.com/)

图片版：

![&#x56FE;&#x7247;&#x7248;cheet-sheet](../.gitbook/assets/vi-vim-cheat-sheet.gif)

## 常用清单

### 光标

```text
h - 左移光标
j - 下移光标
k - 上移光标
l - 右移光标
Ctrl + b - 向后滚动一屏
Ctrl + f - 向前滚动一屏
Ctrl + d - 向前滚动半屏
Ctrl + u - 向后滚动半屏
0 - 移动到行首
$ - 移动到行尾
gg - 移动到文件第一行
G - 移动到文件最后一行
5G - 移动到第五行
```

### 插入模式 - 插入/追加文本

```text
i - 从光标前开始插入字符
I - 从行首开始插入字符
a - 从光标后开始插入字符
A - 从行尾开始插入字符
Esc - 退出插入模式
```

### 编辑

```text
c$ - 从光标位置开始, 修改当前行
cw - 从光标位置开始, 修改单词
u - 撤销
Ctrl + r - 重复
. - 再次执行上个命令
```

### 可视化模式命令（v进入可视化模式）

```text
> - 向右缩进
< - 向左缩进
y - 复制
d - 剪切
~ - 大小写切换
```

### 退出

```text
:w - 保存
:w !sudo tee % - 使用 sudo 保存当前文件
:wq or :x or ZZ - 保存并退出
:q - 退出(修改未保存时警告)
:q! or ZQ - 不保存强制退出
:wqa - write (save) and quit on all tabs
```

### 查找/替换

```text
/pattern - 查找<kbd>pattern</kbd>
?pattern - 向上查找<kbd>pattern</kbd>
n - 查找下一个
N - 查找上一个
:%s/old/new/g - 替换全部
:%s/old/new/gc - (逐个)替换
:noh - 移除搜索结果的高亮显示
```

