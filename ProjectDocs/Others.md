## APP 心跳包

主题：CSDK/Manage/live/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| time | String | 当前时间 |
| version_number | String | app版本号 |
| remote_control_id | String | 遥控器序列号 |
| aircraft_id | String | 飞行器序列号 |

描述：APP 心跳包，每秒发送一次


## 其他异常信息

主题：CSDK/APP/error/callback

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
|  | CSDKError | 异常信息 |

描述：APP 数据解析或线程运行等异常信息