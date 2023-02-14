# ChatToGPT
利用苹果“快捷指令”制作的简易对话应用。

- 支持通过 Siri 对话
- 支持通过 iOS 共享菜单提供话题
- 支持聊天记录转录
- 支持通过聊天记录恢复上一次聊天

https://user-images.githubusercontent.com/12840982/218711133-2940f753-7b9d-4a51-8dae-35a5d16e82d5.mov



## 准备工作

### OpenAI 账号与 API Key

在 [platform.openai.com](https://platform.openai.com) 注册一个体验账号，你将收获 $18 的体验金（本文写于 2023 年 2 月 14 日）。

登录账号之后，打开 [API Key 页面](https://platform.openai.com/account/api-keys)，创建一个新 Key 并及时复制。

### 获取捷径

点击每个指令的链接，并在弹出的「快捷指令」app 中添加它们。

#### 1. 文本转数字指令

https://www.icloud.com/shortcuts/0f05ad8fa7b14b6f86b838e64541d5e6


#### 2. OpenAI 响应数据解析指令

https://www.icloud.com/shortcuts/ec4d93357c8948b5a7b0913fa0dd7399

#### 3. 去除文本开头空行指令

https://www.icloud.com/shortcuts/1501d6813ce34b018fa8a7e35c6207d1

#### 4. 核心指令

在获取这个指令时，需要根据提示，粘贴[之前步骤](https://github.com/EdgarDegas/ChatToGPT/edit/main/README.md#openai-账号与-api-key)获得的 API key。

<img src="https://user-images.githubusercontent.com/12840982/218722332-512c35f0-29b2-4b4b-99f1-6f0fed6a00b4.jpeg" alt="根据提示输入 API Key" style="width:300px;" />

https://www.icloud.com/shortcuts/75c9d736bece4a77b427a630f72ec086


#### 5. 对话指令

这个是你最终将会使用的指令。

若要实现示例视频中的转录到备忘录的功能，可以在获取指令的时候，输入一个你喜欢文件夹名，例如「我和ChatGPT的聊天记录」：

> 你需要亲自去「备忘录」app 中创建名为「我和ChatGPT的聊天记录」的文件夹。

<img src="https://user-images.githubusercontent.com/12840982/218720349-70ebc255-a1be-44ac-aef3-67fb690dc270.PNG" alt="根据提示输入文件夹名" style="width:300px;" />

在使用 Siri 来对话时，需要设置一个结束词来结束对话，否则你只能手动点击屏幕来结束。默认为「再见」，请不要包含任何标点符号：

<img src="https://user-images.githubusercontent.com/12840982/218720211-087d23fc-3d31-4411-a148-603ad6b11ab6.PNG" alt="根据提示输入结束词" style="width:300px;" />

https://www.icloud.com/shortcuts/01c779bec16d4439a57ab64399006c81



## 使用

不要修改前 4 个快捷指令的名称，如果你修改了，可以重新导入。或者，原名称分别为：

1. Number or None
2. ChatGPT v1 Response JSON Resolver
3. Trim Top
4. ChatGPT核心



### 唤醒方式

- 在「快捷指令」app 中，点击「开始聊天」。
- 添加到主屏幕：在「快捷指令」app 中，长按「开始聊天」，点击「详细信息」，点击「添加到主屏幕」。

<img src="https://user-images.githubusercontent.com/12840982/218720745-4c03af47-e489-452e-a11e-60da87969949.jpg" alt="如何添加到主屏幕" style="width:300px;" />

- 对 Siri 说「开始聊天」。这种情况下，如果设置了「备忘录文件夹名」，将会自动打开「备忘录」app。
    - 已知 iOS 16.3 下可以正常使用 Siri，如果无法正常使用可以升级系统。



### 对话

遇到询问「是否允许」的提示时，选择「始终允许」或「允许」。

1. 当提示「我在听。」时，输入或说出你要说的话。
    - 如果说出你设置的「结束词」，对话将立即结束。
2. 等待回应，时间可能持续很久。
    - 如果成功收到回复，可以点击「好」来继续对话，回到第 1 步。
    - 如果失败，将提示你是否重试，点击「好」来重试刚才的对话。

在任一步骤点击「取消」，对话将结束。



### 继续上一次聊天

这个功能需要你配置了「开始聊天」指令的备忘录文件夹名。



如果你在导入时未配置，现在打开「快捷指令」app，长按「开始聊天」，点击「详细信息」，选择顶部的「设置」，点击「自定快捷指令...」，然后根据文本提示填入信息。



在进行过一次对话后，聊天记录将被保存在备忘录的文件夹中。打开备忘录，全选聊天记录，点击「共享...」：

<img src="https://user-images.githubusercontent.com/12840982/218717717-f2e97310-e340-4ef2-b6ed-ba9569066a9d.jpeg" alt="将文本共享给指令" style="width:300px;" />

滚动到弹出的选单的底部，选择「开始聊天」：

<img src="https://user-images.githubusercontent.com/12840982/218717684-da91ff54-aebd-4561-9269-46c2de27b505.jpeg" alt="以共享的文本为基础开始聊天" style="width:300px;" />

接下来的对话将延续这份聊天记录进行。



你也可以用这种方法，选择任意的文本，共享给「开始聊天」快捷指令，然后与它讨论这段文本，比如让它为你翻译成其他语言等。
