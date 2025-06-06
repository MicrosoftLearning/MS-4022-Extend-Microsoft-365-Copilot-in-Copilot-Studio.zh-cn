---
lab:
  title: 2.1：创建提示操作
---

# 创建提示操作

在本练习中，你将创建提示操作、在 Copilot Studio 中测试提示，并在 Copilot 代理中测试提示。 你将创建一个提示操作，来帮助用户将原始想法转化为遵循特定格式和指南的条理清晰的营销推介。

完成此练习大约需要 15 分钟****。

## 在 Copilot Studio 中创建提示操作

1. 通过导航到位于 `https://copilotstudio.microsoft.com` 的 [Copilot Studio](https://copilotstudio.microsoft.com)，在 Web 浏览器中打开 Copilot Studio。
1. 从左侧导航窗格中选择“**库**”。
1. 选择“**新增**”，然后选择“**提示**”。 此时会打开“**添加提示操作**”向导。
1. 在“**操作名称**”字段中，输入 `Create a Contoso Marketing Pitch`。
1. 在“**描述**”字段中，输入 `Create a marketing pitch that follows Contoso guidelines`，然后选择“**下一步**”。 你将转到“**创建提示**”页面。
1. 在“**说明**”文本框中，输入 `Create a marketing pitch for a product based on a `。
1. 将光标置于输入的句子末尾，然后选择“**添加内容**”
1. 选择“文本”。
1. 在“名称”字段中，输入 `draft`。
1. 在“**示例数据**”字段中，输入 `The Mighty Mechanical Pencil is new, exciting, and useful. It's not only the first of its kind pencil, but it's fun to use.`，然后选择“**关闭**”。

    ![Copilot Studio 中提示生成器 UI 的屏幕截图，其中显示了名称配置为“draft”的输入变量。](../Media/prompt-action-input.png)

## 测试并优化提示

1. 在说明框上方选择“**测试**”，以使用提供的示例数据测试提示。
1. 查看测试运行的输出。

我们来优化提示，以创建结构化程度更高且更加一致的输出。

1. 在“**说明**”文本框中，将以下内容添加到现有说明中以修改提示：

    ```The pitch should follow the following Contoso guidelines:
       - Start with a brief hook
       - Describe unique value proposition
       - End with a call-to-action
       - Use an exciting and influential tone
    ```

1. 再次选择“**测试**”以重新测试提示。
1. 请注意响应的不同之处。
1. 选择“保存”。

## 配置和发布操作

1. 在“**选择操作参数**”页上，提供 `draft` 输入变量的以下**描述**：`initial draft of the marketing pitch`。
1. 提供 `text` 输出变量的以下**描述**：`Final marketing pitch that adheres to Contoso guidelines`。
1. 选择**下一步**。
1. 确保已正确输入详细信息，然后选择“**发布**”。
1. 保存并发布操作时，请稍等片刻。
1. 你的操作现已在库中提供。 选择“保存并关闭”。

   > **备注**：新的提示操作可能需要几分钟或更长时间才能显示在代理的“**添加操作**”页的“**特别推荐**”或“**库**”部分中。

## （可选）向代理添加提示操作

如果已完成上一实验室并创建了声明性代理，则可以将此操作添加到代理，并更新代理的说明以引用该操作。

### 添加操作

1. 从**库**中选择要向其添加操作的声明性代理。
1. 在“**详细信息**”部分，选择“**编辑**”。
1. 在“**说明**”文本框中，将以下内容添加到现有说明文本：`Use the Contoso Marketing Pitch action to help marketing stakeholders craft pitches for products based on their draft ideas.`
1. 在“**操作**”下的“代理详细信息”页上，选择“**添加操作**”。
1. 从“**添加操作**”模式窗口的“**特别推荐**”或**库**”部分，选择“**Contoso 营销推介**”。
1. 在操作页上，确保“**名称**”为 `Create a Contoso Marketing Pitch`
1. 确保“**描述**”为 `Create a marketing pitch that follows the Contoso guidelines`。
1. 选择**添加操作**。 这可能需要一小段时间。 该操作将添加到“**操作**”下代理可用的操作列表中。

### 配置操作

1. 从代理可用的操作中选择 `Contoso Marketing Pitch` 操作。 你将转至用于配置操作的属性和设置的页面。
1. 确认“**操作名称**”已设置为 `Create a new Contoso marketing pitch`。
1. 在操作的顶部导航栏中选择“**输入**”。
1. 在“**其他输入**”下，选择“**添加**”。
1. 选择 **Draft** 变量。 此时会显示一个窗体。
1. 确保“**代理将如何填充此输入**”字段设置为“**动态填充最佳选项（默认值）**”。
1. 在“显示名称”字段中输入 `Initial draft`。****
1. 确保“**标识为**”字段设置为“**用户的整个响应**”
1. 在窗口右上方选择“**保存**”。

## （可选）在 Copilot Studio 中测试提示操作。

接下来，使用 Copilot Studio 中的操作测试代理。

1. 在 Copilot Studio 中代理概述页面的“**测试代理**”窗格中，选择“**刷新**”按钮以刷新测试窗格，并加载代理的最新更改。
1. 在测试对话的文本框中，输入 `Create a Contoso marketing pitch based on the following draft: "Bouncy ball is the hottest product on the market for both youth and adults. It's durable and the largest of its kind."`，然后发送消息。
1. 查看响应，并注意代理遵循你在自定义提示操作说明中提供的指导。

你已完成练习并验证了提示操作的功能。
