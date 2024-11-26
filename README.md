DifyAIA仓库-说明文档
==========
本仓库为B站：bannylon7相关Dify AI实战案例相关源码

BillPic2Web(票据内容识别并将识别的票据内容用HTML页面展示)
---
为B战bannylon7发布的Dify AI实战案例教学视频：[(MAC)BillPic2Web—AI智读票据，它能够实现票据图片的自动解析并生成网页](https://www.bilibili.com/video/BV166DDYLE7n/) 的相关源码。<br><br>
BillPic2Web—AI智读票据，它能够实现票据图片的自动解析并生成网页。该AI应用支持用户上传票据图片并选定票据类型。系统首先校验用户所选类型与模型识别图片所得类型是否一致。若一致，应用将自动识别票据内容，并将其转化为可预览的HTML网页；若不一致，则提示用户确认类型后重试。简而言之，BillPic2Web能快速将票据图片转换成可视化的HTML页面，提升工作效率与便捷性。它集成了票据类型识别、内容提取及HTML生成等功能，旨在为用户提供全面的票据数字化解决方案。

#### 使用指南
1、下载文件夹bBillPic2Web到本地任意目录；<br>
2、在BillPic2Web文件夹上右键单击，选择“服务——新建位于文件夹位置的终端窗口“；<br>
3、在打开的终端窗口中输入执行flask服务命令：`Python invoice.py`<br>
4、运行dify，在dify中导入 “Dify AI 应用：BillPic2Web.yml” DSL文件：在打开的工作流中修改LLM节点模型，以及修改HTTP请求节点的get请求的URL。<br>
![](https://raw.githubusercontent.com/BannyLon/DifyAIA/refs/heads/main/BillPic2Web/1731242789983.jpg)


解读Github项目智能机器人(analysis-Github-project)
---
为B战bannylon7发布的Dify AI实战案例教学视频：[(MAC)使用本地部署的Dify搭建 AI自动总结概括GitHub项目](https://www.bilibili.com/video/BV1eNtse9Epo) 的相关源码。<br><br>
这是一个解读Github项目的工作流，用户输入一个github项目的url，通过HTTP请求获取GitHub项目的README文件，并将README文件转换为纯文本，然后HTTP请求获取GitHub项目的README文件的完整结构，利用大语言模型对GitHub项目进行归纳总结，最后输出。这个工作流帮助用户快速了解Github项目。

#### 使用指南
1、下载analysis-Github-project到任意目录；<br>
2、在analysis-Github-project文件夹上右键单击，选择“服务——新建位于文件夹位置的终端窗口“；<br>
3、在打开的终端窗口中输入执行flask服务命令：`Python readme.py`<br>
4、运行dify，在dify中导入 解读Github项目智能机器人.yml DSL文件：在打开的工作流中修改LLM节点模型，以及修改HTTP请求节点的get请求的URL。<br>

![](https://github.com/BannyLon/DifyAIA/blob/main/analysis-Github-project/readmes/analysis-Github-project.png)

思维导图生成助手(Mindmap-generate-assistant)
---
为B战bannylon7发布的Dify AI实战案例教学视频：[Dify AI 教程：自动生成思维导图](https://www.bilibili.com/video/BV1qnsDeZErX)的相关源码。<br><br>
这是一个功能强大的Dify AI应用，它能够根据用户提供的参考内容，迅速一键生成思维导图。该应用的工作流程高度自动化：首先，通过HTTP请求节点配置一个精密的工作流，这个工作流负责将生成的Markdown内容发送到Flask服务，并将其发布为一个便捷的工具。随后，创建一个Agent应用，这个应用能够智能地通过工作流触发工具，进一步将Markdown内容发送到Flask服务。在Flask服务中，Markdown内容会被精心保存为一个.md文件。更为先进的是，该服务会调用Markmap工具，将Markdown文件巧妙地转化为交互式的HTML思维导图。最终，Flask服务会返回一个包含查看链接的JSON响应，用户只需轻松点击链接，即可直观地查看生成的思维导图文件。

#### 使用指南
1、下载Mindmap-generate-assistant到任意目录；<br>
2、在Mindmap-generate-assistant文件夹上右键单击，选择“服务——新建位于文件夹位置的终端窗口“；<br>
3、在打开的终端窗口中输入执行flask服务命令：`Python markmap.py`<br>
4、运行dify，在dify中导入 `思维导图生成助手mindmap_generator.yml` DSL文件：在打开的工作流中修改LLM节点模型，以及修改HTTP请求节点的get请求的URL。然后发布为工具。<br>
5、再次导入 `思维导图生成助手.yml` DSL文件，在打开的Agent更换模型，同时删除已调用的工具，再重新添加刚发布的工具。然后就可以直接运行操作了。

Dify workflow(Dify精选工作流)
---
Dify workflow将存储我精心整理的所有与学习相关的Dify工作流。我会不定期进行更新，确保你能找到所需的工作流。
| 文件名称 | 文件描述 |文件图示 |
| :-------------: | :----------: | :------------: |
| [RedCanvas.yml](https://www.bilibili.com/video/BV1jTyeYGE8q/) |   一键生成吸引眼球的小红书文案和配图，让您的每篇内容都成为焦点！   |![](./Dify%20workflow/IME/RedCanvas.jpg?raw=true)|
| [Twitter 账号分析助手.yml](https://www.bilibili.com/video/BV1Vw2QY4Ezf/)        |    根据用户提供的Twitter账户ID，利用HTTP请求和外部爬虫工具来抓取该ID的推文内容，并使用先进的LLM（Large Language Model，大型语言模型）技术对抓取到的社交平台数据进行深度分析。最终，我们将基于分析结果，模拟该用户的写作风格，撰写出符合我们要求的推文内容。     |        ![](./Dify%20workflow/IME/Twitter.jpg?raw=true) |
| [知识库图像检索与展示.yml](https://www.bilibili.com/video/BV1zexgeDEMe/)        |    通过知识检索从知识库中检索出带有图片链接的内容，然后借助HTTP请求节点将图片链接显示出来，实现一个直观且吸引人的图文结合客服交互场景，为用户带来更加生动、便捷的沟通体验。     |        ![](./Dify%20workflow/IME/1729836804207.jpg?raw=true) |
| [知识全网搜索.yml](https://www.bilibili.com/video/BV1BhtCeUEye/)        |    根据用户提问，利用Exa.ai搜索引擎搜索相关网页内容，然后对网页内容进行摘要，最后以一种便于阅读的的格式排版输出。妈妈再也不用担心我的学习，想学哪里搜哪里。     |        ![](./Dify%20workflow/IME/1729837233247.jpg?raw=true) |
| [资讯推送应用.yml](https://www.bilibili.com/video/BV1XsxneqE96/)       |    从号称程序员圈的"微博"的 Hacker News 获取最佳的文章资讯，并将整理后的资讯推送到企业微信群中。     |        ![](./Dify%20workflow/IME/1729837393352.jpg?raw=true) |
| [解析网页内容存到知识库.yml](https://www.bilibili.com/video/BV1CkxXeLEnn/)      |    利用Jina Reader从指定URL提取核心内容，借助大语言模型（LLM）将这些内容转化为清晰、易管理的文本内容，最后通过知识库API，将精炼后的文档上传至指定的ID知识库中。这一流程将极大地促进我们未来在构建检索增强生成模型（RAG）方面的工作。     |        ![](./Dify%20workflow/IME/1729837328598.jpg?raw=true) |
| [dify AI 教程：图文智控链.yml](https://www.bilibili.com/video/BV1JiyXYNE2g/)      |    图文智控链是一款基于人工智能技术的智能工作流工具。它能够智能识别用户上传的图片和文档，并根据内容的不同进行灵活处理。无论是纯图片、纯文档还是图文混合的内容，该工作流都能迅速判断并启动相应的处理模式。通过精准的图片解读和文档总结功能，该工作流能够帮助用户快速获取所需信息，提高工作效率。     |        ![](./Dify%20workflow/IME/1729845555795.jpg?raw=true) |
| [Dify AI 教程：ChatWithPaper .yml](https://www.bilibili.com/video/BV1CCSUYrExd/)     |    AI - ChatWithPaper 是由 Dify 开发的学术论文对话助手。它基于预先提供的论文摘要、方法论分析和评估来回答用户关于特定论文的问题。它能像该领域的资深学者一样，与对研究感兴趣的读者进行专业交流。当涉及知识局限性时， AI - ChatWithPaper会及时告知用户。     |        ![](./Dify%20workflow/IME/1730695240344.jpg?raw=true) |
| [Dify AI 应用：Save To Notion.yml](https://www.bilibili.com/video/BV1BaUuYXEde/)     |    复刻“Save to Notion”这个扩展的功能，教大家如何在dify上搭建一个“一键将网页内容保存至Notion”的工作流。     |        ![](./Dify%20workflow/IME/1732612780877.jpg?raw=true) |
| [Dify AI 应用：News Hot List-36氪.yml](https://www.bilibili.com/video/BV1R5U6YvEZB/)     |    一键获取36氪平台的热榜精华文章     |        ![](./Dify%20workflow/IME/1732613122342.jpg?raw=true) |



<br><br><br><br><br><br>


👨‍💼 作者：BannyLon7

💚 微信：banny-pan

🗨 微信公众号：嗯哌

🌍网站: https://www.npie.net
