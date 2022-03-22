---
date: 2021-03-09T10:58:08-04:00
description: "记录了 Vim 编辑器常用命令速查功能，这些命令分为全局命令、光标移动、插入模式、文本编辑、缩进、复制、查找 / 替换、宏、寄存器、标签、差异比较等常用的 Vim 命令，是每位 Vim 使用者必备的参考资料。"
featured_image: "/images/Pope-Edouard-de-Beaumont-1844.jpg"
images: ["/images/Pope-Edouard-de-Beaumont-1844.jpg"]
tags: ["scene"]
categories: "Story"
title: " Vim命令速查"
---




> 本速查表按分类列出了 Vim 常用的命令和快捷键，数量较多，可使用 Ctrl + F 进行查找。

全局命令
----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:h[elp] 关键字</kbd></td><td>显示指定关键字的帮助</td></tr><tr><td><kbd>:sav[eas] 文件名</kbd></td><td>另存为...</td></tr><tr><td><kbd>:clo[se]</kbd></td><td>关闭当前窗口</td></tr><tr><td><kbd>:ter[minal]</kbd></td><td>打开新的终端窗口</td></tr><tr><td><kbd>K</kbd></td><td>打开光标所在单词对应的 man 页面</td></tr></tbody></table>

移动光标
----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>h</kbd></td><td>左移光标</td></tr><tr><td><kbd>j</kbd></td><td>下移光标</td></tr><tr><td><kbd>k</kbd></td><td>上移光标</td></tr><tr><td><kbd>l</kbd></td><td>右移光标</td></tr><tr><td><kbd>H</kbd></td><td>移动到当前页面顶部</td></tr><tr><td><kbd>M</kbd></td><td>移动到当前页面中间</td></tr><tr><td><kbd>L</kbd></td><td>移动到当前页面底部</td></tr><tr><td><kbd>w</kbd></td><td>移动到下个单词开头</td></tr><tr><td><kbd>W</kbd></td><td>移动到下个单词开头（单词含标点）</td></tr><tr><td><kbd>e</kbd></td><td>移动到下个单词结尾</td></tr><tr><td><kbd>E</kbd></td><td>移动到下个单词结尾（单词含标点）</td></tr><tr><td><kbd>b</kbd></td><td>移动到上个单词开头</td></tr><tr><td><kbd>B</kbd></td><td>移动到上个单词开头（单词含标点）</td></tr><tr><td><kbd>%</kbd></td><td>跳转到配对的符号</td></tr><tr><td><kbd>0</kbd></td><td>移动到行首</td></tr><tr><td><kbd>^</kbd></td><td>移动到行首的非空白符</td></tr><tr><td><kbd>$</kbd></td><td>移动到行尾</td></tr><tr><td><kbd>g_</kbd></td><td>移动到行内最后一个非空白符</td></tr><tr><td><kbd>gg</kbd></td><td>移动到文件第一行</td></tr><tr><td><kbd>G</kbd></td><td>移动到文件最后一行</td></tr><tr><td><kbd>5gg</kbd> 或 <kbd>5G</kbd></td><td>移动到第 5 行</td></tr><tr><td><kbd>fx</kbd></td><td>移动到字符 <code>x</code> 下次出现的位置</td></tr><tr><td><kbd>tx</kbd></td><td>移动到字符 <code>x</code> 下次出现的位置的前一个字符</td></tr><tr><td><kbd>Fx</kbd></td><td>移动到字符 <code>x</code> 上次出现的位置</td></tr><tr><td><kbd>Tx</kbd></td><td>移动到字符 <code>x</code> 上次出现的位置的后一个字符</td></tr><tr><td><kbd>;</kbd></td><td>重复之前的 <kbd>f</kbd>、<kbd>t</kbd>、<kbd>F</kbd>、<kbd>T</kbd> 操作</td></tr><tr><td><kbd>,</kbd></td><td>反向重复之前的 <kbd>f</kbd>、<kbd>t</kbd>、<kbd>F</kbd>、<kbd>T</kbd> 操作</td></tr><tr><td><kbd>}</kbd></td><td>移动到下一个段落（当编辑代码时则为函数／代码块）</td></tr><tr><td><kbd>{</kbd></td><td>移动到上一个段落（当编辑代码时则为函数／代码块）</td></tr><tr><td><kbd>zz</kbd></td><td>移动屏幕使光标居中</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>e</kbd></td><td>向下移动屏幕一行（保持光标不动）</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>y</kbd></td><td>向上移动屏幕一行（保持光标不动）</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>b</kbd></td><td>向上滚动一屏</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>f</kbd></td><td>向下滚动一屏</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>d</kbd></td><td>向下滚动半屏</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>u</kbd></td><td>向上滚动半屏</td></tr></tbody></table>

插入模式（插入 / 追加文本）
---------------

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>i</kbd></td><td>从光标前开始插入字符</td></tr><tr><td><kbd>I</kbd></td><td>从行首开始插入字符</td></tr><tr><td><kbd>a</kbd></td><td>从光标后开始插入字符</td></tr><tr><td><kbd>A</kbd></td><td>从行尾开始插入字符</td></tr><tr><td><kbd>o</kbd></td><td>在当前行之下另起一行，开始插入字符</td></tr><tr><td><kbd>O</kbd></td><td>在当前行之上另起一行，开始插入字符</td></tr><tr><td><kbd>ea</kbd></td><td>从当前单词末尾开始插入</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>h</kbd></td><td>在插入模式下，删除光标前的字符</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>w</kbd></td><td>在插入模式下，删除光标前的单词</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>j</kbd></td><td>在插入模式下，另起一行</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>t</kbd></td><td>在插入模式下，向右缩进，宽度由 <code>shiftwidth</code> 控制</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>d</kbd></td><td>在插入模式下，向左缩进，宽度由 <code>shiftwidth</code> 控制</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>n</kbd></td><td>在插入模式下，在光标之前插入自动补全的下一个匹配项</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>p</kbd></td><td>在插入模式下，在光标之前插入自动补全的上一个匹配项</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>rx</kbd></td><td>在当前光标处插入 x 寄存器的内容</td></tr><tr><td><kbd>Esc</kbd></td><td>退出插入模式</td></tr></tbody></table>

编辑文本
----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>r</kbd></td><td>替换当前字符</td></tr><tr><td><kbd>J</kbd></td><td>将下一行合并到当前行，并在两部分文本之间插入一个空格</td></tr><tr><td><kbd>gJ</kbd></td><td>将下一行合并到当前行，两部分文本之间不含空格</td></tr><tr><td><kbd>gwip</kbd></td><td>重新调整段落</td></tr><tr><td><kbd>g~</kbd></td><td>切换整个文本的大小写（即大写变小写，小写变大写）</td></tr><tr><td><kbd>gu</kbd></td><td>把整个文本改成小写</td></tr><tr><td><kbd>gU</kbd></td><td>把整个文本改成大写</td></tr><tr><td><kbd>cc</kbd> 或 <kbd>S</kbd></td><td>将光标所在的行删除，然后进入插入模式</td></tr><tr><td><kbd>C</kbd> 或 <kbd>c$</kbd></td><td>删除光标所在位置到行尾的所有文本，然后进入插入模式</td></tr><tr><td><kbd>ciw</kbd></td><td>将光标所在的单词删除，然后进入插入模式</td></tr><tr><td><kbd>cw</kbd></td><td>从光标位置开始，修改单词</td></tr><tr><td><kbd>s</kbd></td><td>删除当前字符，然后进入插入模式</td></tr><tr><td><kbd>xp</kbd></td><td>将当前字符后移</td></tr><tr><td><kbd>u</kbd></td><td>undo - 撤销最近一次操作</td></tr><tr><td><kbd>U</kbd></td><td>恢复 / 撤销最后修改的行</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>r</kbd></td><td>redo - 重做（和 <kbd>u</kbd> 相反）</td></tr><tr><td><kbd>.</kbd></td><td>再次执行上一个命令</td></tr></tbody></table>

选择文本（可视化模式）
-----------

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>v</kbd></td><td>进入可视化模式，移动光标高亮选择，然后，可以对被选中的文本执行命令</td></tr><tr><td><kbd>V</kbd></td><td>进行可视化模式，以行为单位进行选择</td></tr><tr><td><kbd>o</kbd></td><td>在可视化模式下，让光标在选择区域的开头和结尾进行切换</td></tr><tr><td><kbd>O</kbd></td><td>在可视化模式下，切换光标到选择区域的角</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>v</kbd></td><td>进入可视化模式，矩阵选择（即列模式）</td></tr><tr><td><kbd>aw</kbd></td><td>在可视化模式下，选择当前单词</td></tr><tr><td><kbd>ab</kbd></td><td>在可视化模式下，选择被 <code>()</code> 包裹的区域的内容（包含括号）</td></tr><tr><td><kbd>aB</kbd></td><td>在可视化模式下，选择被 <code>{}</code> 包裹的区域的内容（包含花括号）</td></tr><tr><td><kbd>at</kbd></td><td>在可视化模式下，选择被 <code>&lt;&gt;</code> 包裹的区域的内容（包含 &lt;&gt; 标签）</td></tr><tr><td><kbd>ib</kbd></td><td>在可视化模式下，选择被 <code>()</code> 包裹的区域的内容（不包含括号）</td></tr><tr><td><kbd>iB</kbd></td><td>在可视化模式下，选择被 <code>{}</code> 包裹的区域的内容（不包含花括号）</td></tr><tr><td><kbd>it</kbd></td><td>在可视化模式下，选择被 <code>&lt;&gt;</code> 包裹的区域的内容（不包含 &lt;&gt; 标签）</td></tr><tr><td><kbd>Esc</kbd></td><td>退出可视化模式</td></tr></tbody></table>

可视化模式命令
-------

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>&gt;</kbd></td><td>向右缩进</td></tr><tr><td><kbd>&lt;</kbd></td><td>向左缩进</td></tr><tr><td><kbd>y</kbd></td><td>复制选中的文本</td></tr><tr><td><kbd>d</kbd></td><td>剪切选中的文本</td></tr><tr><td><kbd>~</kbd></td><td>对选中的文本进行大小写切换</td></tr><tr><td><kbd>u</kbd></td><td>将选中的文本转换为小写</td></tr><tr><td><kbd>U</kbd></td><td>将选中的文本转换为大写</td></tr></tbody></table>

寄存器
---

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:reg[isters]</kbd></td><td>显示寄存器的内容</td></tr><tr><td><kbd>"xy</kbd></td><td>复制内容到寄存器 x</td></tr><tr><td><kbd>"xp</kbd></td><td>粘贴寄存器 x 中的内容</td></tr><tr><td><kbd>"+y</kbd></td><td>复制内容到系统剪贴板寄存器</td></tr><tr><td><kbd>"+p</kbd></td><td>粘贴系统剪贴板寄存器的内容</td></tr></tbody></table>

标记和位置
-----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:marks</kbd></td><td>显示标记列表</td></tr><tr><td><kbd>ma</kbd></td><td>设置当前位置为标记 a</td></tr><tr><td><kbd>`a</kbd></td><td>跳转到标记 a 的位置</td></tr><tr><td><kbd>`0</kbd></td><td>跳转到 Vim 上一次退出时的位置</td></tr><tr><td><kbd>`"</kbd></td><td>跳转到该文件上次编辑时的位置</td></tr><tr><td><kbd>`.</kbd></td><td>跳转到该文件中最后一次修改的位置</td></tr><tr><td><kbd>``</kbd></td><td>跳转到最后跳转的位置</td></tr><tr><td><kbd>:ju[mps]</kbd></td><td>列出所有跳转</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>i</kbd></td><td>转到跳转列表较新的位置</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>o</kbd></td><td>转到跳转列表较旧的位置</td></tr><tr><td><kbd>:changes</kbd></td><td>列出所有修改历史</td></tr><tr><td><kbd>g,</kbd></td><td>转到修改历史列表较新的位置</td></tr><tr><td><kbd>g;</kbd></td><td>转到修改历史列表较旧的位置</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>]</kbd></td><td>跳转到当前光标所在的标签</td></tr></tbody></table>

