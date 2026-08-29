# AgileX Piper SDK 与资料清单

下载日期：2026-08-29

## 推荐使用顺序

1. 新项目使用 `pyAgxArm`，不要以旧 `piper_sdk` 作为主实现。
2. Windows 原生控制使用 `pyAgxArm` + `python-can-agx-cando`。
3. Linux/WSL2 使用 `pyAgxArm` + SocketCAN；Piper CAN 波特率为 `1,000,000 bit/s`。
4. CAN 读写和固件识别跑通后，再接入 `agx_arm_ros` 与 MoveIt。

## 已下载仓库

| 用途 | 本地路径 | 分支 | 提交 | 版本 |
| --- | --- | --- | --- | --- |
| 主 Python SDK | `vendor/agilex/pyAgxArm` | `master` | `2255d88e1fab` | `1.0.0` |
| Windows CANDO 后端 | `vendor/agilex/python-can-agx-cando` | `master` | `b222c4027ad4` | `0.0.1` |
| ROS2 驱动 | `vendor/agilex/agx_arm_ros` | `ros2` | `77882f4305c5` | 多 ROS 包 |
| 旧版 Piper SDK | `vendor/agilex/piper_sdk` | `master` | `c9e8a28174e7` | `0.6.2` |

ROS2 仓库的 `agx_arm_urdf` 子模块也已下载，提交为 `f6642ce0d7872c686f29c99e9e10cd23d1d49313`。

## 关键本地文档

- Piper API：[`vendor/agilex/pyAgxArm/docs/piper/piper_api.md`](../../vendor/agilex/pyAgxArm/docs/piper/piper_api.md)
- Piper 固件匹配表：[`vendor/agilex/pyAgxArm/docs/piper/firmware_reference.md`](../../vendor/agilex/pyAgxArm/docs/piper/firmware_reference.md)
- CAN 模块说明：[`vendor/agilex/pyAgxArm/docs/can_user.md`](../../vendor/agilex/pyAgxArm/docs/can_user.md)
- WSL2 USB-CAN 指南：[`vendor/agilex/pyAgxArm/docs/wsl2_usb_can_guide.md`](../../vendor/agilex/pyAgxArm/docs/wsl2_usb_can_guide.md)
- Windows 后端说明：[`vendor/agilex/python-can-agx-cando/README.md`](../../vendor/agilex/python-can-agx-cando/README.md)
- ROS2 使用说明：[`vendor/agilex/agx_arm_ros/README.md`](../../vendor/agilex/agx_arm_ros/README.md)
- ROS2 CAN 配置：[`vendor/agilex/agx_arm_ros/docs/CAN_USER.md`](../../vendor/agilex/agx_arm_ros/docs/CAN_USER.md)
- 旧版 V2 接口文档：[`vendor/agilex/piper_sdk/asserts/V2/INTERFACE_V2.MD`](../../vendor/agilex/piper_sdk/asserts/V2/INTERFACE_V2.MD)
- 旧版常见问题：[`vendor/agilex/piper_sdk/asserts/Q&A.MD`](../../vendor/agilex/piper_sdk/asserts/Q&A.MD)

## 已下载手册

- [`Piper_Quick_Start_EN.pdf`](Piper_Quick_Start_EN.pdf)
  - 来源：`https://static.generation-robots.com/media/agilex-piper-user-manual.pdf`
  - 大小：1,502,344 bytes
  - SHA-256：`F13613899C80719B5A407CC69894338588CDF87A521562F1091C9A30AA3752F2`
  - 已验证文件头为 `%PDF-1.5`，共 12 页；全部页面已成功渲染并完成可读性检查。

官方中文快速手册地址已确认，但下载时松灵服务器出现 TLS 证书过期，忽略证书后仍返回 HTTP 502，因此没有保存损坏或不完整文件：

`https://new.agilex.ai/raw/upload/20241017/%EF%BC%88%E5%B7%B2%E5%8E%8B%E7%BC%A9%EF%BC%89%E6%AD%A3-PiPER%E4%BD%BF%E7%94%A8%E6%89%8B%E5%86%8C_%E4%B8%AD%E6%96%87%E7%89%880925_52071.pdf`

## 当前 USB-CAN 线索

本机 Windows PnP 历史中存在 `candleLight USB to CAN adapter`，硬件 ID 为 `VID_1D50&PID_606F`，与官方 WSL2 指南示例一致。检查时设备状态为 `Unknown`，没有作为当前在线设备枚举；首次连机前仍需重新插拔或检查 USB 连接/驱动。

## 上游地址

- https://github.com/agilexrobotics/pyAgxArm
- https://github.com/agilexrobotics/python-can-agx-cando
- https://github.com/agilexrobotics/agx_arm_ros
- https://github.com/agilexrobotics/piper_sdk
