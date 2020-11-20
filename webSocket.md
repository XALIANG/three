## == 常量

WebSocket.CONNECTING  连接

WebSocket.OPEN  打开

WebSocket.CLOSING  交割

WebSocket.CLOSED 关闭


## 属性

WebSocket.extensions 只读
服务器选择的扩展

WebSocket.onclose
用于指定连接关闭后的回调函数

WebSocket.onerror
用于指定连接失败后的回调函数。

WebSocket.onmessage
用于指定当从服务器接受到信息时的回调函数。

WebSocket.onopen
用于指定连接成功后的回调函数。

WebSocket.protocol 只读
服务器选择的下属协议。

WebSocket.readyState 只读
当前的链接状态。

WebSocket.url 只读
WebSocket 的绝对路径。

## 方法

WebSocket.close([code[, reason]])
关闭当前链接。

WebSocket.send(data)
对要传输的数据进行排队。


## 事件

**使用 addEventListener() 或将一个事件监听器赋值给本接口的 oneventname 属性，来监听下面的事件。**

`close`
当一个 WebSocket 连接被关闭时触发。
也可以通过 onclose 属性来设置。


`error`
当一个 WebSocket 连接因错误而关闭时触发，例如无法发送数据时。
也可以通过 onerror 属性来设置.

`message`
当通过 WebSocket 收到数据时触发。
也可以通过 onmessage 属性来设置。

`open`
当一个 WebSocket 连接成功时触发。
也可以通过 onopen 属性来设置。

*创建一个连接*

`const socket = new WebSocket('ws://localhost:8080');`

*连接已打开*

```
socket.addEventListener('open', function (event) {
    socket.send('Hello Server!');
});

```
*监听消息*

```socket.addEventListener('message', function (event) {
    console.log('Message from server ', event.data);
});

```