宏
-

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>qa</kbd></td><td>录制宏 a</td></tr><tr><td><kbd>q</kbd></td><td>停止录制宏</td></tr><tr><td><kbd>@a</kbd></td><td>执行宏 a</td></tr><tr><td><kbd>@@</kbd></td><td>重新执行上次执行的宏</td></tr></tbody></table>

复制、剪切和粘贴
--------

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>yy</kbd></td><td>复制当前行</td></tr><tr><td><kbd>2yy</kbd></td><td>复制 2 行</td></tr><tr><td><kbd>yw</kbd></td><td>复制当前单词</td></tr><tr><td><kbd>y$</kbd></td><td>复制从光标位置开始到行末的内容</td></tr><tr><td><kbd>p</kbd></td><td>在光标后粘贴复制的内容</td></tr><tr><td><kbd>P</kbd></td><td>在光标前粘贴复制的内容</td></tr><tr><td><kbd>dd</kbd></td><td>剪切当前行</td></tr><tr><td><kbd>2dd</kbd></td><td>剪切 2 行</td></tr><tr><td><kbd>dw</kbd></td><td>剪切当前单词</td></tr><tr><td><kbd>d$</kbd> 或 <kbd>D</kbd></td><td>剪切从光标位置开始到行末的内容</td></tr><tr><td><kbd>x</kbd></td><td>剪切当前字符</td></tr></tbody></table>

