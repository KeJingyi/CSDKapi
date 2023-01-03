## 开始推流

主题：CSDK/Camera/live/start

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| url | String | RTMP推流地址 |
| token | String | 声网令牌 |
| type | int | 推流类型 |

描述：开启推流直播，挂载多云台时默认推送左云台视频流。可选声网或 RTMP 推流。声网类型码为 1，发送token；RTMP 类型码为 2，发送 url

响应主题：CSDK/Camera/live/start/callback

响应参数：无

响应描述：执行开始推流结果


## 停止推流

主题：CSDK/Camera/live/stop

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| type | int | 推流类型 |

描述：停止推流直播

响应主题：CSDK/Camera/live/stop/callback

响应参数：无

响应描述：执行停止推流结果


## 推流状态

主题：CSDK/Camera/live/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| video_bitRate | int | 视频码率 |
| audio_bitRate | int | 音频码率 |
| video_fps | float | 视频帧率 |
| video_cache_size | int | 直播的包缓冲队列长度 |
| video_resolution | LiveVideoResolution | 视频分辨率 |

描述：推流直播状态
