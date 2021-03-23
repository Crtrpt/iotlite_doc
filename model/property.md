# property 
### 方向
D<->C 
设备的当前属性 可以设备端发给控制端 也可以控制端发给设备端

### 描述
##### dsl property 键描述
- name:
  属性的名称
- desc:
  属性的描述信息
- value:
  设备当前的值
- threshold:
  设备变动的阈值
- defaultValue:
  设备的默认值
- expect :
  设备的期望值


### 示例
```javascript
  {
      "name": "temperature",
      "desc": "温度",
      "value": 0,
      "defaultValue": 0,
      "expect": 0
  },
```