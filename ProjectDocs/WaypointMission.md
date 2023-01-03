## 加载任务

主题：CSDK/Waypoint/loadMission

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
|  | WaypointMission | 航点任务对象 |

描述：加载航线任务对象

响应主题：CSDK/Waypoint/loadMission/callback

响应参数：无

响应描述：任务加载结果

### WaypointMission

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| name | String | 任务名 |
| auto_flight_speed | int | 自动飞行速度（1~15m/s） |
| max_flight_speed | int | 最大飞行速度（1~15m/s） |
| safetyHeight | float | 安全起飞/返航高度（相对高度） |
| heading_mode | WaypointMissionHeadingMode | 飞机偏航角模式，默认为 AUTO |
| finished_action | WaypointMissionFinishedAction | 结束动作，默认为NO_ACTION |
| goto_first_waypoint_mode | WaypointMissionGotoWaypointMode | 飞向第一个航点的模式，默认为 SAFELY |
| exit_mission_on_rc_signal_lost_enabled | boolean | 遥控失联时是否退出任务，默认为 true |
| altitude_mode | AltitudeMode | 航点高度模式，默认为 ABSOLUTE |
| waypoints | Waypoint[]  | 航点数组，按照航点执行顺序插入 |
| waypointList | List < Waypoint > | 航点列表，按照航点执行顺序插入 |
| machineNestType | MachineNestType | 机巢类型 |
| machine_nest_id | String | 机巢ID |
| original_machine_nest_info | BeyondLandingInfo | 原机巢信息 |
| original_alternate_point | BeyondLandingInfo | 原备降点信息 |
| machineNestValue | MachineNestValue | （可选）三层机巢控制参数 |
| next_machine_nest_id | String | （可选）下一机巢ID |
| next_machine_nest_info | BeyondLandingInfo | （可选）下一机巢信息 |
| next_alternate_point | BeyondLandingInfo | （可选）下一备降点信息 |
| repeat_times | int | （可选）任务重复次数，默认为 1 |

描述：JSON数据结构，用于描述航点任务对象，具体参数参考常量表

#### Waypoint

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| index | int | 航点索引 |
| latitude | double | 纬度 |
| longitude | double | 经度 |
| altitude | float | 高度 |
| heading | int | 机头方向 -180~180 |
| gimbal_pitch | float | 云台俯仰角 |
| actions | WaypointAction[] | （可选）航点动作数组，动作插入顺序为动作执行顺序 |
| actionList | List < WaypointAction > | （可选）航点动作列表，动作插入顺序为动作执行顺序 |
| flight_path_mode | WaypointV2FlightPathMode | （可选）飞行路径模式，默认为GOTO_POINT_STRAIGHT_LINE_AND_STOP |
| heading_mode | WaypointV2HeadingMode | 转向模式 |

##### WaypointAction

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| index | int | 动作索引 |
| action_param | float | （可选）动作参数，当动作类型 action_type 配置不同值时，此参数代表不同意思，具体见大疆文档 |
| action_type | WaypointActionType | 动作类型 |
| file_custom_name | String | （可选）照片重命名 |


## 开始执行任务

主题：CSDK/Waypoint/startMission

参数：无

描述：开始执行航线任务

响应主题：CSDK/Waypoint/startMission/callback

响应参数：无

响应描述：开始执行任务的结果


## 暂停任务

主题：CSDK/Waypoint/interruptMission

参数：无

描述：暂停执行中的任务

响应主题：CSDK/Waypoint/interruptMission/callback

响应参数：无

响应描述：暂停任务的结果


## 恢复任务

主题：CSDK/Waypoint/recoverMission

参数：无

描述：恢复执行中断/暂停的航线任务

响应主题：CSDK/Waypoint/recoverMission/callback

响应参数：无

响应描述：恢复执行任务的结果


## 停止任务

主题：CSDK/Waypoint/stopMission

参数：无

描述：停止执行航点任务

响应主题：CSDK/Waypoint/stopMission/callback

响应参数：无

响应描述：停止航点任务的结果


## 任务状态

主题：CSDK/Waypoint/state/listener

参数：

| 参数名称 | 参数类型 | 参数描述 |
| :------: | :------: | :------: |
| waypoint_index | int | 当前执行的航点索引 |
| total_waypoint_count | float | 航点总数 |
| state | WaypointState | 任务状态 |
| uploadEvent | WaypointMissionUploadEvent | 任务上传状态 |
| error | CSDKError | 执行任务遇到的异常 |
| onMissionExecutionStart | boolean | 任务开始 |
| onMissionExecutionStopped | boolean | 任务结束 |
| onMissionExecutionFinish | CSDKError | 任务执行完成 |

描述：发布当前任务状态；该状态的部分参数在特定机型上有缺失