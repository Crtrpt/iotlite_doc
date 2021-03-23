# 告警
### 方向
D-C


### 示例
```javascript
    {
      "name": "温度过低",
      "level": "20",
      "interval": 10,
      "condition":"temperature<20",
      "resume": "temperature>20"
    },
```

### 设备端支持的话 
可以直接发送给控制端

设备端可以直接发送 `温度过低` 事件

topic: 
```
/productSn/deviceSn
```
payload:
``` javascript
 {
    "action":"alarm",
    "name":"温度过低"
 }
```
--------------------

### 设备端如果不支持的话
通过监控属性值的变化 控制端自动创建 告警

- condition 为触发条件
- resume 为恢复条件
- interval 为触发间隔
- level 为告警级别
- name 为告警名称

topic: 
```
/productSn/deviceSn
```
payload:
``` javascript
 {
    "action":"property",
    "name":"power",
    "value: 0
 }
```


