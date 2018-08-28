#### 以管理员（超级用户）身份执行上一个由于权限问题而被拒绝的命令
```bash
sudo !!
```

#### 查找并终止进程
```bash
kill $(ps aux | grep 'process_name' | awk '{print $2}')
```