文本缩进
----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>&gt;&gt;</kbd></td><td>将当前行向右缩进，宽度由 <code>shiftwidth</code> 控制</td></tr><tr><td><kbd>&lt;&lt;</kbd></td><td>将当前行向左缩进，宽度由 <code>shiftwidth</code> 控制</td></tr><tr><td><kbd>&gt;%</kbd></td><td>向右缩进 <code>()</code> 或 <code>{}</code> 内的区域（光标需置于括号上）</td></tr><tr><td><kbd>&gt;ib</kbd></td><td>向右缩进 <code>()</code> 内的区域（光标需置于括号上）</td></tr><tr><td><kbd>&gt;at</kbd></td><td>向右缩进 <code>&lt;&gt;</code> 标签内的区域（光标需置于 &lt;&gt; 标签上）</td></tr><tr><td><kbd>3==</kbd></td><td>自动缩进 3 行</td></tr><tr><td><kbd>=%</kbd></td><td>自动缩进 <code>()</code> 或 <code>{}</code> 内的区域（光标需置于括号上）</td></tr><tr><td><kbd>=iB</kbd></td><td>自动缩进 <code>{}</code> 内的区域（光标需置于括号上）</td></tr><tr><td><kbd>gg=G</kbd></td><td>自动缩进整个缓冲区</td></tr><tr><td><kbd>]p</kbd></td><td>粘贴并调整缩进至当前行</td></tr></tbody></table>

