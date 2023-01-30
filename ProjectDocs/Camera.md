## 拍摄照片

主题：CSDK/Camera/startShootPhoto

参数：无

描述：拍摄照片

响应主题：CSDK/Camera/startShootPhoto/callback

响应参数：无

响应描述：执行拍照命令的结果


## 开始录制视频

主题：CSDK/Camera/startRecordVideo

参数：无

描述：开始录制视频

响应主题：CSDK/Camera/startRecordVideo/callback

响应参数：无

响应描述：执行开始录制视频命令的结果


## 停止录制视频

主题：CSDK/Camera/stopRecordVideo

参数：无

描述：停止录制视频

响应主题：CSDK/Camera/stopRecordVideo/callback

响应参数：无

响应描述：执行停止录制视频命令的结果


## 设置图传视频源

主题：CSDK/Camera/setCameraVideoStreamSource

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| source | CameraVideoStreamSource | 视频源类型 |

描述：设置图传视频源

响应主题：CSDK/Camera/setCameraVideoStreamSource/callback

响应参数：无

响应描述：执行设置视频源命令的结果


## 设置相机模式

主题：CSDK/Camera/setMode

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| payload_index | int | 负载索引 |
| mode | CameraMode | 相机模式 |

描述：设置相机工作模式

响应主题：CSDK/Camera/setMode/callback

响应参数：无

响应描述：执行设置相机工作模式的结果


## 设置单次变焦

主题：CSDK/Camera/setOpticalZoomFactor

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| payload_index | int | 负载索引 |
| factor | float | 变焦倍数 |

描述：设置单次变焦

响应主题：CSDK/Camera/setOpticalZoomFactor/callback

响应参数：无

响应描述：执行设置单次变焦命令的结果


## 格式化相机

主题：CSDK/Camera/format/callback

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| location | StorageLocation | 存储位置 |

描述：格式化相机

响应主题：CSDK/Camera/format/callback

响应参数：无

响应描述：执行格式化相机命令的结果


## 生成媒体文件监听

主题：CSDK/Camera/MediaFileCallback/listener

参数：MediaFile

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| payload_index | int | 负载索引 |
| valid | boolean | 文件有效值 |
| index | int | 文件索引 |
| type | MediaType | 媒体文件类型 |
| name | String | 文件名称 |
| size | long | 文件大小（字节） |
| date | String | 文件生成时间 |
| *storage_location* | *StorageLocation* | *存储位置* |
| *id* | *String* | *服务器传过来的文件Id* |

描述：当启动拍照或者录像后，相机会产生新的照片或者视频，可以通过这个接口获取产生的媒体文件信息


## 设置红外分屏模式

主题：CSDK/Camera/splitScreen

参数：无

描述：设置红外分屏模式，仅支持带红外摄像头的机型（M30T，M3T，H20T）

响应主题：CSDK/Camera/splitScreen/callback

响应参数：无

响应描述：执行设置红外分屏模式的结果


## 开始拍摄全景照片

主题：CSDK/Camera/startShootPanoramaPhoto

参数：无

描述：拍摄全景照片。此接口需在飞行状态下调用，飞行器会旋转机身和云台，拍摄25张照片，最后合成一张全景图，生成的全景照片可在**生成媒体文件监听**接口中获取到

响应主题：CSDK/Camera/startShootPhoto/callback

响应参数：无

响应描述：拍摄全景照片的结果
