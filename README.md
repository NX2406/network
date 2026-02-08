# Network Traffic Burner (Linux 流量消耗/测速脚本)

这是一个简单高效的 Linux 流量消耗脚本。支持**单向只跑下行**、**单向只跑上行**以及**双向循环**模式。

主要用于消耗 VPS 或服务器每月未使用的流量额度，防止流量清零浪费。

## 🚀 特性 (Features)

- **交互式菜单**：小白友好，一键选择模式。
- **自动依赖管理**：自动检测并安装 `wget`, `python3`, `speedtest-cli` 等必要组件。
- **多模式支持**：
    - 📥 **只跑下行**：使用 `wget` 下载大文件到 `/dev/null`（不占用磁盘空间，速度最快）。
    - 📤 **只跑上行**：使用 `speedtest-cli` 模拟上传。
    - 🔄 **双向循环**：先下载后上传，无限循环。
- **无残留**：脚本运行结束后不会在系统留下垃圾文件。

## 🛠 使用方法 (Usage)

### 一键运行 (One-Click Command)

复制以下命令到终端即可直接运行：

```bash
bash <(curl -sL https://raw.githubusercontent.com/NX2406/network/main/Data%20usage)
