# Socketio_Client
使用socketIO_client构建的python客户端示例

# 说明  

使用之前安装socketIO-client  

```git
$ pip install socketIO-client
```
与服务端的连接在 client.py 中完成  

更改与服务器连接的有关配置,请在client.py中完成

# 使用 client.py 进行开发  

首先将 client.py 文件放在项目目录下  

执行 import client  

发送数据只需调用 client.send() 即可  

接收数据需要调用 client.recv(channl,callback)  

callback 为收到消息时调用的方法，以下做了示例  

```python
def doSomeThing(*args):
    print('recv:', args)


# recv调用示例
client.recv('view_channl', doSomeThing)

# 若想收到消息 务必调用此方法
client.wait()
```