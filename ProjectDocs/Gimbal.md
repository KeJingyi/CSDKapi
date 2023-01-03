## 云台状态

主题：CSDK/Gimbal/state/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| payload_index | int | 负载索引 |
| pitch | float | 俯仰角 |
| roll | float | 横滚角 |
| yaw | float | 偏航角 |

描述：云台姿态数据


## 旋转云台

主题：CSDK/Gimbal/rotate

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| payload_index | int | 负载索引 |
| mode | RotationMode | 控制模式 |
| pitch | float | 俯仰角度/速度 |
| roll | float | 横滚角度/速度 |
| yaw | float | 偏航角度/速度 |
| time | float | 动作执行时间 |

描述：控制云台旋转角度

响应主题：CSDK/Gimbal/rotate/callback

响应参数：无

响应描述：执行控制云台角度命令的结果


## 云台复位

主题：CSDK/Gimbal/reset

参数：无

描述：控制云台复位（回中）

响应主题：CSDK/Gimbal/reset/callback

响应参数：无

响应描述：执行云台复位命令的结果
