# 豆包文章生成工具 ai_writer

# 一、项目适用场景
大批量有相同格式且要求不高的文字材料生成（例如自媒体文案创作）

# 二、项目亮点
## 1.文章生成速度快。
经测试，200篇6000中文字符的长文章只需要150秒，平均1s不到。
因为使用了异步调用，理论上来说只要网络稳定，本地硬件性能允许，无论生成200篇还是2000篇，其总生成时间都是以生成时间最长的那一篇为准。 
也就是说，时间复杂度是 O(1) 而不是 O(n)。

## 2.泛化性强，通过变换提示词就可以稳定生成不同领域、不同风格的文章。
有一个专门的文件夹./prompts ，可以存储多种场景和风格的提示词，随时变化场景，灵活使用

## 3.可以生成长文章，文章深度和内容丰富度大大提高。
事实上，项目中生成一次文章，其实调用了3-5次大模型对话，每次对话生成一个段落，最后再拼起来。
突破了大模型单次对话最多输出4096个字符的限制。

# 使用方法和运作原理
点击标题左侧链接标志查看流程图

![doubao_writer](https://github.com/user-attachments/assets/a4139bd5-7e82-4493-a78d-0d5c7c8856fb)