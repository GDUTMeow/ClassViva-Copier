# ClassViva-Copier

添加一个按钮，点击后复制 Classviva 的题目为 HTML 代码，便于使用 AI 进行题目的分析及解答

- GreasyFork: https://greasyfork.org/zh-CN/scripts/539284-%E5%A4%8D%E5%88%B6-classviva-%E7%9A%84%E9%A2%98%E7%9B%AE%E4%B8%BA-html-%E4%BB%A3%E7%A0%81
- Github: https://github.com/GDUTMeow/ClassViva-Copier/raw/refs/heads/master/ClassViva-Copier.user.js

![](https://cdn.jsdelivr.net/gh/GDUTMeow/ClassViva-Copier/img/msedge_eoz8WVc93Y.png)

> [!tip]
>
> 建议使用 Prompt 如下（记得换掉里面的那些说明的地方）
> ```
> 我正在网上学习（科目，例如高等数学），并完成有关的练习题，但是这个题目没有给我思路和答案，我没法验证我做的是否正确，我现在把题目的 HTML 发给你，请你告诉我这题怎么做，以及他的答案是什么
> 我的第一题是：（放HTML）
> ```

## 为什么要给 AI HTML 代码，而不是截图/直接复制题目

我也曾经是截图/复制题目的，但是他们都有各自的问题

首先，直接复制题目的情况下，复制出来的结果很可能会格式错乱，而且很难阅读，AI识别的时候也会识别出错，所以直接复制是我最不考虑的

然后是截图，不得不说，截图是一个好办法（相较于直接复制而言），它至少保留了题目的完整结构，但是 AI 识图会出错，对于一堆元素挤在一起的情况（积分、求和、开根等），它会识别的有问题，这就导致我得让 AI 先重复一遍题目，看看它是否识别正确后，再去看它给我的答案

而直接给 HTML 就没有这种问题，AI 能够正确从 HTML 的结构中解析出式子原本的样子和题目的要求，虽然复制的内容多了点，而且每次要从 Dev tool 扒代码很麻烦 ，但是是最准确的

所以我就做了这样一个油猴脚本，让我不用开 Dev tool 直接去扒代码，相当于简化操作了

## AI 建议

|       名称       |     公司      |                     网址                     |                            优缺点                            |
| :--------------: | :-----------: | :------------------------------------------: | :----------------------------------------------------------: |
|     Deepseek     |   深度求索    |          https://chat.deepseek.com           | 优点：深度思考很有用，基本不会出错；可以 Google 登录（要挂梯子，或者用对应[油猴脚本](https://github.com/GamerNoTitle/TemperMonkeyScript)）<br />缺点：太慢了！！！容易服务器繁忙 |
|     腾讯元宝     |     腾讯      |         https://yuanbao.tencent.com          | 优点：Deepseek有的优点它全有<br />缺点：必须登录（微信/QQ），输入长度短（容易输入不完整题） |
|      Gemini      |    Google     |     https://gemini.google.com/?hl=zh-cn      | 优点：够快，如果要写论文还有学术研究模式<br />缺点：用量有限，要梯子 |
| Google AI Studio |    Google     | https://aistudio.google.com/prompts/new_chat | 优点：够快，而且永久免费，有最新的 Gemini 模型<br />缺点：仅限部分地区，要挂梯子 |
|     ChatGPT      |    OpenAI     |             https://chatgpt.com/             | 优点：真的有吗？<br />缺点：要挂梯子，用量有限，慢，容易封号，要非大陆手机号验证 |
|      Claude      | Anthropic PBC |              https://claude.ai               | 优点：够快<br />缺点：要挂梯子，用量有限，要非大陆手机号验证 |
|       Grok       |       X       |              https://grok.com/               | 优点：够快<br />缺点：要挂梯子，思考模式用量有限，要非大陆手机号验证 |

就我个人来说，推荐用 Google AI Studio，就它给的最多了，并且够用，够快