# 文件说明

* [czhx1-periodictable.tex](czhx1-periodictable.tex): 生成元素周期表的 TeX 代码（**要求 TexLive 2025 版本**）
* [czhx1-periodictable.pdf](czhx1-periodictable.pdf): 由 [czhx1-periodictable.tex](czhx1-periodictable.tex) 生成的 PDF 文件。
* [czhx1-periodictable.png](czhx1-periodictable.png): 通过 [ImageMagick](https://imagemagick.org/index.php) 将 [czhx1-periodictable.pdf](czhx1-periodictable.pdf) 转换成的 PNG 文件。

转换命令：

```sh
convert -density 300 czhx1-periodictable.pdf czhx1-periodictable.png
```

# 关于字体

由于元素周期表的第 104 ~ 118 号元素，常见的字体大都不包含这些字。

|||||||||||||||||
|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|:--|
| 元素序号 | 104 | 105 | 106 | 107 | 108 | 109 | 110 | 111 | 112 | 113 | 114 | 115 | 116 | 117 |118 |
| 元素符号 | Rf  | Db  | Sg  | Bh  | Hs  | Mt  | Ds  | Rg  | Cn  | Nh  | Fl  | Mc  | Lv  | Ts  | Og  |
| 元素名称 | 𬬻  | 𬭊  | 𬭳  | 𬭛  | 𬭶  | 鿏  | 𫟼  | 𬬭  | 鿔  | 鿭  | 𫓧  | 镆  | 𫟷  | 鿬  | 鿫

> 可在 Latex 文档中，直接使用 “𬬻𬭊𬭳𬭛𬭶鿏𫟼𬬭鿔鿭𫓧镆𫟷鿬鿫” 进行测试。

所以将 “元素周期表” 制作成一个 PNG 图片，这样，在编译及阅读《初中化学》时，就不用再考虑各种字体的问题。

除了使用微软的 `SimSun` 字体外，还可以使用小米的 [MiSans](https://hyperos.mi.com/font/zh/download/) 或 [BabelStone Han](https://www.babelstone.co.uk/Fonts/Han.html) 字体。在 `czhx1-periodictable.tex` 针对这几种字体都提供了相应的代码。

注意：

1. `SimSun` 和 `BabelStone Han` 字体**不能免费商用**，而 `MiSans` 可以。
2. 在 Windows 下安装字体时，要选择 “为所有用户安装”，**不能选** “安装”。


# 关于背景色

直接使用 `\pgfPT` 生成的元素表，不同类型的元素有着不同的背景色。在使用电脑查看 PDF 文件时，有助于直观的了解元素分类。

但是，当使用普通的黑白打印机打印时，不少元素的背景色太深，纸件不清晰。这时，可以考虑通过 `csSolid` 生成没有颜色（背景是白色）的元素表。

详见 [czhx1-periodictable.tex](czhx1-periodictable.tex)。
