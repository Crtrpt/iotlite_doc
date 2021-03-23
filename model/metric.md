# 设备的监控指标 
### 通过监控属性的变化 创建折线图
```javascript
 "metric":[
    {
      "name":"温度",
      "source": {
        "type": "property",
        "name": "temperature"
      }
    }
  ],
```
 
###  TODO 虚拟属性  通过属性计算出来的值 创建折线图
```javascript
  {
      "name":"面积",
      "source": {
        "type": "compute",
        "name": "width*height"
      }
    }
```