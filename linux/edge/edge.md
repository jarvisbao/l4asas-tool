# Edge简介
Edge是L4A SAS的客户端，用于跟L4A SAS保持通信，以及跟企业/组织里各数据中心的网关建立安全隧道，并通过安全隧道访问数据中心内的IT服务。
目前支持Windows、Linux。

# Linux
## Edge安装
Linux的Edge是绿色版本，免安装，只需要将压缩包解压到任意目录即可。压缩包中包含一个文件：

- edge 这是edge的服务程序

## Edge设置
用管理员权限打开命令行窗口，转到Edge所在目录，先输入以下命令设置Edge的参数：

```
edge setup -H 47.110.41.171 -p 7500 -t *******
```

其中，参数-t后面跟的是管理员提供的当前用户的令牌。

然后输入以下命令，将Edge安装成系统服务：

```
sudo edge install
```
上述命令执行完后，会在系统里生成一个名为sasedge的服务。

## Edge服务的启停
有以下几种方式可以启动或者停止Edge服务

- 通过命令行

#### 启动Edge服务
打开Terminal，转到edge所在目录，通过以下命令可以启动Edge 服务：

```
sudo ./edge start
```

#### 停止Edge服务
通过以下命令可以启动Edge 服务：

```
sudo ./edge stop
```
