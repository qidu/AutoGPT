# AutoGPT: 构建、部署和运行 AI 智能体

[![Discord Follow](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fdiscord.com%2Fapi%2Finvites%2Fautogpt%3Fwith_counts%3Dtrue&query=%24.approximate_member_count&label=total%20members&logo=discord&logoColor=white&color=7289da)](https://discord.gg/autogpt) &ensp;
[![Twitter Follow](https://img.shields.io/twitter/follow/Auto_GPT?style=social)](https://twitter.com/Auto_GPT) &ensp;

<!-- Keep these links. Translations will automatically update with the README. -->
[Deutsch](https://zdoc.app/de/Significant-Gravitas/AutoGPT) | 
[Español](https://zdoc.app/es/Significant-Gravitas/AutoGPT) | 
[français](https://zdoc.app/fr/Significant-Gravitas/AutoGPT) | 
[日本語](https://zdoc.app/ja/Significant-Gravitas/AutoGPT) | 
[한국어](https://zdoc.app/ko/Significant-Gravitas/AutoGPT) | 
[Português](https://zdoc.app/pt/Significant-Gravitas/AutoGPT) | 
[Русский](https://zdoc.app/ru/Significant-Gravitas/AutoGPT) | 
[中文](https://zdoc.app/zh/Significant-Gravitas/AutoGPT)

**AutoGPT** 是一个强大的平台，允许您创建、部署和管理持续运行的 AI 智能体，以自动化复杂的工作流程。

## 托管选项
   - 下载自托管（免费！）
   - [加入等待列表](https://bit.ly/3ZDijAI) 获取云托管测试版（内测阶段 - 公开发布即将到来！）

## 如何自托管 AutoGPT 平台
> [!NOTE]
> 自行设置和托管 AutoGPT 平台是一个技术性过程。
> 如果您更喜欢开箱即用的解决方案，我们建议[加入等待列表](https://bit.ly/3ZDijAI)获取云托管测试版。

### 系统要求

在进行安装之前，请确保您的系统满足以下要求：

#### 硬件要求
- CPU：建议 4 核以上
- 内存：最低 8GB，建议 16GB
- 存储空间：至少 10GB 可用空间

#### 软件要求
- 操作系统：
  - Linux（建议 Ubuntu 20.04 或更高版本）
  - macOS（10.15 或更高版本）
  - Windows 10/11 with WSL2
- 必需软件（最低版本）：
  - Docker Engine（20.10.0 或更高版本）
  - Docker Compose（2.0.0 或更高版本）
  - Git（2.30 或更高版本）
  - Node.js（16.x 或更高版本）
  - npm（8.x 或更高版本）
  - VSCode（1.60 或更高版本）或任何现代代码编辑器

#### 网络要求
- 稳定的互联网连接
- 访问所需端口（将在 Docker 中配置）
- 能够建立出站 HTTPS 连接

### 更新的设置说明：
我们已迁移到一个完全维护且定期更新的文档站点。

👉 [在这里查看官方自托管指南](https://docs.agpt.co/platform/getting-started/)


本教程假设您已安装 Docker、VSCode、git 和 npm。

---

#### ⚡ 一键快速设置（推荐用于本地托管）

跳过手动步骤，使用我们的自动设置脚本在几分钟内开始使用。

macOS/Linux：
```
curl -fsSL https://setup.agpt.co/install.sh -o install.sh && bash install.sh
```

Windows（PowerShell）：
```
powershell -c "iwr https://setup.agpt.co/install.bat -o install.bat; ./install.bat"
```

这将安装依赖项、配置 Docker 并启动您的本地实例 —— 一气呵成。

### 🧱 AutoGPT 前端

AutoGPT 前端是用户与我们强大的 AI 自动化平台交互的地方。它提供了多种方式来使用和利用我们的 AI 智能体。这是您将 AI 自动化想法变为现实的界面：

   **智能体构建器：** 对于想要自定义的用户，我们直观的低代码界面允许您设计和配置自己的 AI 智能体。
   
   **工作流管理：** 轻松构建、修改和优化您的自动化工作流程。您通过连接块来构建智能体，每个块执行单一操作。
   
   **部署控制：** 管理智能体的生命周期，从测试到生产。
   
   **即用型智能体：** 不想构建？只需从我们的预配置智能体库中选择并立即投入使用。
   
   **智能体交互：** 无论您是自己构建还是使用预配置的智能体，都可以通过我们用户友好的界面轻松运行和交互。

   **监控和分析：** 跟踪智能体的性能并获得洞察，以持续改进您的自动化流程。

[阅读本指南](https://docs.agpt.co/platform/new_blocks/)了解如何构建自己的自定义块。

### 💽 AutoGPT 服务器

AutoGPT 服务器是我们平台的动力源。这是您的智能体运行的地方。部署后，智能体可以由外部源触发并可以持续运行。它包含使 AutoGPT 平稳运行的所有基本组件。

   **源代码：** 驱动我们的智能体和自动化流程的核心逻辑。
   
   **基础设施：** 确保可靠和可扩展性能的强大系统。
   
   **市场：** 一个综合市场，您可以在其中找到和部署各种预构建的智能体。

### 🐙 示例智能体

以下是您可以使用 AutoGPT 做的两个示例：

1. **从热门话题生成病毒式视频**
   - 该智能体读取 Reddit 上的话题。
   - 它识别热门话题。
   - 然后根据内容自动创建短视频。

2. **从视频中识别社交媒体的热门引语**
   - 该智能体订阅您的 YouTube 频道。
   - 当您发布新视频时，它会转录视频。
   - 它使用 AI 识别最有影响力的引语以生成摘要。
   - 然后，它编写帖子自动发布到您的社交媒体。

这些示例只是展示了您可以使用 AutoGPT 实现的一小部分！您可以创建自定义工作流程来为任何用例构建智能体。

---

### **许可证概述：**

🛡️ **Polyform Shield 许可证：**
`autogpt_platform` 文件夹中的所有代码和内容均根据 Polyform Shield 许可证授权。这个新项目是我们正在开发的用于构建、部署和管理智能体的平台。</br>_[了解更多关于这项工作](https://agpt.co/blog/introducing-the-autogpt-platform)_

🦉 **MIT 许可证：**
AutoGPT 存储库的所有其他部分（即 `autogpt_platform` 文件夹之外的所有内容）均根据 MIT 许可证授权。这包括原始的独立 AutoGPT 智能体，以及诸如 [Forge](https://github.com/Significant-Gravitas/AutoGPT/tree/master/classic/forge)、[agbenchmark](https://github.com/Significant-Gravitas/AutoGPT/tree/master/classic/benchmark) 和 [AutoGPT Classic GUI](https://github.com/Significant-Gravitas/AutoGPT/tree/master/classic/frontend) 等项目。</br>我们还在其他存储库中发布根据 MIT 许可证授权的额外工作，例如在 AutoGPT 平台中开发和使用的 [GravitasML](https://github.com/Significant-Gravitas/gravitasml)。另请参阅我们根据 MIT 许可证授权的 [Code Ability](https://github.com/Significant-Gravitas/AutoGPT-Code-Ability) 项目。

---
### 使命
我们的使命是提供工具，以便您可以专注于重要的事情：

- 🏗️ **构建** - 为了不起的事物奠定基础。
- 🧪 **测试** - 将您的智能体调整到完美。
- 🤝 **委托** - 让 AI 为您工作，让您的想法成真。

成为革命的一部分！**AutoGPT** 将继续存在，站在 AI 创新的最前沿。

**📖 [文档](https://docs.agpt.co)**
&ensp;|&ensp;
**🚀 [贡献](CONTRIBUTING.md)**

---
## 🤖 AutoGPT Classic
> 以下是关于 AutoGPT 经典版本的信息。

**🛠️ [构建您自己的智能体 - 快速入门](classic/FORGE-QUICKSTART.md)**

### 🏗️ Forge

**打造您自己的智能体！** &ndash; Forge 是一个即用型工具包，用于构建您自己的智能体应用程序。它处理大部分样板代码，让您可以将所有创造力投入到使*您的*智能体与众不同的事物上。所有教程都位于[这里](https://medium.com/@aiedge/autogpt-forge-e3de53cc58ec)。[`forge`](/classic/forge/) 的组件也可以单独使用，以加速开发并减少智能体项目中的样板代码。

🚀 [**开始使用 Forge**](https://github.com/Significant-Gravitas/AutoGPT/blob/master/classic/forge/tutorials/001_getting_started.md) &ndash;
本指南将引导您完成创建自己的智能体并使用基准测试和用户界面的过程。

📘 [了解更多](https://github.com/Significant-Gravitas/AutoGPT/tree/master/classic/forge)关于 Forge

### 🎯 Benchmark

**衡量您的智能体性能！** `agbenchmark` 可以与任何支持智能体协议的智能体一起使用，与项目的 [CLI] 集成使其在 AutoGPT 和基于 forge 的智能体中更易于使用。基准测试提供严格的测试环境。我们的框架允许自主、客观的性能评估，确保您的智能体为实际行动做好准备。

<!-- TODO: insert visual demonstrating the benchmark -->

📦 Pypi 上的 [`agbenchmark`](https://pypi.org/project/agbenchmark/)
&ensp;|&ensp;
📘 [了解更多](https://github.com/Significant-Gravitas/AutoGPT/tree/master/classic/benchmark)关于基准测试

### 💻 UI

**让智能体易于使用！** `frontend` 为您提供用户友好的界面来控制和监控您的智能体。它通过[智能体协议](#-agent-protocol)连接到智能体，确保与我们生态系统内外的许多智能体兼容。

<!-- TODO: insert screenshot of front end -->

前端开箱即用地与存储库中的所有智能体配合使用。只需使用 [CLI] 运行您选择的智能体！

📘 [了解更多](https://github.com/Significant-Gravitas/AutoGPT/tree/master/classic/frontend)关于前端

### ⌨️ CLI

[CLI]: #-cli

为了尽可能轻松地使用存储库提供的所有工具，在存储库的根目录中包含一个 CLI：

```shell
$ ./run
Usage: cli.py [OPTIONS] COMMAND [ARGS]...

Options:
  --help  Show this message and exit.

Commands:
  agent      Commands to create, start and stop agents
  benchmark  Commands to start the benchmark and list tests and categories
  setup      Installs dependencies needed for your system.
```

只需克隆存储库，使用 `./run setup` 安装依赖项，您就可以开始了！

## 🤔 有问题？遇到问题？有建议？

### 获取帮助 - [Discord 💬](https://discord.gg/autogpt)

[![Join us on Discord](https://invidget.switchblade.xyz/autogpt)](https://discord.gg/autogpt)

要报告错误或请求功能，请创建一个 [GitHub Issue](https://github.com/Significant-Gravitas/AutoGPT/issues/new/choose)。请确保其他人没有为相同主题创建问题。

## 🤝 姊妹项目

### 🔄 Agent Protocol

为了保持统一标准并确保与许多当前和未来应用程序的无缝兼容性，AutoGPT 采用了 AI Engineer Foundation 的[智能体协议](https://agentprotocol.ai/)标准。这标准化了从您的智能体到前端和基准测试的通信路径。

---

## Stars 统计

<p align="center">
<a href="https://star-history.com/#Significant-Gravitas/AutoGPT">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Significant-Gravitas/AutoGPT&type=Date&theme=dark" />
    <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Significant-Gravitas/AutoGPT&type=Date" />
    <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Significant-Gravitas/AutoGPT&type=Date" />
  </picture>
</a>
</p>


## ⚡ 贡献者

<a href="https://github.com/Significant-Gravitas/AutoGPT/graphs/contributors" alt="View Contributors">
  <img src="https://contrib.rocks/image?repo=Significant-Gravitas/AutoGPT&max=1000&columns=10" alt="Contributors" />
</a>
