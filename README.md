<div align="center">

# 🕷️ Spider

**Python 爬虫与逆向工程练习集**

[![Language](https://img.shields.io/badge/language-Python-blue.svg)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/panghehe666/spider/pulls)

*记录爬虫学习路上的各种技巧：JS 逆向、字体反爬、小说下载、聊天机器人……*

</div>

---

## 📖 项目简介

本仓库是我在学习 **网络爬虫** 与 **反爬对抗** 过程中积累的一系列实战小脚本，涵盖：

- 🔓 **JS 逆向** —— 破解前端加密参数，模拟真实请求
- 🔤 **字体反爬** —— 解析自定义 WOFF 字体映射，还原被混淆的文本
- 📚 **小说爬取** —— 多分页章节自动下载与本地保存
- 🤖 **趣味机器人** —— 基于图灵 API 的命令行聊天机器人

每个脚本都聚焦于一个具体技巧，代码精简、注释到位，适合爬虫初学者参考学习。

## 📂 项目结构

```
spider/
├── JS逆向有道词典翻译.py   # 逆向有道翻译接口的 sign/bv 加密参数
├── 反字体加密.py           # 下载并解析 WOFF 字体，还原字体加密文本
├── 舔狗机器人.py           # 图灵聊天机器人 + 搜狗搜索联动
├── book/
│   ├── 居家小说.py         # 小说章节批量下载（支持多分页、去重、礼貌延时）
│   └── find.py             # 目录文件遍历小工具
└── README.md
```

## ✨ 亮点一览

| 脚本 | 核心技术 | 说明 |
| --- | --- | --- |
| `JS逆向有道词典翻译.py` | MD5 签名、时间戳加盐、requests | 还原有道翻译网页版的 `sign`、`lts`、`salt` 等加密参数生成逻辑，实现命令行即时翻译 |
| `反字体加密.py` | fontTools、字体映射表 | 针对自定义字体反爬，建立 `uniXXXX` 字形编码与真实字符的映射，批量替换还原原文 |
| `book/居家小说.py` | BeautifulSoup、异常重试、礼貌延时 | 自动构造章节 URL，处理一章多分页的情况，去重后按章节保存为 txt |
| `舔狗机器人.py` | 图灵 API、网页解析 | 命令行聊天机器人，输入「搜索」可联动网页检索 |

## 🚀 快速开始

### 环境要求

- Python 3.7+

### 安装依赖

```bash
pip install requests beautifulsoup4 jsonpath fontTools
```

### 运行示例

```bash
# 命令行翻译（逆向有道接口）
python JS逆向有道词典翻译.py

# 小说下载
cd book && python 居家小说.py

# 聊天机器人
python 舔狗机器人.py
```

## ⚠️ 免责声明

> 本仓库所有代码**仅供学习与技术交流使用**，请勿用于任何商业用途或非法用途。
> 爬取数据时请遵守目标网站的 `robots.txt` 协议及相关法律法规，控制请求频率，文明爬虫。
> 因使用本仓库代码产生的一切后果，由使用者自行承担。

## 🤝 贡献

欢迎提交 Issue 和 Pull Request，一起交流爬虫技巧！

---

<div align="center">

如果这个项目对你有帮助，欢迎点个 ⭐ Star 支持一下～

</div>
