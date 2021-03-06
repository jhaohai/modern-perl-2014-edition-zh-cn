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

> 如何阅读文档

> Perl 有许多文档，那该从哪儿开始？

> `perldoc perltoc` 展示了核心文档的内容目录。`perldoc perlfaq` 展示了 Perl 常见问题的内容目录。`perldoc perlop` 和 `perldoc perlsyn` 分别是 Perl 运算符和语法结构的文档。`perldoc perldiag` 揭示了 Perl 的警告消息。`perldoc perlvar` 列出了所有 Perl 的符号变量。略读这些文档会让你对这门语言有个很好的概览。

`perldoc` 工具还有很多别的功能（参见 `perldoc perldoc`）。如果要搜索 Perl FAQ，使用 `-q` 选项外加关键字。比如说，`perldoc -q sort` 返回三个问题：_How do I sort an array by
(anything)?_，_How do I sort a hash (optionally by value instead of key)?_ 以及 _How can I always keep my hash sorted?_。

`-f` 选项显示 Perl 内置方法的文档。`perldoc -f sort` 解释了 `sort` 方法的功能。如果你不知道你想要的方法的名称，可以通过 `perldoc perlfunc` 浏览可用的内置方法列表。

`-v` 选项查找内置变量。比如说，`perldoc -v $PID` 显示当前程序进程号变量的文档。根据你的 shell 的不同，你可能需要给变量做正确的引用。

`-l` 选项会使 `perldoc` 显示文档的 _路径_ 而不是文档的内容。**注意有些模块可能会用单独的 `.pod` 文件而不是在 `.pm` 中**。

`-m` 选项会不加任何修饰的显示整个模块的 _内容_ ，包括代码等。

Perl 使用的文档格式称为 _POD_ ，是 _Plain Old Documentation_ 的缩写。`perldoc perlpod` 解释了 POD 是怎样工作的。其他的 POD 工具包括 `podchecker`，用来检验 POD 文档的结构是否正确，以及 `Pod::Webserver` CPAN 模块，可以通过一个精简 web 服务将本地的 POD 转换成 HTML 显示出来。

## 表达性

Larry Wall 一开始学习语言学，研究人类语言。然后他设计了 Perl。与其他围绕数学符号设计的语言不同，Perl 一开始就考虑到人类如何交流的。因此，你有极大的自由实现你的程序来达到你的要求。你可以编写简单的，直截了当的代码或者将许多的代码片段组合成更大的程序。你可以从多种编码规范中选择，你可以回避或者使用高级的特性。

当其他语言认为只有一种最优的方法解决一个问题时，Perl 允许 _你_ 决定什么是最易读的，最有用的，最吸引人的，或者最有趣的。

Perl 黑客对此有一句口号： _TIMTOWTDI_，读作 “Tim Toady“，或者是 “There's more than one way to do it!”。

尽管这种表达性能让技术精湛的大师创造出出色的程序，但它同时能够让菜鸟写出糟糕的代码。经验和良好的习惯会在你设计你的程序时指引你，但选择永远是你的。表达自己的想法，但记住可读性和可维护性，尤其是为了你后来的人。

学习 Perl 就像学习任何一门口语。你需要学习一些单词，然后将它们组成句子，然后享受简单的对话。精通来自于读和写的锻炼。为了写出良好的代码你无需了解 Perl 所有的细节，但是本章所述的准则对你作为程序员的成长至关重要。

Perl 初学者往往发现某些语法结构很奇怪。这些用法能在有经验的开发者手中被很好的利用，但是如果不喜欢你也可以避免使用他们。

作为 Perl 的另一个设计目标，Perl 极力避免产生另有经验的（Perl）开发者意外的结果。比如说，将两个变量相加（`$first_num + $second_num`）很显然是数值的操作；操作符需要把两个变量当作数值并产生一个数值的结果。无论 `$first_num` 和 `$second_num` 的内容是什么，Perl 需要把它们强制转换成数值。你使用数值操作符意图把它们当作数字处理，Perl 也很乐意这么做。

Perl 专家把这个原则称作 _DWIM_，或者是 _do what I mean_。你也可以说 Perl 遵循着 _最少意外原则_。大概了解 Perl（尤其是上下文）后，你将可能会知道一个不熟悉的 Perl 表达式的意图。

Perl 的表现性能够让新手写出可用的程序而无需理解整个语言。这就是设计！资深的开发者通常把它称作 _baby Perl_。这是一种表示喜爱的称呼，因为每个人都是从新手开始的。通过不断训练和从更有经验的程序员学习，你将会理解使用更强大的语法和技术。你可以用你理解的方式写出简单的代码。不断的练习，最终你会熟练的使用它们。

一个 Perl 资深开发者会用下面的方法把一列数字乘三：
    
    my @tripled = map { $_ * 3 } @numbers;
    
而一个熟练使用 Perl 的人可能会用：

    my @tripled;

    for my $num (@numbers)
    {
        push @tripled, $num * 3;
    }

而新手则会这么做：

    my @tripled;

    for (my $i = 0; $i < scalar @numbers; $i++)
    {
        $tripled[$i] = $numbers[$i] * 3;
    }

每个程序都做相同的事，而每个都在用不同的方法使用 Perl。

当你适应了 Perl，你能让它为你做更多事情。经验上讲，你可以专注于你想做 _什么_ 而不是 _怎样_ 去做。即便如此，Perl 会很乐意和运行 expert perl 一样运行 baby perl。你可以为了清晰，表现性，重用性以及可维护性上设计和改进你的程序，一部分或者整体。通过这种灵活性和实用性，有效的完成眼前的任务比下一年写出纯粹的优美的代码更好。

## 上下文

在口语中，一个单词或短语的意思可能取决于你如何使用它；当前的 _上下文_ 能够帮助弄清含义。比如说，一个不恰当的复数使用“Please give me one hamburgers!”，名词的复数形式与数量不一致，听起来是错误的。还有性别错误的“la gato”，文中写的是女性，而名词是男性。这会让母语使用者笑话。有的单词有两重意思；比如说一只羊是 sheep，而两只羊还是 sheep。

Perl 中的上下文也类似。
