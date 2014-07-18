# 序言

_Modern Perl_ 形容了世界上最高效的 Perl 程序员的工作方式。他们充分使用了语言的风格。他们对 CPAN 加以利用。他们对书写强大、可维护、可扩展、简洁、高效的代码有着独特的见解和精湛的技巧。当然，你也可以学到这个本领！

Perl 最初作为一个简单的系统管理工具出现在1987年。虽然它起初作为 shell 脚本和 C 编程的一种折衷，但如今它已经成为一个强大的，通用的语言家族。Perl 拥有坚实的实用主义历史和光明的不断发展的未来。

在 Perl 的悠久历史--尤其是19年的 Perl 5--我们对于什么是优秀的 Perl 程序的理解发生了改变。尽管你可以不利用语言提供的任何便利写出高效的程序，但是整个 Perl 社区有着创新、借鉴、增强、精良的观念并且提供给任何愿意学习它们的人们。

## 运行 Modern Perl

来自 [CPAN](https://metacpan.org/pod/CPAN) `Modern::Perl` 模块会让 Perl 警告含糊不清的结构以及书写，别且启用现代 Perl 版本中引入的新的特性。除非特别说明，以下的代码片段：

    #!/usr/bin/env perl

    use Modern::Perl '2013';
    use autodie;

等效于：

    #!/usr/bin/env perl

    use 5.016;      # implies "use strict;"
    use warnings;
    use autodie;
    
有些示例使用了试验性函数比如 `ok()`，`like()`， `is()` [testing](https://metacpan.org/pod/Test::More)，这些程序可遵循以下模式：

    #!/usr/bin/env perl

    use Modern::Perl;
    B<use Test::More;>

    # example code here

    B<done_testing();>
    
当前稳定的 Perl 版本是 Perl 5.18。如果你使用的更早些的版本，对于书中的某些示例你可能需要更改才能运行。本书中的示例能完好运行在 Perl 5.14.0 以及更新的版本上，但是我们推荐使用至少 Perl 5.16。尽管所谓的 “Modern Perl” 指的是 Perl 5.10.1 及以后的版本，但是又很多后来新加的特性是现代开发中必不可少的。

如果你还没有安装 Perl （或者安装的版本过于陈旧），你可以自己安装一个更新的版本。对于 Windows 用户，可以从 http://www.strawberryperl.com 下载 Strawberry Perl 或者从 http://www.activestate.com/activeperl 下载 ActivePerl。其他已经预装 Perl （和 C 编译器以及其他开发工具）的操作系统的用户可以安装 CPAN 模块 `App::perlbrew`。 安装指南参见 https://metacpan.org/pod/App::perlbrew。

`perlbrew` 允许你同时安装管理多个版本的 Perl。这使得你可以在多个版本间自由切换，将 Perl 和 CPAN 安装到你的主目录并且不影响系统自带的 Perl。如果你曾经有过向你的系统管理员请求权限去安装软件的经历，那么你就知道这会简单许多。

# 编者

如果没有很多人的疑问、评论、建议、忠告、知识、鼓励，也就不会有这本书。作者特别感谢：

John SJ Anderson, Peter Aronoff, Lee Aylward, Alex Balhatchet, Nitesh Bezzala, Ævar Arnfjörð Bjarmason, Matthias Bloch, John Bokma, Vasily Chekalkin, Dmitry Chestnykh, E. Choroba, Tom Christiansen, Anneli Cuss, Paulo Custodio, Steve Dickinson, Kurt Edmiston, Felipe, Shlomi Fish, Jeremiah Foster, Mark Fowler, John Gabriele, Nathan Glenn, Kevin Granade, Andrew Grangaard, Bruce Gray, Ask Bjørn Hansen, Tim Heaney, Graeme Hewson, Robert Hicks, Michael Hicks, Michael Hind, Mark Hindess, Yary Hluchan, Daniel Holz, Mike Huffman, Gary H. Jones II, Curtis Jewell, Mohammed Arafat Kamaal, James E Keenan, Kirk Kimmel, Graham Knop, Yuval Kogman, Jan Krynicky, Michael Lang, Jeff Lavallee, Moritz Lenz, Andy Lester, Jean-Baptiste Mazon, Josh McAdams, Gareth McCaughan, John McNamara, Shawn M Moore, Alex Muntada, Carl Mäsak, Chris Niswander, Nelo Onyiah, Chas. Owens, ww from PerlMonks, Jess Robinson, Dave Rolsky, Gabrielle Roth, Grzegorz Rożniecki, Jean-Pierre Rupp, Eduardo Santiago, Andrew Savige, Lorne Schachter, Steve Schulze, Dan Scott, Alex-ander Scott-Johns, Phillip Smith, Christopher E. Stith, Mark A. Stratman, Bryan Summersett, Audrey Tang, Scott Thomson, Ben Tilly, Ruud H. G. van Tol, Sam Vilain, Larry Wall, Lewis Wall, Paul Waring, Colin Wetherbee, Frank Wiegand, Doug Wilson, Sawyer X, David Yingling, Marko Zagozen, Ahmad M. Zawawi, harleypig, hbm, sunnavy.

如仍有错误都是固执的作者的错。




