文本搜索和替换
-------

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>/pattern</kbd></td><td>在当前文本中查找 <code>pattern</code></td></tr><tr><td><kbd>?pattern</kbd></td><td>向上查找 <code>pattern</code></td></tr><tr><td><kbd>\vpattern</kbd></td><td>把 <code>pattern</code> 中的非字母数字字符视为正则表达式特殊字符（不需转义字符）</td></tr><tr><td><kbd>n</kbd></td><td>查找下一个</td></tr><tr><td><kbd>N</kbd></td><td>查找上一个</td></tr><tr><td><kbd>:%s/old/new/g</kbd></td><td>把 <code>old</code> 全部替换成 <code>new</code></td></tr><tr><td><kbd>:%s/old/new/gc</kbd></td><td>把 <code>old</code> 逐个替换成 <code>new</code></td></tr><tr><td><kbd>:noh[lsearch]</kbd></td><td>移除搜索结果的高亮显示</td></tr></tbody></table>

多文件编辑
-----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:e[dit] 文件名</kbd></td><td>在新建的缓冲区打开指定文件名的文件</td></tr><tr><td><kbd>:bn[ext]</kbd></td><td>切换到下一个缓冲区</td></tr><tr><td><kbd>:bp[revious]</kbd></td><td>切换到上一个缓冲区</td></tr><tr><td><kbd>:bd[elete]</kbd></td><td>关闭缓冲区</td></tr><tr><td><kbd>:b[uffer]2</kbd></td><td>切换到第 2 个缓冲区</td></tr><tr><td><kbd>:b[uffer] 文件</kbd></td><td>切换到指定文件的缓冲区</td></tr><tr><td><kbd>:ls</kbd> 或 <kbd>:buffers</kbd></td><td>列出所有打开的缓冲区</td></tr><tr><td><kbd>:sp[lit] 文件名</kbd></td><td>在新建的缓冲区打开指定文件名的文件，并水平分割窗口</td></tr><tr><td><kbd>:vs[lit] 文件名</kbd></td><td>在新建的缓冲区打开指定文件名的文件，并垂直分割窗口</td></tr><tr><td><kbd>:vert[ical] ba[ll]</kbd></td><td>以垂直窗口的形式编辑所有缓冲区</td></tr><tr><td><kbd>:tab ba[ll]</kbd></td><td>以标签的形式编辑所有缓冲区</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>ws</kbd></td><td>水平分割窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wv</kbd></td><td>垂直分割窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>ww</kbd></td><td>在窗口间切换</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wq</kbd></td><td>关闭窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wx</kbd></td><td>切换到下一个窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>w=</kbd></td><td>让每个窗口具有相同高度和宽度</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wh</kbd></td><td>切换到左侧窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wl</kbd></td><td>切换到右侧窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wj</kbd></td><td>切换到下侧窗口</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wk</kbd></td><td>切换到上侧窗口</td></tr></tbody></table>

