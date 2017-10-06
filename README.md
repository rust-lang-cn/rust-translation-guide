# Rust 文档翻译指引
>  Rust Translation Guide

本文给出翻译 Rust 官方相关文档的一些建议和具体指导操作，内容由 [rust-lang-cn](https://github.com/rust-lang-cn) 项目组编写，如有不合理或错误的地方，随时欢迎指出纠正，谢谢！

## Rust 官方文档

Rust 语言的基础文档大都列在 https://www.rust-lang.org/en-US/documentation.html 页面上，目前 Rust 官方团队已经将相关文档拆分到不同的仓库上：

- 《Rust 程序设计语言》（The Rust Programming Language）：https://doc.rust-lang.org/book/，对应仓库：https://github.com/rust-lang/book
- 《通过例子学 Rust》（Rust by Example）：https://rustbyexample.com/，对应仓库：https://github.com/rust-lang/rust-by-example
- The Rustonomicon：https://doc.rust-lang.org/nomicon/，对应仓库：https://github.com/rust-lang-nursery/nomicon
- 《Rust 语言参考》（The Rust Reference）：https://doc.rust-lang.org/nightly/reference/，对应仓库：https://github.com/rust-lang-nursery/reference

以上文档优先处理，这些文档都循序渐进翻译成中文文档。还有其他更多官方的文档：

- Cargo 使用指南（The Cargo Guide）：http://doc.crates.io/guide.html
- TOML 语法：https://github.com/toml-lang/toml
- A Rust Cookbook：https://rust-lang-nursery.github.io/rust-cookbook/，对应仓库：https://github.com/rust-lang-nursery/rust-cookbook
- 标准库 API 指南（Standard Library API Reference）：https://doc.rust-lang.org/std/
- Rust 编译错误索引（Rust Compiler Error Index）：https://doc.rust-lang.org/error-index.html
- The Unstable Book：https://doc.rust-lang.org/nightly/unstable-book/

上述文档的源文件有些是放在 [rust](https://github.com/rust-lang/rust) 和 [cargo](https://github.com/rust-lang/cargo) 的仓库的子目录中：https://github.com/rust-lang/rust/tree/master/src/doclhttps://github.com/rust-lang/cargo/tree/master/src/doc 和 https://github.com/rust-lang/cargo/tree/master/src/doc。

另外除了 `README.md` 文件外，还可以创建 `CONTRIBUTING.md` 和 `CONTRIBUTOR.md` 文件，前者是介绍如何参与项目的指南文件，后者可以列出参与项目的贡献者名单。这两份文件上，可以保留原文件基础上，再加上如何翻译的介绍和翻译者等信息。

[rust-lang-cn](https://github.com/rust-lang-cn) 项目组已经翻译好的 [《通过例子学 Rust》](https://github.com/rust-lang-cn/rust-by-example-cn)就是按照这些原则进行的。

## 总体建议

对于官方文档的翻译，我们建议中文版的仓库的目录结构保持一致，原则上官方原仓库的每一个更新，中文版都应该跟随着更新，比如 `README.md` 文件，以及配套的编译文档的工具都要随着官方英文文档更新而同步更新。

还有授权协议也和官方文档保持一致，Rust 官方对项目的授权大都是双协议（Apache 和 MIT协议）授权，而且让使用者自由从这两个协议中任选一个协议进行重新授权。所以建议文档的中文翻译仓库采取和官方相同的授权方式。

`README.md` 说明文件尽可能和官方同步，也可加上中文额外的内容。官方的文档 `README.md` 写的一般会比较详尽，包括 `git clone` 项目到文档项目的编译到最终的预览方式都给出详尽说明。中文的翻译项目同样建议保持一样的内容，让读者 `clone` 整个中文的项目也可以按照指引运行起来。

## 文字排版

Rust 的相关文档主要以网页的形式呈现出来，为了让翻译后文档规范且易于阅读，这里也给出一定排版规则（此处列出常见且重要的几点）：

- 汉字，字母，数字等之间以一个空格隔开
- 英文专有词汇注意大小写，如 Rust 不应该写成 rust 或 RUST
- 表示强调：
  - 汉字中的强调使用加粗，不应该斜体，在 `Markdown` 中使用 `**` 将内容包含起来，如：`**语言**` 效果为 **语言**
  - 英文中使用斜体，在 `Markdown` 中使用 `*` 将内容包含起来，如：*Rust* 效果为 *Rust*
- 翻译文档中主要使用中文标点符号，中文符号应遵循国家符号标准，在保持英文的内容上，使用英文标点符号

更多排版注意内容可参考[《中文排版指南》](https://github.com/aakloxu/chinese-copywriting-guidelines)。

## 语句表达

- 忠于英文原文，不增删内容，若英文原文本身有误，向原文提交错误修改
- 翻译后内容注意语句通顺，符合中文语言习惯，比如英文中特别喜欢用 “You” 来承上启下，但中文不一定出现 “你” 这个人称（可考虑去掉人称代词）
- 对专有名词或 Rust 术语，建议在翻译中文词汇后面加上英文词汇，用小括号括起来
- 对英文表述暂时无法翻译清晰的语句，建议在括号后面加上原英文句子。

## 统一翻译术语和固定用语

文档在翻译过程中，有些词汇或短语可能会反复遇到，有一些是英语的固有的短语或常见表述，在翻译成中文时，应该在文章中保持一致，比如：

- see also：参见，参考
- up to：取决于

此类内容后续会不断整理更新。

除了固有短语外，还有一类是和 Rust 或计算机相关的科技术语，在翻译过程中应使用正确的术语，参见[《Rust 语言术语中英文对照表》](https://github.com/rust-lang-cn/english-chinese-glossary-of-rust/blob/master/rust-glossary.md)。

## 翻译流程

TODO...

## 有关参考

- 维基百科: 科技条目翻译指引 http://zh.wikipedia.org/wiki/Wikipedia:%E7%A7%91%E6%8A%80%E6%9D%A1%E7%9B%AE%E7%BF%BB%E8%AF%91%E6%8C%87%E5%BC%95

## 授权协议
[![CC0](https://licensebuttons.net/p/zero/1.0/80x15.png)](https://creativecommons.org/publicdomain/zero/1.0/) Rust 文档翻译指引属于公有领域作品。
