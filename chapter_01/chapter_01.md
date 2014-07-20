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
    
第一个例子显示了`List::Util`模块内嵌的文档。第二个例子显示了一个纯文档文件，在这个例子里是核心文档的目录表。第三个例子显示了一个 CPAN 发行版 [moose](https://metacpan.org/release/Moose) 的内置的纯文档文件。