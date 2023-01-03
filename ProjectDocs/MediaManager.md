*此模块所有 MediaFile 相关参数参见**相机**-**生成媒体文件监听**接口*

## 获取媒体文件列表

主题：CSDK/Camera/Media/getFileList

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| storage_location | StorageLocation | 存储位置 |

描述：获取飞机机体内存或 sd 卡中的媒体文件列表

响应主题：CSDK/Camera/Media/getFileList/callback

响应参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| media_file_list | List < MediaFile > | 媒体文件列表 |

响应描述：从飞机获取到的媒体文件列表


## 上传媒体文件

主题：CSDK/Camera/Media/uploadFile

参数：MediaFile

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| index | int | 文件索引 |
| id | String | 服务器传过来的文件Id |

描述：根据 index 获取对应文件并用 id 命名上传到服务器。除此之外的 MediaFile 参数非必需

响应主题：CSDK/Camera/Media/uploadFile/callback

响应参数：无

响应描述：上传媒体文件结果


## 上传媒体文件列表

主题：CSDK/Camera/Media/uploadFileList

响应参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| media_file_list | List < MediaFile > | 媒体文件列表 |

描述： MediaFile 的必要参数及逻辑见**上传媒体文件**接口

响应主题：CSDK/Camera/Media/uploadFile/callback

响应参数：无

响应描述：上传媒体文件列表结果


## 删除媒体文件

主题：CSDK/Camera/Media/deleteFile

参数：MediaFile

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| index | int | 文件索引 |

描述：根据 MediaFile 对象的 index 在飞机中获取对应文件并删除

响应主题：CSDK/Camera/Media/deleteFile/callback

响应参数：无

响应描述：删除媒体文件结果
