## 安装
- 在`Big Sur`这个系统里面，每次重启都需要自行的在终端输入`sudo yabai --load-sa`这行命令`yabai`才能正常启动,为了解决这种情况，作者给出了解决方案：
```shell
sudo visudo -f /private/etc/sudoers.d/yabai
```
- 然后编辑；
`<user> ALL = (root) NOPASSWD: /usr/local/bin/yabai --load-sa`
- 里面的`<user>`就是你的用户名，如果不知道是什么你可以在终端输入`whoami`  
- 我的内容如下：
``` shell
itgoyo ALL = (root) NOPASSWD: /usr/local/bin/yabai --load-sa
```
- 然后在`yabairc`配置文件里面的首行复制一下命令:
```shell
sudo yabai --load-sa
yabai -m signal --add event=dock_did_restart action="sudo yabai --load-sa"
```
## 问题
- 如何更新文件
## todo
manage window set which app run on that window

