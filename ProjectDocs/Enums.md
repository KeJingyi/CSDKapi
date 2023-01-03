## PositioningSolution

| 常量值 | 常量描述 |
| :------: | :------: |
| NONE | 未定位 |
| SINGLE_POINT | 单点定位 |
| FLOAT | 浮动定位 |
| FIXED_POINT | 定点定位 |


## CameraVideoStreamSource

| 常量值 | 常量描述 |
| :------: | :------: |
| DEFAULT | 默认镜头，单镜头相机默认使用此镜头类型 |
| WIDE | 广角镜头 |
| ZOOM | 变焦镜头 |
| INFRARED_THERMAL | 红外镜头 |
| VISIBLE | 可见光。在 Mavic 3 Enterprise 系列机型上，广角和变焦统一用可见光镜头实现 |


## CameraMode

| 常量值 | 常量描述 |
| :------: | :------: |
| SHOOT_PHOTO | 拍照模式 |
| RECORD_VIDEO | 录像模式 |
| PLAYBACK | 回放模式 |
| MEDIA_DOWNLOAD | 下载模式 |
| BROADCAST | 广播模式 |


## StorageLocation

| 常量值 | 常量描述 |
| :------: | :------: |
| SDCARD | SD 卡 |
| INTERNAL_STORAGE | 机载存储器 |


## MediaType

| 常量值 | 常量描述 |
| :------: | :------: |
| JPEG | JPEG 格式（照片） |
| MP4 | MP4 格式（视频） |
| MOV | MOV 格式（视频） |
| *DNG* | *DNG 格式（照片）* |


## RotationMode

| 常量值 | 常量描述 |
| :------: | :------: |
| RELATIVE_ANGLE | 相对角度 |
| ABSOLUTE_ANGLE | 绝对角度 |
| SPEED | 速度 |


## WaypointMissionHeadingMode

| 常量值 | 常量描述 |
| :------: | :------: |
| AUTO | 自动（沿航线方向） |
| USING_WAYPOINT_HEADING | 使用航点自定义航向 |
| USING_INITIAL_DIRECTION | 使用飞机起飞时航向（固定） |
| CONTROL_BY_REMOTE_CONTROLLER | 手动控制 |


## WaypointMissionFinishedAction

| 常量值 | 常量描述 |
| :------: | :------: |
| NO_ACTION | 悬停 |
| GO_HOME | 返航 |
| AUTO_LAND | 降落 |
| GO_FIRST_WAYPOINT | 返回首航点 |
| BEYOND_LANDING | 异地降落 |


## WaypointMissionGotoWaypointMode

| 常量值 | 常量描述 |
| :------: | :------: |
| SAFELY | 安全模式（上升到安全高度再飞向首航点） |
| POINT_TO_POINT | 倾斜飞至首航点 |


## AltitudeMode

| 常量值 | 常量描述 |
| :------: | :------: |
| ABSOLUTE | 绝对高度（海拔） |
| RELATIVE | 相对高度 |


## WaypointV2FlightPathMode

| 常量值 | 常量描述 |
| :------: | :------: |
| CURVATURE_CONTINUOUS_PASSED | 曲线飞行，过点不停 |
| GOTO_POINT_CURVE_AND_STOP | 曲线飞行，到点停 |
| GOTO_POINT_STRAIGHT_LINE_AND_STOP | 直线飞行，到点停 |
| COORDINATE_TURN | 协调转弯 |


## WaypointV2HeadingMode

| 常量值 | 常量描述 |
| :------: | :------: |
| AUTO | 自动（沿航线方向） |
| FIXED | 固定 |
| WAYPOINT_CUSTOM | 使用航点自定义航向 |
| MANUAL | 手动控制 |
| GIMBAL_YAW_FOLLOW | 跟随云台偏航角方向 |


## WaypointActionType

| 常量值 | 常量描述 |
| :------: | :------: |
| STAY | 悬停 |
| START_TAKE_PHOTO | 拍照 |
| START_RECORD | 开始录像 |
| STOP_RECORD | 停止录像 |
| ROTATE_AIRCRAFT | 旋转飞机 |
| GIMBAL_PITCH | 云台俯仰角控制 |
| CAMERA_ZOOM | 相机变焦 |
| CAMERA_FOCUS | 相机对焦 |