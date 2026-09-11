# FITS Header Editor

> 浏览器端快速、安全地查看、编辑、添加与导出天文 **FITS**（`.fits`、`.fit`、`.fts`）头文件元数据的在线工具，完全在客户端本地运行。
>
> 🔗 **在线工具**: [https://abctool.info/fits-header-editor-online/](https://abctool.info/fits-header-editor-online/)
>
> 🌐 [English](README.md) | [Español](README.es.md) | **中文** | [日本語](README.ja.md)

---

## 简介

在传统工作流中，查看或修改天文 FITS 文件头元数据通常需要安装庞大的专业桌面软件（例如 SAOImage DS9、AstroImageJ、PixInsight），或者编写使用 `astropy.io.fits` 的 Python 脚本。

**[FITS Header Editor Online](https://abctool.info/fits-header-editor-online/)** 将完整的 FITS 文件头查看与编辑能力直接带入您的网页浏览器：
- **100% 本地运行与隐私保护**：文件解析和处理均在浏览器本地完成，天文图像与元数据绝不上传到任何服务器。
- **免安装随开即用**：支持 Windows、macOS、Linux、平板等任何配备现代浏览器的设备。
- **实时文件头编辑**：实时增、删、改、排 80 字符标准 FITS 卡片。
- **灵活的导出格式**：一键保存并下载修改后的 `.fits` 完整文件，也可将元数据单独导出为 JSON 或 TXT 格式。

---

## 使用指南

### 1. 导入 FITS 文件

打开 [FITS Header Editor Online](https://abctool.info/fits-header-editor-online/)，首先看到的是文件导入界面：

![FITS Header Editor Online - 文件导入界面](./src/img/1-fits-header-viewer-editor.png)

- **选择或拖拽文件**：直接将 `.fits`、`.fit` 或 `.fts` 文件拖拽至虚线区域，或点击 **Select FITS File** 选择文件。
- **加载示例文件**：若想快速体验功能，点击 **Load Sample FITS** 即可一键载入内置的天文样例文件（`13838SgrA.fits`）。

---

### 2. 查看与检索元数据

导入文件后，将展示完整的交互式文件头编辑表格：

![FITS Header Editor Online - 编辑器界面](./src/img/2-fits-header-editor-ui.png)

- **文件概览信息**：顶部横幅显示文件名、文件大小、Header Cards 总数以及 HDU 类型（如 `Primary HDU`）。
- **即时搜索**：使用搜索框（`Search keywords, values, comments...`）快速根据关键字名称、数值或注释进行即时过滤。
- **分类标签筛选**：按常用天文功能分类快速筛选卡片：
  - **All**：按序查看所有卡片。
  - **Target & Coord**：目标天体名称、赤经/赤纬坐标（RA/DEC）、历元等。
  - **Camera & Optics**：曝光时间、增益（Gain）、滤镜名称、焦距、像元尺寸。
  - **WCS Coordinates**：天体测量投影标准坐标参数（CRVAL、CRPIX、CD 矩阵）。
  - **Structural**：FITS 基础结构卡片（SIMPLE、BITPIX、NAXIS、EXTEND 等）。

---

### 3. 编辑、添加与管理关键字

编辑表格提供细致的卡片管理功能：

- **编辑数值与类型**：支持行内直接修改值与类型。布尔型提供便捷的下拉选择（`T (True)` / `F (False)`），字符串与数值类型可直接输入。
- **天文快捷键（Quick Helpers）**：点击预置的常用天文参数按钮，一键插入对应标准键：
  - `+ OBJECT`（目标天体名称）
  - `+ EXPTIME`（曝光时间/秒）
  - `+ FILTER`（光学滤镜）
  - `+ BAYERPAT`（拜耳色彩阵列排列）
  - `+ GAIN`（传感器增益）
  - `+ FOCALLEN`（望远镜焦距）
  - `+ PIXSIZE`（像元物理尺寸）
  - `+ OBSERVER`（观测者/拍摄者名称）
- **自定义关键字**：点击 **+ Add Keyword** 即可创建任意自定义 FITS 卡片，支持指定类型、键值与注释。
- **调序与删除**：点击右侧上下箭头（`↑`、`↓`）调整卡片排列顺序，点击（`✕`）删除不需要的卡片。
- **重置更改**：点击右上角 **Reset** 可随时撤销所有未保存的改动，恢复文件初始状态。

---

### 4. 保存与导出

完成编辑后：
- **Save & Download FITS**：重新打包更新后的文件头与原始图像二进制数据，直接生成并下载标准的 `.fits` 文件。
- **Export JSON**：将所有文件头卡片导出为结构化 JSON 键值对，方便后续脚本分析与自动化处理。
- **Export TXT**：导出干净的标准纯文本 FITS 头文件内容。

---

## 支持格式与兼容性

| 特性 | 说明 |
| :--- | :--- |
| **支持的文件扩展名** | `.fits`, `.fit`, `.fts` |
| **HDU 支持** | Primary HDU 及标准图像扩展 |
| **规范标准** | 遵循 NASA / IAU 标准 80 列 FITS 卡片格式规范 |
| **安全与隐私** | 100% 浏览器本地运行（WebAssembly / JavaScript），无需上传云端 |

---

## 访问在线工具

👉 立即在浏览器中使用：**[https://abctool.info/fits-header-editor-online/](https://abctool.info/fits-header-editor-online/)**
