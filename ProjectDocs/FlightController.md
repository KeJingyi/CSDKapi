## GPS 状态

主题：CSDK/FlightController/gpsState/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| altitude | float | 无人机相对高度 |
| latitude | double | 无人机纬度 |
| longitude | double | 无人机经度 |
| satellite_count | int | GPS 卫星数 |

描述：无人机 GPS 状态数据


## IMU 状态

主题：CSDK/FlightController/imuState/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| pitch | float | 俯仰角 |
| roll | float | 横滚角 |
| yaw | float | 偏航角 |
| angular_velocity_pitch | float | 俯仰角速度 |
| angular_velocity_roll | float | 横滚角速度 |
| angular_velocity_yaw | float | 偏航角速度 |

描述：无人机姿态数据


## 飞行速度

主题：CSDK/FlightController/velocityState/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| x | float | 水平 x 轴速度 |
| y | float | 水平 y 轴速度 |
| z | float | 垂直 z 轴速度 |

描述：相对大地坐标的机身速度


## 飞行模式

主题：CSDK/FlightController/FlightMode/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| mode | FlightMode | 无人机飞行模式 |

描述：当前无人机所处于的飞行控制模式


## 降落

主题：CSDK/FlightController/startLanding

参数：无

描述：控制无人机降落

响应主题：CSDK/FlightController/startLanding/callback

响应参数：无

响应描述：执行降落命令的结果


## 停止当前动作

主题：CSDK/FlightController/cancelCurrentAction

参数：无

描述：停止无人机当前动作，包括**取消返航**、**取消起飞**、**取消降落**、**停止任务**

响应主题：CSDK/FlightController/cancelCurrentAction/callback

响应参数：无

响应描述：执行停止当前动作命令的结果


## 重启飞行器

主题：CSDK/FlightController/reboot

参数：无

描述：重启无人机。请勿在飞行器电机起转后进行重启。

响应主题：CSDK/FlightController/reboot/callback

响应参数：无

响应描述：执行重启无人机命令的结果


## 获取/释放虚拟摇杆控制权

主题：CSDK/FlightController/setVirtualStickModeEnabled

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| enabled | boolean | 获取/释放标志 |

描述：开启/关闭虚拟摇杆控制模式。开启后遥控器实体摇杆将失去飞机控制权。

响应主题：CSDK/FlightController/setVirtualStickModeEnabled/callback

响应参数：无

响应描述：获取/释放虚拟摇杆控制权的结果


## 发送虚拟摇杆控制数据

主题：CSDK/FlightController/sendVirtualStickFlightControlData

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| pitch | float | 俯仰轴控制参数 |
| roll | float | 横滚轴控制参数 |
| yaw | float | 偏航轴控制参数 |
| vertical_throttle | float | 垂直方向控制参数 |

描述：发送虚拟摇杆控制数据。俯仰轴，横滚轴，垂直方向采用速度模式控制。偏航轴采用角度模式控制。飞行器飞行采用大地坐标系。

响应主题：无


## RTK 控制组件

### 设置 RTK 控制状态

主题：CSDK/FlightController/RTK/setRtkEnabled

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| enabled | boolean | rtk 控制状态 |

描述：设置飞行器上的RTK模块开启或者关闭，必须在飞行器桨叶起转之前设置，起转之后调用无效。 传入true时表示开启RTK模块，此时飞行器必须有RTK数据才能起飞，且飞控会开始使用RTK模块传入的精准位置信息。传入false时表示关闭RTK模块，此时飞控将不会使用RTK模块的位置信息。

响应主题：CSDK/FlightController/RTK/setRtkEnabled/callback

响应参数：无

响应描述：执行开启/关闭 rtk 命令的结果


### RTK 状态

主题：CSDK/FlightController/RTK/state/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| altitude | float | 无人机高度 |
| latitude | double | 无人机纬度 |
| longitude | double | 无人机经度 |
| heading | float | 无人机偏航角 |
| positioning_solution | PositioningSolution | RTK 模块定位状态 |

描述：RTK 状态数据



