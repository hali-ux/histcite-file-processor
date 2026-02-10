# histcite-file-processor

你好！👋  
这是一个小巧实用的 Python 小工具，帮助你把从 Web of Science 导出的 textplain 文本“清洗/重排”为 HistCite 能识别的格式，方便直接导入 HistCite 做引文分析或学术计量学研究。

为什么会有这个工具？
- Web of Science 的 textplain 导出与 HistCite 期望的字段顺序和部分标签不完全一致，本工具会自动：
  - 去掉 HistCite 不支持的字段；
  - 补全 HistCite 需要但缺失的标签（用占位文字标注）；
  - 按 HistCite 常用的字段顺序重排记录；
  - 最后以 Windows ANSI (mbcs) 编码保存，便于在 Windows 上的 HistCite 中打开。

用起来很简单（快速上手）
1. 把要处理的 .txt 文件放到你在脚本中指定的 input 文件夹。  
2. 修改脚本顶部的 input_folder / output_folder 路径为你的实际路径。  
3. 在命令行运行脚本：
   - python "textplain清洗主程序.py"
4. 输出会生成 savedrecs1.txt、savedrecs2.txt …（HistCite 能识别的命名），保存在你设定的 output 文件夹。

注意事项（常见问题）
- 脚本默认把一些字段（如 D3、DA、CL、BN、RI、OI）移除，因为这些标签不是 HistCite 支持的。  
- 若你的 HistCite 版本或导出格式与脚本假设略有不同，欢迎把样例发给我，我们可以一起改进。  
- 脚本会把输出保存为 ANSI（mbcs），这是为了兼容 Windows 上的 HistCite；如果你需要 UTF-8 等别的编码，可以按需修改脚本最后的 open(...) 中的 encoding 参数。

想改进/反馈/贡献？
非常欢迎！无论是兼容性问题、功能建议（比如支持批量配置、GUI、把输出转 CSV），还是直接的代码贡献，都很欢迎你打开 issue 或发 PR。

联系我
- 邮箱（作者留的联系方式）：wsw123467w123467@outlook.com

如果觉得这个小工具对你有用，别忘了给个 ⭐，也可以把你遇到的问题/样例发给我，我们一起优化～谢谢！🙂