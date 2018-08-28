# 短小精悍的命令行合集

## 命令行相关

#### 以管理员身份执行上一个由于权限被拒的命令
```bash
sudo !!
```
示例：

![sudo !!](./images/sudo_!!.gif)

#### 切换工作目录
```bash
# 切换回上一个工作目录
cd -

# 把上个命令的参数作为 cd 参数使用
cd !$
```
#### 执行多个命令
```bash
# 顺序执行多个命令
command_1; command_2

# 如果 command_1 执行成功，则执行 command_2
command_1 && command_2

# 如果 command_1 执行失败，则执行 command_2
command_1 || command_2
```
#### 查找并终止进程
```bash
kill $(ps aux | grep 'process_name' | awk '{print $2}')
```

#### 统计并显示历史记录中最常用的命令
```bash
history | awk 'BEGIN {FS="[ \t]+|\\|"} {print $3}' | sort | uniq -c | sort -nr | head
```

## 快捷键相关

> 默认以 Mac 键盘示例，Windows 用户请将 `control` 键改为 `Ctrl` 键。

#### 搜索并执行过去使用过的命令
control + R 进入`反向搜索`模式。
```bash
(reverse-i-search)`':
```

#### 移动光标

control + A 将光标移动至命令行开头位置；
control + E 将光标移动只命令行结尾位置；

## TODO
- [ ] 为每一个技巧配上 gif 图