多文件搜索
-----

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:vim[grep] /pattern/ {`{file}`}</kbd></td><td>在多个文件中搜索 <code>pattern</code></td></tr><tr><td><kbd>:cn[ext]</kbd></td><td>移动至下一个搜索结果</td></tr><tr><td><kbd>:cp[revious]</kbd></td><td>移动至上一个搜索结果</td></tr><tr><td><kbd>:cope[n]</kbd></td><td>打开搜索结果列表</td></tr><tr><td><kbd>:ccl[ose]</kbd></td><td>关闭 quickfix 窗口</td></tr></tbody></table>

标签
--

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:tabnew</kbd> 或 <kbd>tabnew {page.words.file}</kbd></td><td>在新标签中打开文件</td></tr><tr><td><kbd>Ctrl</kbd> + <kbd>wT</kbd></td><td>将窗口编程标签</td></tr><tr><td><kbd>gt</kbd> 或 <kbd>:tabn[ext]</kbd></td><td>切换到下一个标签</td></tr><tr><td><kbd>gT</kbd> 或 <kbd>:tabp[revious]</kbd></td><td>切换到上一个标签</td></tr><tr><td><kbd>2gt</kbd></td><td>切换到第 2 个标签</td></tr><tr><td><kbd>:tabm[ove] 2</kbd></td><td>把当前标签移动到第 2 个位置（下表从 0 开始）</td></tr><tr><td><kbd>tabc[lose]</kbd></td><td>关闭当前标签</td></tr><tr><td><kbd>:tabo[nly]</kbd></td><td>关闭其他标签</td></tr><tr><td><kbd>:tabdo command</kbd></td><td>在所有标签中执行指定的命令（如：使用 <kbd>tabdo q</kbd> 关闭所有标签）</td></tr></tbody></table>

Diff（文件比较）
----------

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>zf</kbd></td><td>手动定义一个折迭行为</td></tr><tr><td><kbd>zd</kbd></td><td>删除光标处的折迭</td></tr><tr><td><kbd>za</kbd></td><td>展开 / 收起光标处的区块</td></tr><tr><td><kbd>zo</kbd></td><td>展开光标处的区块</td></tr><tr><td><kbd>zc</kbd></td><td>折迭光标处的区块</td></tr><tr><td><kbd>zr</kbd></td><td>展开当前折迭层级</td></tr><tr><td><kbd>zm</kbd></td><td>收起当前折迭层级</td></tr><tr><td><kbd>zi</kbd></td><td>切换折迭功能</td></tr><tr><td><kbd>]c</kbd></td><td>跳转到下一个不同处</td></tr><tr><td><kbd>[c</kbd></td><td>跳转到上一个不同处</td></tr><tr><td><kbd>do</kbd> 或 <kbd>:diffg[et]</kbd></td><td>从其他缓冲区获取不同之处</td></tr><tr><td><kbd>dp</kbd> 或 <kbd>:diffpu[t]</kbd></td><td>把不同之处存入其他缓冲区</td></tr><tr><td><kbd>:diffthis</kbd></td><td>把当前窗口的内容作为文件对比的一部分</td></tr><tr><td><kbd>:dif[fupdate]</kbd></td><td>刷新，重新比较</td></tr><tr><td><kbd>:diffo[ff]</kbd></td><td>关闭当前窗口的 Diff 模式</td></tr></tbody></table>

退出
--

<table><thead><tr><th width="30%">命令 / 快捷键</th><th>功能描述</th></tr></thead><tbody><tr><td><kbd>:w</kbd></td><td>保存</td></tr><tr><td><kbd>:w !sudo tee %</kbd></td><td>使用 <code>sudo</code> 保存当前文件</td></tr><tr><td><kbd>:wq</kbd> 或 <kbd>:x</kbd> 或 <kbd>ZZ</kbd></td><td>保存并退出</td></tr><tr><td><kbd>:q</kbd></td><td>退出（文件已修改且未保存时 Vim 将发出警告）</td></tr><tr><td><kbd>:q!</kbd> 或 <kbd>ZQ</kbd></td><td>强制退出（即使文件未保存）</td></tr><tr><td><kbd>:wqa</kbd></td><td>保存所有标签页，并全部退出</td></tr></tbody></table>