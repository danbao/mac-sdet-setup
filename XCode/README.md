# XCode

从 App store 或苹果开发者网站安装 [Xcode](https://developer.apple.com/xcode/) 。

紧接着，安装 Xcode command line tools，运行：

```bash
  xcode-select --install
```

运行命令后，按照指引，你将完成 Xcode command line tools 安装。

---
`注`:

如果你不是一名 iOS 或 OS X 开发者，可以跳过安装 XCode 的过程，直接安装  Xcode command line tools 。安装完成后，你将可以直接在 terminal 中使用主要的命令，比如：`make, GCC, clang, perl, svn, git, size, strip, strings, libtool, cpp` 等等。

如果你想了解 Xcode command line tools 包含多少可用的命令，可以到 `/Library/Developer/CommandLineTools/usr/bin` 查看。以下为其中的命令列表：

```bash
  $ ls -la
  total 216632
  drwxr-xr-x  116 root  admin      3712 Nov 13 12:35 .
  drwxr-xr-x    7 root  admin       224 Oct 20 09:19 ..
  -rwxr-xr-x    1 root  admin     22816 Oct 20 09:24 BuildStrings
  -rwxr-xr-x    1 root  admin     29312 Oct 20 09:24 CpMac
  -rwxr-xr-x    1 root  admin    105488 Oct 20 09:24 DeRez
  -rwxr-xr-x    1 root  admin     18512 Oct 20 09:23 GetFileInfo
  -rwxr-xr-x    1 root  admin     62960 Oct 20 09:24 MergePef
  -rwxr-xr-x    1 root  admin     23008 Oct 20 09:23 MvMac
  -rwxr-xr-x    1 root  admin     24432 Oct 20 09:23 ResMerger
  -rwxr-xr-x    1 root  admin    111408 Oct 20 09:24 Rez
  -rwxr-xr-x    1 root  admin     40400 Oct 20 09:24 RezDet
  -rwxr-xr-x    1 root  admin     22864 Oct 20 09:24 RezWack
  -rwxr-xr-x    1 root  admin     22896 Oct 20 09:23 SetFile
  -rwxr-xr-x    1 root  admin     23760 Oct 20 09:24 SplitForks
  -rwxr-xr-x    1 root  admin     22832 Oct 20 09:24 UnRezWack
  -rwxr-xr-x    1 root  admin     33920 Oct 20 09:23 ar
  -rwxr-xr-x    1 root  admin     28000 Oct 20 09:24 as
  -rwxr-xr-x    1 root  admin     18176 Oct 20 09:24 asa
  -rwxr-xr-x    1 root  admin    212208 Oct 20 09:24 bison
  -rwxr-xr-x    1 root  admin    150048 Oct 20 09:23 bitcode_strip
  lrwxr-xr-x    1 root  admin         5 Nov 13 12:35 c++ -> clang
  -rwxr-xr-x    1 root  admin     23152 Oct 20 09:23 c89
  -rwxr-xr-x    1 root  admin     23248 Oct 20 09:24 c99
  lrwxr-xr-x    1 root  admin         5 Nov 13 12:35 cc -> clang
  -rwxr-xr-x    1 root  admin  78335840 Oct 20 09:24 clang
  lrwxr-xr-x    1 root  admin         5 Nov 13 12:35 clang++ -> clang
  -rwxr-xr-x    1 root  admin    120064 Oct 20 09:23 cmpdylib
  -rwxr-xr-x    1 root  admin    145872 Oct 20 09:24 codesign_allocate
  lrwxr-xr-x    1 root  admin        17 Nov 13 12:35 codesign_allocate-p -> codesign_allocate
  -rwxr-xr-x    1 root  admin      3344 Sep 26 06:40 cpp
  -rwxr-xr-x    1 root  admin     27712 Oct 20 09:24 ctags
  -rwxr-xr-x    1 root  admin    145824 Oct 20 09:24 ctf_insert
  lrwxr-xr-x    1 root  admin        13 Nov 13 12:35 dsymutil -> llvm-dsymutil
  -rwxr-xr-x    1 root  admin   1006032 Oct 20 09:23 dwarfdump
  -rwxr-xr-x    1 root  admin    193040 Oct 20 09:24 dyldinfo
  -rwxr-xr-x    1 root  admin    569056 Oct 20 09:23 flex
  -rwxr-xr-x    1 root  admin    569056 Oct 20 09:24 flex++
  lrwxr-xr-x    1 root  admin         3 Nov 13 12:35 g++ -> gcc
  -rwxr-xr-x    1 root  admin    103188 Sep 26 09:01 gatherheaderdoc
  -rwxr-xr-x    1 root  admin     18672 Oct 20 09:23 gcc
  lrwxr-xr-x    1 root  admin         8 Nov 13 12:35 gcov -> llvm-cov
  -rwxr-xr-x    1 root  admin   2128288 Oct 20 09:24 git
  lrwxr-xr-x    1 root  admin         3 Nov 13 12:35 git-receive-pack -> git
  -rwxr-xr-x    1 root  admin   1196640 Oct 20 09:24 git-shell
  lrwxr-xr-x    1 root  admin         3 Nov 13 12:35 git-upload-archive -> git
  -rwxr-xr-x    1 root  admin   1206048 Oct 20 09:24 git-upload-pack
  -rwxr-xr-x    1 root  admin    142336 Oct 20 09:24 gm4
  -rwxr-xr-x    1 root  admin    165152 Oct 20 09:24 gnumake
  -rwxr-xr-x    1 root  admin     90960 Oct 20 09:24 gperf
  -rwxr-xr-x    1 root  admin     24384 Oct 20 09:24 hdxml2manxml
  -rwxr-xr-x    1 root  admin    162025 Sep 26 09:01 headerdoc2html
  -rwxr-xr-x    1 root  admin     65520 Oct 20 09:24 indent
  -rwxr-xr-x    1 root  admin    136784 Oct 20 09:24 install_name_tool
  -rwxr-xr-x    1 root  admin   2165904 Oct 20 09:23 ld
  -rwxr-xr-x    1 root  admin       230 Sep 26 08:51 lex
  -rwxr-xr-x    1 root  admin    154592 Oct 20 09:24 libtool
  -rwxr-xr-x    1 root  admin     66000 Oct 20 09:24 lipo
  -rwxr-xr-x    1 root  admin     67840 Oct 20 09:24 lldb
  -rwxr-xr-x    1 root  admin   3305040 Oct 20 09:24 llvm-cov
  -rwxr-xr-x    1 root  admin  29665296 Oct 20 09:24 llvm-dsymutil
  -rwxr-xr-x    1 root  admin  10548768 Oct 20 09:24 llvm-nm
  -rwxr-xr-x    1 root  admin  11871088 Oct 20 09:23 llvm-objdump
  -rwxr-xr-x    1 root  admin     32672 Oct 20 09:24 llvm-otool
  -rwxr-xr-x    1 root  admin   1264256 Oct 20 09:24 llvm-profdata
  -rwxr-xr-x    1 root  admin   2857264 Oct 20 09:24 llvm-size
  -rwxr-xr-x    1 root  admin      3567 Sep 26 08:55 lorder
  -rwxr-xr-x    1 root  admin    142336 Oct 20 09:24 m4
  -rwxr-xr-x    1 root  admin    165152 Oct 20 09:24 make
  -rwxr-xr-x    1 root  admin      7604 Sep 26 08:54 mig
  lrwxr-xr-x    1 root  admin         7 Nov 13 12:35 nm -> llvm-nm
  -rwxr-xr-x    1 root  admin    132896 Oct 20 09:24 nm-classic
  -rwxr-xr-x    1 root  admin    162720 Oct 20 09:23 nmedit
  lrwxr-xr-x    1 root  admin        12 Nov 13 12:35 objdump -> llvm-objdump
  lrwxr-xr-x    1 root  admin        10 Nov 13 12:35 otool -> llvm-otool
  -rwxr-xr-x    1 root  admin    648720 Oct 20 09:24 otool-classic
  -rwxr-xr-x    1 root  admin    132784 Oct 20 09:24 pagestuff
  -rwxr-xr-x    1 root  admin     23344 Oct 20 09:23 projectInfo
  lrwxr-xr-x    1 root  admin         7 Nov 13 12:35 ranlib -> libtool
  -rwxr-xr-x    1 root  admin     59328 Oct 20 09:23 rebase
  -rwxr-xr-x    1 root  admin    204960 Oct 20 09:24 redo_prebinding
  -rwxr-xr-x    1 root  admin     62464 Oct 20 09:23 resolveLinks
  -rwxr-xr-x    1 root  admin     73664 Oct 20 09:24 rpcgen
  -rwxr-xr-x    1 root  admin     48864 Oct 20 09:23 segedit
  lrwxr-xr-x    1 root  admin         9 Nov 13 12:35 size -> llvm-size
  -rwxr-xr-x    1 root  admin    120080 Oct 20 09:23 size-classic
  -rwxr-xr-x    1 root  admin    130816 Oct 20 09:24 stapler
  -rwxr-xr-x    1 root  admin    120400 Oct 20 09:23 strings
  -rwxr-xr-x    1 root  admin    189568 Oct 20 09:24 strip
  -rwxr-xr-x    1 root  admin    329168 Oct 20 09:24 svn
  -rwxr-xr-x    1 root  admin    111488 Oct 20 09:24 svnadmin
  -rwxr-xr-x    1 root  admin     98976 Oct 20 09:23 svnbench
  -rwxr-xr-x    1 root  admin     57008 Oct 20 09:24 svndumpfilter
  -rwxr-xr-x    1 root  admin     63600 Oct 20 09:23 svnfsfs
  -rwxr-xr-x    1 root  admin     90848 Oct 20 09:24 svnlook
  -rwxr-xr-x    1 root  admin     62256 Oct 20 09:23 svnmucc
  -rwxr-xr-x    1 root  admin     82384 Oct 20 09:24 svnrdump
  -rwxr-xr-x    1 root  admin    115840 Oct 20 09:24 svnserve
  -rwxr-xr-x    1 root  admin     83248 Oct 20 09:24 svnsync
  -rwxr-xr-x    1 root  admin     36400 Oct 20 09:24 svnversion
  -rwxr-xr-x    1 root  admin  87411088 Oct 20 09:23 swift
  lrwxr-xr-x    1 root  admin         5 Nov 13 12:35 swift-autolink-extract -> swift
  -rwxr-xr-x    1 root  admin   5031520 Oct 20 09:23 swift-build
  -rwxr-xr-x    1 root  admin    384480 Oct 20 09:23 swift-build-tool
  -rwxr-xr-x    1 root  admin    461136 Oct 20 09:24 swift-demangle
  lrwxr-xr-x    1 root  admin         5 Nov 13 12:35 swift-format -> swift
  -rwxr-xr-x    1 root  admin   5031552 Oct 20 09:23 swift-package
  -rwxr-xr-x    1 root  admin   5031472 Oct 20 09:23 swift-run
  -rwxr-xr-x    1 root  admin     53024 Oct 20 09:24 swift-stdlib-tool
  -rwxr-xr-x    1 root  admin   5031504 Oct 20 09:24 swift-test
  lrwxr-xr-x    1 root  admin         5 Nov 13 12:35 swiftc -> swift
  -rwxr-xr-x    1 root  admin  12000704 Oct 20 09:23 tapi
  -rwxr-xr-x    1 root  admin     32592 Oct 20 09:24 unifdef
  -rwxr-xr-x    1 root  admin      2946 Sep 26 08:55 unifdefall
  -rwxr-xr-x    1 root  admin     50272 Oct 20 09:24 unwinddump
  -rwxr-xr-x    1 root  admin     37120 Oct 20 09:23 xml2man
  -rwxr-xr-x    1 root  admin       135 Sep 26 08:57 yacc
```