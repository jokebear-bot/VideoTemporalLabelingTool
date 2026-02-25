# 视频时间标注工具

[English](README.md) | [中文](README.zh.md) | [日本語](README.ja.md)

基于 wxPython 的图形界面视频时间标注应用。用于记录视频的时间标签，并存储对应的起始和结束帧索引。

![UI](./UI.png)

## 功能特点

- 🎥 支持多种视频格式（.avi, .mp4, .mov, .mkv, .wav）
- 🏷️ 时间标注，支持起始/结束帧选择
- 🎯 多种动作类型（绊倒、争球，可自定义）
- 📐 镜头类型分类（近景、中景、远景）
- ⚡ 可调整的帧步进间隔（5, 10, 15, 20, 30 FPS）
- 💾 CSV 格式导出标注数据
- 🖥️ 跨平台支持（Windows, macOS, Linux）

## 系统要求

- Python >= 3.9（推荐：3.12 LTS）
- wxPython >= 4.2.0
- pandas >= 2.0.0
- opencv-python >= 4.9.0
- numpy >= 1.24.0

## 安装方法

### 从 PyPI 安装（即将推出）

```bash
pip install vtlt
```

### 从源码安装

```bash
# 克隆仓库
git clone https://github.com/jokebear-bot/VideoTemporalLabelingTool.git

# 进入目录
cd VideoTemporalLabelingTool

# 安装依赖
pip install -r requirements.txt

# 或作为包安装
pip install -e .
```

## 快速开始

### 直接运行

```bash
# 从源码运行
python -m vtlt

# 或使用入口点（pip 安装后）
vtlt
```

### 使用说明

1. **设置数据集路径**：输入视频数据集目录的路径
2. **设置存储路径**：输入标签保存的路径
3. **选择视频**：使用上/下按钮切换视频
4. **浏览帧**：使用 +/- 按钮或 FPI（每间隔帧数）浏览帧
5. **标记起止**：点击"开始"和"结束"按钮标记时间边界
6. **选择类型**：选择镜头类型（近景/中景/远景）
7. **保存标签**：点击"保存"将标签存储到 CSV

## 项目结构

```
VideoTemporalLabelingTool/
├── src/
│   └── vtlt/
│       ├── __init__.py      # 包初始化
│       ├── app.py           # GUI 应用
│       ├── service.py       # 业务逻辑
│       └── resource/        # 资源文件
├── tests/                   # 单元测试
├── requirements.txt         # 依赖项
├── pyproject.toml          # 项目配置
├── README.md               # 英文文档
└── CHANGELOG.md            # 版本历史
```

## 开发

### 设置开发环境

```bash
# 安装开发依赖
pip install -e ".[dev]"

# 运行测试
pytest

# 格式化代码
black src/
ruff check src/

# 类型检查
mypy src/
```

### 构建包

```bash
python -m build
```

## 兼容性

| Python 版本 | 状态 |
|------------|------|
| 3.9 | ✅ 支持 |
| 3.10 | ✅ 支持 |
| 3.11 | ✅ 支持 |
| 3.12 | ✅ 推荐（LTS）|

## 更新日志

详见 [CHANGELOG.md](CHANGELOG.md)。

## 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

## 致谢

- 原作者：Pengnan Fan
- Python 3.12 兼容性现代化
