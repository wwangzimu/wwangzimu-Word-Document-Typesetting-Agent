一种基于微调训练的智能WORD文档和Latex论文格式化工具。

功能:
文本层级识别: 该工具基于20W token上下文窗口的模型，能够智能识别文本的层级
格式转换: 通过微调训练，该工具能够精准识别WORD和Latex的样式，并调用API自动进行格式修改。
便捷操作: 用户只需提供文本内容和目标格式模板，即可快速生成符合要求的文档。
应用场景: 论文写作、发文审校、自动化办公等领域
  论文写作: 帮助学生和科研人员快速完成论文初稿的写作，并自动生成符合学术规范的格式。
  发文审校: 协助编辑和审稿人检查论文格式，提高审稿效率。
  自动化办公: 自动生成各种格式的文档，如报告、合同、信函等，提高工作效率。
数据集：预计使用开源的论文数据集，使用工具将Latex格式分割成模板和内容两个部分，然后重新构造训练数据集，预计使用2W篇论文
项目分三期开发
1期：
实现对目录、多级标题、正文、换行符等的字体样式修改（非文本生成式比如直接生成markdown一类代码），上下文限制在4K或者8K以内。形成初步的DEMO，通过自行构建数据集微调训练，增强对非结构化的目录、多级标题、正文的识别能力和fuctioncalling，实现一个可以类人修改word思考和操作形态的multi-AGENT应用
目前需要做的是:
1.产品形态细节确定
2.技术路线预研与定型
3.数据集构建训练
2期：
在1期的基础上、增强数据集，重新训练。更换更大尺寸的模型与更长上下文窗口，实现对更长文本识别，对上下划线、脚注、引用等更多类型的复杂文档结构进行优化，会针对性对论文和部分模板进行进一步的优化。
3期：
打通WORD和WPS，作为插件，支持WORD和WPS的模板调用修改。
