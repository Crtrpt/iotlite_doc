# 事件# property 
### 方向
D-C

### 示例
```javascript
    {
      "name": "turn off",
      "desc": "关电",
      "condition":"power==0"
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
```javascript
 {
    "action":"event",
    "name":"turn off"
 }
```

--------------------

### 设备端如果不支持的话
可以通过控制端对属性的监控产生事件

设备端修改power 到 0 控制端自动触发 `turn off` 事件


topic: 
```
/productSn/deviceSn
```
payload:
``` javascript
 {
    "action":"property",
    "name":"power",
    "value:0
 }
```


