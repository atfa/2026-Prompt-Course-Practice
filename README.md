# LLM开发实践课仓库

本仓库是LLM（大语言模型）开发实践课的代码仓库，包含了一系列实践项目，从基础的API调用到复杂的工具调用和文档仓库访问。

## 目录结构

```
├── practice01/          # 基础LLM API调用实践
├── practice02/          # 工具调用基础实践
├── practice03/          # 文件操作和网络访问工具实践
├── practice04/          # 聊天历史管理实践
├── practice05/          # AnythingLLM文档仓库访问实践
├── tools/               # 工具文件
├── .env                 # 环境变量配置文件
├── log.txt              # 聊天历史和关键信息日志
└── README.md            # 项目说明文件
```

## 子目录说明

### practice01 - 基础LLM API调用实践

**文件说明**：
- `chat_client.py`：实现流式调用LLM API的聊天客户端，支持多轮对话，实时显示模型响应
- `llm_client.py`：实现单次调用LLM API并统计性能指标，包括执行时间和Token使用情况
- `prompt01.txt`：系统提示词配置文件

**功能**：
- 基于HTTP协议的LLM API调用
- 流式和非流式两种API调用方式
- 环境变量配置和管理
- 简单的命令行聊天客户端
- LLM响应的性能指标分析

### practice02 - 工具调用基础实践

**文件说明**：
- `tool_client.py`：实现基础的工具调用功能，包括简单的工具定义和调用流程
- `prompt02.txt`：系统提示词配置文件

**功能**：
- 工具调用的基础实现
- 简单的工具定义和执行
- 工具调用流程的基本框架

### practice03 - 文件操作和网络访问工具实践

**文件说明**：
- `tool_client.py`：实现文件操作和网络访问工具的客户端
- `prompt03.txt`：系统提示词配置文件

**功能**：
- 文件操作工具：列出目录内容、重命名文件、删除文件、创建文件、读取文件
- 网络访问工具：访问网页并返回内容
- 完整的工具调用流程实现
- 命令行交互界面

### practice04 - 聊天历史管理实践

**文件说明**：
- `tool_client.py`：扩展了聊天历史管理功能的客户端
- `prompt04.txt`：系统提示词配置文件

**功能**：
- 聊天历史搜索工具：搜索历史聊天记录
- 聊天历史总结：自动总结冗长的聊天历史
- 关键信息提取：按照5W规则提取聊天中的关键信息
- 聊天历史长度和轮数的监控

### practice05 - AnythingLLM文档仓库访问实践

**文件说明**：
- `tool_client.py`：扩展了AnythingLLM文档仓库访问功能的客户端
- `prompt05.txt`：系统提示词配置文件

**功能**：
- AnythingLLM文档仓库访问工具：访问文档仓库，查询仓库中的文件和内容
- 使用subprocess模块调用curl命令
- API认证和中文编码处理
- 完善的错误处理机制

## 环境配置

本项目使用`.env`文件管理环境变量，包括：

- `BASE_URL`：LLM API的基础URL
- `MODEL`：使用的LLM模型
- `API_KEY`：LLM API的认证密钥
- `TEMPERATURE`：生成文本的温度参数
- `MAX_TOKENS`：最大生成Token数
- `ANYTHINGLLM_API_KEY`：AnythingLLM的API密钥
- `ANYTHINGLLM_WORKSPACE_SLUG`：AnythingLLM的工作区slug

## 使用方法

1. 配置`.env`文件，填写相应的API密钥和配置参数
2. 进入相应的practice目录，运行`python tool_client.py`或`python chat_client.py`
3. 按照提示输入消息，与AI助手进行交互

## 工具列表

| 工具名称 | 描述 | 所在目录 |
|---------|------|---------|
| `list_directory` | 列出指定目录下的所有文件和目录，包括基本属性 | practice03, practice04, practice05 |
| `rename_file` | 修改指定目录下的文件名称 | practice03, practice04, practice05 |
| `delete_file` | 删除指定目录下的文件 | practice03, practice04, practice05 |
| `create_file` | 在指定目录下创建新文件并写入内容 | practice03, practice04, practice05 |
| `read_file` | 读取指定目录下的文件内容 | practice03, practice04, practice05 |
| `fetch_webpage` | 访问指定URL的网页并返回内容 | practice03, practice04, practice05 |
| `search_chat_history` | 搜索聊天历史记录 | practice04, practice05 |
| `anythingllm_query` | 访问AnythingLLM文档仓库 | practice05 |

## 技术栈

- Python 3.12+
- HTTP/HTTPS客户端
- JSON处理
- 命令行交互
- Subprocess模块
- 环境变量管理

## 实验报告

每个practice目录下都有对应的实验报告，详细记录了实验目的、过程、结果和总结：

- `practice01/practice01实验报告.md`
- `practice02/practice02实验报告.md`
- `practice03/practice03实验报告.md`
- `practice04/practice04实验报告.md`
- `practice05/practice05实验报告.md`

## 总结

本仓库通过一系列实践项目，逐步构建了一个功能丰富的LLM应用，从基础的API调用到复杂的工具调用和文档仓库访问，展示了LLM应用开发的完整流程和技术要点。通过这些实践，我们学习了：

- LLM API的调用方法（流式和非流式）
- 工具调用的设计和实现
- 文件操作和网络访问
- 聊天历史管理和分析
- 外部服务的集成（如AnythingLLM）

这些技术和经验为构建更加智能、功能丰富的LLM应用奠定了基础。