# Video Temporal Labeling Tool

[English](README.md) | [中文](README.zh.md) | [日本語](README.ja.md)

A wxPython-based GUI application for temporal video data labeling. It records temporal labels for videos and stores the corresponding start and end frame indices.

![UI](./UI.png)

## Features

- 🎥 Support multiple video formats (.avi, .mp4, .mov, .mkv, .wav)
- 🏷️ Temporal labeling with start/end frame selection
- 🎯 Multiple action types (tripping, faceoff, customizable)
- 📐 Shot type classification (close, mid, far)
- ⚡ Adjustable frame step interval (5, 10, 15, 20, 30 FPS)
- 💾 CSV export for labeled data
- 🖥️ Cross-platform support (Windows, macOS, Linux)

## Requirements

- Python >= 3.9 (Recommended: 3.12 LTS)
- wxPython >= 4.2.0
- pandas >= 2.0.0
- opencv-python >= 4.9.0
- numpy >= 1.24.0

## Installation

### From PyPI (Coming Soon)

```bash
pip install vtlt
```

### From Source

```bash
# Clone the repository
git clone https://github.com/jokebear-bot/VideoTemporalLabelingTool.git

# Navigate to directory
cd VideoTemporalLabelingTool

# Install dependencies
pip install -r requirements.txt

# Or install as a package
pip install -e .
```

## Quick Start

### Run directly

```bash
# Run from source
python -m vtlt

# Or using the entry point (after pip install)
vtlt
```

### Usage

1. **Set Dataset Path**: Enter the path to your video dataset directory
2. **Set Store Path**: Enter the path where labels will be saved
3. **Select Video**: Use Previous/Next buttons to navigate videos
4. **Navigate Frames**: Use +/- buttons or FPI (Frames Per Interval) to move through frames
5. **Mark Start/End**: Click "Start" and "End" buttons to mark temporal boundaries
6. **Select Type**: Choose shot type (Close/Mid/Far)
7. **Save Label**: Click "Save" to store the label to CSV

## Project Structure

```
VideoTemporalLabelingTool/
├── src/
│   └── vtlt/
│       ├── __init__.py      # Package initialization
│       ├── app.py           # GUI application
│       ├── service.py       # Business logic
│       └── resource/        # Resource files
├── tests/                   # Unit tests
├── requirements.txt         # Dependencies
├── pyproject.toml          # Project configuration
├── README.md               # This file
└── CHANGELOG.md            # Version history
```

## Development

### Setup Development Environment

```bash
# Install development dependencies
pip install -e ".[dev]"

# Run tests
pytest

# Format code
black src/
ruff check src/

# Type checking
mypy src/
```

### Building Package

```bash
python -m build
```

## Compatibility

| Python Version | Status |
|---------------|--------|
| 3.9 | ✅ Supported |
| 3.10 | ✅ Supported |
| 3.11 | ✅ Supported |
| 3.12 | ✅ Recommended (LTS) |

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Credits

- Original Author: Pengnan Fan
- Modernized for Python 3.12 compatibility
