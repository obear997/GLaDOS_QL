> 什么是青龙面板 青龙面板支持python3、javaScript、shell、typescript 的定时任务管理面板（A timed task management panel that supports typescript, javaScript, python3, and shell.）

### 修改脚本

> 什么是serve酱？ 「Server酱」，英文名「ServerChan」，是一款「手机」和「服务器」、「智能设备」之间的通信软件。 说人话？就是从服务器、路由器等设备上推消息到手机的工具。

在 `sckey` 和 `cookie` 后面填写 serve酱的 `sckey`（不需要可以跳过）和 账号 `cookie`

![在这里插入图片描述](./_resources/4b6651c89c074fa89f59fa030d876944_3ad06e5fd4fb44f4b.png)

#### 获取serve酱的 `sckey`

serve酱官网：https://sct.ftqq.com/

<img width="962" height="541" src="./_resources/watermark_type_d3F5LXplbmhlaQ_sh_09e605635241469da.png" class="jop-noMdConv">

#### 获取账号 `cookie`

打开“开发者工具”，通常快捷键为F12，或是点击浏览器选项-更多工具-开发者工具，打开后如图所示点击 “网络” （未进行汉化的话是：network）标签

<img width="962" height="533" src="./_resources/watermark_type_d3F5LXplbmhlaQ_sh_a3fb233e149241a8a.png" class="jop-noMdConv">

### 上传脚本

#### 方法1：直接上传脚本

![在这里插入图片描述](./_resources/watermark_type_d3F5LXplbmhlaQ_sh_85f23192896a4bc9b.png)

可通过 `ftp` 工具直接找到青龙面板安装位置，在 `scripts` 目录中新增自己的目录，所以直接把签到脚本文件放根目录也可以。

青龙面板可能会根据你所使用的命令存放目录，所以每个人都不一样，我的 `docker` 安装目录为：`/etc/systemd/docker/` ，而青龙面板则存放在 `docker` 的子目录中。

#### 方法2：新建脚本

在青龙面板中找到 “脚本管理”

![在这里插入图片描述](./_resources/watermark_type_d3F5LXplbmhlaQ_sh_2710d78fde4640609.png)

从面板右侧点击 ”+“ 按钮

![在这里插入图片描述](./_resources/766a869e0fdd4576b4d695d8801cade2_872374f62c1d4ada9.png)

根据自己的实际情况填写脚本信息，用到的是 `Python` 所以，文件最后是 `.py`

![在这里插入图片描述](./_resources/watermark_type_d3F5LXplbmhlaQ_sh_b910dc692cdd4cd78.png)

### 添加签到任务

在青龙面板中找到定时任务

![在这里插入图片描述](./_resources/watermark_type_d3F5LXplbmhlaQ_sh_a6340a57362946d99.png)

从面板右侧点击 ”新建任务“

![在这里插入图片描述](./_resources/8136b97659214f8491816f588328c2fc_3600cf0bdc1241eea.png)

按照上面创建的文件的名称和路径设置任务命令

![在这里插入图片描述](./_resources/watermark_type_d3F5LXplbmhlaQ_sh_97ff97fb3b67403d9.png)

时间规则为：`秒 分 时 天 月 周`，如：`0 9 * * *` ，意思是`每天09:00`执行该脚本。

### 测试效果

点击任务后面的 ”运行“ 按钮进行手动执行一次

![在这里插入图片描述](./_resources/ffde4bed28a34af1a6cf6a48457282fa_53e8d504d4df4a4d9.png)

点击任务后面的 ”日志“ 按钮查看运行日志

![在这里插入图片描述](./_resources/10a731652af542bfb8edf19cb755bffc_146e566df53e43338.png)

见到下面日志，说明成功签到，并且获得了1天奖励时间。

![在这里插入图片描述](./_resources/watermark_type_d3F5LXplbmhlaQ_sh_719c7ee35308481cb.png)

到此，GLaDOS自动签到就部署成功了。