Elementary Functional Algorithms
====

Edition: $\displaystyle e = \sum \limits _{n=0}^{\infty }{\frac {1}{n!}} = 1 + {\frac {1}{1}}+{\frac {1}{1\cdot 2}}+{\frac {1}{1\cdot 2\cdot 3}}+\cdots = 2.718283$

2023/10

This book introduces about elementary functional algorithms and data structures. It includes side-by-side comparison about purely functional realization and their imperative counterpart, with 120 exercises and answers.

<img src="https://user-images.githubusercontent.com/332938/95418499-442e4b00-096a-11eb-81b9-496020aa5f10.jpg" width="400">

Contents
--------

I am adding exercises and answers to the **second edition** from 2023/03 (added 120 answers as of 2023/10). I wrote the first edition from 2009 to 2017, then rewrote from 2020 to 2023. The PDF can be **downloaded** ([EN](https://github.com/liuxinyu95/AlgoXY/files/12855002/algoxy-en.pdf), [中文](https://github.com/liuxinyu95/AlgoXY/files/12855005/algoxy-zh-cn.pdf)). The 1st edition in Chinese ([中文](https://book.douban.com/subject/26931430/)) was published in 2017. I switched my focus to the mathematics of programming from 2018, see ([github](https://github.com/liuxinyu95/unplugged)).


- Preface
- Chapter 1, List;
- Chapter 2, Binary Search Tree;
- Chapter 3, Insertion sort;
- Chapter 4, Red-black tree;
- Chapter 5, AVL tree;
- Chapter 6, Radix tree, Trie and Prefix Tree;
- Chapter 7, B-Trees;
- Chapter 8, Binary Heaps;
- Chapter 9, Selection sort;
- Chapter 10, Binomial heap, Fibonacci heap, and pairing heap;
- Chapter 11, Queue;
- Chapter 12, Sequence;
- Chapter 13, Divide and conquer sort;
- Chapter 14, Search;
- Appendices and answers

Install
--------

You need TeXLive to build the book in PDF format. We use LuaLaTeX, an extended version of TeX.

### Install TeXLive

In Debian/Ubuntu like Linux environment, do **NOT** install the TeXLive through apt-get. Go to TeXLive [official site](https://tug.org/texlive/) to download the setup script.

```bash
$ wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl.zip
$ unzip install-tl.zip
$ cd install-tl
$ sudo ./install-tl -gui text -repository http://mirror.ctan.org/systems/texlive/tlnet
```

In Windows, TeXLive provides a [gui based installer](https://tug.org/texlive/), in Mac OS X, there's a [MacTeX](https://www.tug.org/mactex/).

### Others

You need the GNU make tool, in Debian/Ubuntu like Linux, it can be installed through:

```bash
$ sudo apt-get install build-essential
```

In Windows, you can use WSL or install MSYS. In Mac OS X, please install the developer tool from this command line:

```bash
$ xcode-select --install
```

### Font setting

The default build supports Linux, Mac OS X, and Windows. You can install additional font (like [Noto CJK](https://github.com/notofonts/noto-cjk/)) typesetting (see `prelude.sty`). Some system fonts, e.g. STKaiti, were moved to `/System/Library/AssetsV2/com_apple_MobileAsset_Font7` in Mac OS X from 2022, you need add the path to the local TeXLive configuration:

```bash
sudo tlmgr conf texmf OSFONTDIR /System/Library/AssetsV2/com_apple_MobileAsset_Font7
```

### Build the book PDF

enter the folder contains the book TeX manuscript, run

```bash
$ make
```

This will generate algoxy-en.pdf and algoxy-zh-cn.pdf. If you only need the Chinese version for example, you can run `make cn` instead. Run `make force-cn` or `make force-en` to force build the book.

--

LIU Xinyu
