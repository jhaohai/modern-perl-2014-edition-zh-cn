# Perl 哲学

Perl 将事情做好--它灵活，宽松，可扩展。能干的程序员每天都在用它解决任何事情：从一行一次性的自动操作到长时间、多人协作的大项目。

Perl 是实用主义的。一切由你决定。你决定如何解决你的问题，Perl 将按照你的意思去执行。

Perl 和你一起成长。在接下来的时间里，你会学习如何写出正确的，有用的程序--你将会懂得这个语言是_如何_工作，_为什么_这么工作。Modern Perl 利用这些知识，结合整个 Perl 社区的经验来帮助你写出可运行的，可维护的代码。

首先，你需要了解如果学习更多。

## Perldoc

Perl 有着文档的文化传统。`perldoc`工具是完整的 Perl 安装的一部分。但是某些 Unix-like 系统会要求你安装额外的包，比如 Debian 或者 Ubuntu GNU/Linux 的`perl-doc`。`perldoc`命令行工具会现实每个安装在系统中的 Perl 模块的文档--无论是核心模块还是从 Perl 档案库（CPAN）安装的模块--以及上千页的 Perl 核心文档。

> http://perldoc.perl.org/ 上有最近版本的 Perl 文档。
> http://search.cpan.org/ 和 http://metacpan.org/ 上的 CPAN 索引提供了所有 CPAN 模块的文档。
> 其他的发行版，比如 ActivePerl 和 Strawberry Perl 提供了本地 HTML 格式的文档。

使用`perldoc`阅读模块的文档或者核心文档。

    perldoc List::Util
    perldoc perltoc
    perldoc Moose::Manual
    
第一个例子显示了`List::Util`模块内嵌的文档。第二个例子显示了一个纯文档文件，在这个例子里是核心文档的目录表。第三个例子显示了一个 CPAN 发行版 [moose](https://metacpan.org/release/Moose) 的内置的纯文档文件。`perldoc`隐藏了这些细节，读取诸如 `Data::Dumper` 核心库中的文档与从 CPAN 中安装的是没有区别的。这种高度的一致性会让你受益--Perl 文化非常重视文档以至于那些外部的库都仿照语言核心文档的模式。

标准的文档模板包含了模块的描述，使用的说明案例,以及详细的模块和其接口的说明。尽管文档的数量因作者而异，但是文档格式都高度的一致。

> 小贴士：如何阅读文档
> Perl 有许多文档，那该从哪儿开始？
> `perldoc perltoc` 展示了核心文档的内容目录。`perldoc perlfaq` 展示了 Perl 常见问题的内容目录。`perldoc perlop` 和 `perldoc perlsyn` 分别是 Perl 运算符和语法结构的文档。`perldoc perldiag` 揭示了 Perl 的警告消息。`perldoc perlvar` 列出了所有 Perl 的符号变量。略读这些文档会让你对这门语言有个很好的概览。

`perldoc` 工具还有很多别的功能（参见 `perldoc perldoc`）。如果要搜索 Perl FAQ，使用 `-q` 选项外加关键字。比如说，`perldoc -q sort` 返回三个问题：_How do I sort an array by
(anything)?_，_How do I sort a hash (optionally by value instead of key)?_ 以及 _How can I always keep my hash sorted?_。

`-f` 选项显示 Perl 内置方法的文档。`perldoc -f sort` 解释了 `sort` 方法的功能。如果你不知道你想要的方法的名称，可以通过 `perldoc perlfunc` 浏览可用的内置方法列表。

`-v` 选项查找内置变量。比如说，`perldoc -v $PID` 显示当前程序进程号变量的文档。根据你的 shell 的不同，你可能需要给变量做正确的引用。

`-l` 选项会使 `perldoc` 显示文档的 _路径_ 而不是文档的内容。**注意有些模块可能会用单独的 `.pod` 文件而不是在 `.pm` 中**。
