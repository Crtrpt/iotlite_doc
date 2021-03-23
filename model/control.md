# 控制
### 方向
C-D


### 示例
```javascript
    {
      "name": "turn off",
      "desc": "关电",
      "condition":"power=0"
    },
```

### 设备端支持的话 
可以直接发送给控制端

设备端可以直接发送 `turn off` 事件

topic: 
```
/productSn/deviceSn
```
payload:
``` javascript
 {
    "action":"contrl",
    "name":"turn off"
 }
```

--------------------

### 设备端如果不支持的话
通过执行 action 指定的 脚本 修改property 属性

转换为属性的变化发送给设备端

topic: 
```
/productSn/deviceSn
```
payload:
``` javascript
 {
    "action":"property",
    "name":"power",
    "value": 0
 }
```


