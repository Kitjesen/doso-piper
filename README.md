# AgileX Piper 控制资料包

本目录用于松灵（AgileX）Piper 系列机械臂的控制接入。

## 本地入口

- 主 SDK：[`vendor/agilex/pyAgxArm`](vendor/agilex/pyAgxArm/README.md)
- Windows USB-CAN 后端：[`vendor/agilex/python-can-agx-cando`](vendor/agilex/python-can-agx-cando/README.md)
- ROS2 驱动：[`vendor/agilex/agx_arm_ros`](vendor/agilex/agx_arm_ros/README.md)
- 旧版 SDK（仅兼容参考）：[`vendor/agilex/piper_sdk`](vendor/agilex/piper_sdk/README%28ZH%29.MD)
- 资料与版本清单：[`docs/agilex/README.md`](docs/agilex/README.md)
- 第三方来源与许可证：[`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md)

当前只完成官方源码和资料下载，尚未安装 Python 包，也没有向机械臂发送控制帧。

`vendor/` 下的上游仓库已按固定提交展开为可直接浏览的源码快照，不包含上游 Git 元数据；各组件继续适用其原始许可证。
