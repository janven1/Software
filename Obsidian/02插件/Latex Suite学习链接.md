---
date_create: 2025-12-19-星期五
type: Software
software:
status: unstarted
source:
---
# 00链接

| 序号  |                                                             文件                                                             | 类型  | 介绍                     |    添加时间    |
| :-: | :------------------------------------------------------------------------------------------------------------------------: | :-: | ---------------------- | :--------: |
|  1  | [Latex suite](https://pkmer.cn/Pkmer-Docs/10-obsidian/obsidian%E7%A4%BE%E5%8C%BA%E6%8F%92%E4%BB%B6/obsidian-latex-suite/)  | 📰  | PKmer通过片段、文本扩展和编辑器增强功能 | 2025-12-19 |
|  2  |                           [LaTeX Suite插件使用说明书](https://zhuanlan.zhihu.com/p/1970279918010074629)                           | 📰  | 知乎说明书                  | 2025-12-19 |
|  3  | [ Latex Suite 插件的配置](https://zhuanlan.zhihu.com/p/1928918917822260425?share_code=xMnhPDpfpuGR&utm_psn=1971036474515391551) | 📰  | 介绍了latex suite教程       | 2025-12-19 |
|  4  |                                      [快速编辑的魔法](https://forum.pkmer.net/t/topic/7117)                                       | 📰  | Moy大佬编写的Latex suite案例  | 2025-12-19 |
| 99  |             [Latex suite code from others](https://github.com/artisticat1/obsidian-latex-suite/discussions/50)             | 💬  | 其他代码丰富使用方式             | 2025-12-19 |
## 99借鉴代码
Here are my favorite custom snippets, for your pleasure. I have plenty of text mode snippets, because this plugin is useful for more than just formatting math!

**Text Mode Snippets**

- Colored text in Obsidian using HTML snippets in text mode:  
    `{trigger: "clr", replacement: "\<font style=\"color:${0:Red}\"\>$1\<\/font\> $2", options: "tA", description: "Add colored font HTML"},`
    
- Automatically prettify header links  
    `{trigger: "\\[\\[(.*)#(.+)\\]\\]P", replacement: "[[[[0]]#[[1]]|[[1]]]]", options: "rtA", description: "Auto-prettify links (Capitalized headers)"},`  
    _Note 1_: I have versions of this snippet that paste in the alias in lower case, but it necessitates adding some lines to the JavaScript.  
    _Note 2_: A tabstop of the kind "...|${0:[[1]]}]]" does not work to auto-select the alias, as the entire link is selected automatically. I tried adding zero-width characters but Obsidian highlights them as errors.
    
- Automatically treat lone letters as math symbols:  
    `{trigger: "([^'])\\b((?![aAI])[a-zA-Z])\\b([\\n\\s\\.,])", replacement: "[[0]]$[[1]]$[[2]]", options: "rtA", description: "Automatically treat lone characters as math (except a, A, I)"},`  
    _Note 1_: This triggers before newline, space, comma and period, but not after an apostrophe. This can be changed in the first and last capture groups (...).  
    _Note 2_: Currently, this converts abbreviations like "i.e." "e.g." to math. To avoid this behavior add "ieg" to the lookahead exclusion group (?!...).
    
- Automatically treat numbers as math:  
    `{trigger: "\\b(-?\\d*\\.?\\d+)\\b(\\s|,|\\.\\s)", replacement: "$\\hspace{0pt}[[0]]$[[1]]", options: "rtA", description: "Automatically convert numbers to math"},`  
    _Note 1_: This detects positive numbers and decimals. It triggers before space, comma, or a period followed by a space. Therefore, for lists it's important to use the alternate notation "1) " rather than "1. "  
    _Note 2_: As of the writing of this comment ([Replacements with "$\d" or "[[\d" #49](https://github.com/artisticat1/obsidian-latex-suite/issues/49)), we can't have a digit follow the $ symbol in replacements, so a zero-width character is inserted.
    

**Math Mode Snippets**

- Color control in math mode:  
    `{trigger: "clr", replacement: "\\color{${0:white} $1", options: "mA", description: "Control math mode color"},`
    
- Common subscripts  
    `{trigger: "([a-zA-Z])(i|j|n|m|k|x|y)\\2{1}", replacement: "[[0]]_{[[1]]}", options: "rmA", description: "Common subscripts"},`  
    `{trigger: "([a-zA-Z])([a-zA-Z])p(\d)", replacement: "[[0]]_{[[1]]+[[2]]}", options: "rmA", description: "Common subscripts (plus)"},`  
    `{trigger: "([a-zA-Z])([a-zA-Z])m(\d)", replacement: "[[0]]_{[[1]]-[[2]]}", options: "rmA", description: "Common subscripts (minus)"},`  
    _Note 1_: This will subscript the letters in the group (i|j|...) if typed twice after a letter (xii →xi). Be careful writing out "gamma", or alter the list.  
    _Note 2_: The other lines implement xip1 →xi+1, ftm3 →ft−3 etc. .  
    _Note 3_: I made sure to remove "xi" from the Greek letter list in the JavaScript, but you can write custom snippets to override this issue.
    
- Articulated Sum  
    `{trigger: "\\summ", replacement: "\\sum_{${0:i}=1}^{${1:n}} $2", options: "mA", description: "Articulated sum"},`
    
- Vector/matrix transpose  
    `{trigger: "\\\\mathbf{([A-Za-z])}T", replacement: "\\mathbf{[[0]]}^{\\top}", options: "rmA", description: "Transpose"},`
    
- Align visual after the fact  
    `{trigger: "A", replacement: "\\begin{align}\n${VISUAL}\n\\end{align}", options: "mA", description: "Align visual"},`
    

Feel free to use any of these, and please let me know of any bugs and edge cases! Thanks again to [@artisticat1](https://github.com/artisticat1) for this plugin











# 01教程
功能：通过片段、文本扩展和编辑器增强功能
## 01基础语法
```text
{trigger:"关键词", replacement:"替换词", option:""},
```
- `trigger` : 触发规则的字串
- `replacement` : 替换成的字串;
- `options` : 替换选项
- `priority (optional)`: 优先级，数字越大优先级越高，默认是 0，可以是负数 (不是字符串)
- `flags (optional)`: 使用 正则表达式 来触发时，正则表达式的 flag

### options

|        标志         | 含义                                                |
| :---------------: | ------------------------------------------------- |
|         m         | 只在**数学公式中**有效                                     |
|         t         | 只在**数学公式之外**有效                                    |
|         M         | 只在**多行公式中**有效                                     |
|         n         | 只在**行内公式中**有效；<br>不自动添加空格（no space）               |
|         A         | 不需要转义符Tab也可被识别为trigger                            |
|         r         | 允许使用正则表达式作为 trigger                               |
|         v         | 只有在选中文本时才触发                                       |
|         c         | 只在 **代码块中** 有效                                    |
|         s         | 在触发后自动添加一个空格                                      |
|         w         | 仅在单词边界（word boundary）触发                           |
|         i         | 匹配时忽略大小写（case-insensitive）                        |
|         e         | 允许 snippet 替换选中文本（即选中一段内容后直接包裹）                   |
|    `$0,$1,...`    | 光标的跳跃顺序，替换后光标置于 `$0` 的位置，按一次 `tab` 跳转到 `$1` 的位置…… |
|     `${0:y}`      | 意思同上，不过设置默认值（此处是 y）                               |
| `[[1]],[[2]],...` | 正则表达式的捕获的分组 1，分组 2……                              |
|    `{VISUAL}`     | 表示选中的文本                                           |
### replace
replace 字段也可以是一个函数。
要编写替换函数，你需要一些「正则表达式」和「JavaScript」的知识，

## 02代码
### 01希腊字母

|     命令      |   简写   |     显示      |    命令    |   简写   |    显示     |
| :---------: | :----: | :---------: | :------: | :----: | :-------: |
|   \alpha    |   @a   |  $\alpha$   |    A     |        |     A     |
|    \beta    |   @b   |   $\beta$   |    B     |        |     B     |
|   \gamma    |   @g   |  $\gamma$   |  \Gamma  |   @G   | $\Gamma$  |
|   \delta    |   @d   |  $\delta$   |  \Delta  |   @D   | $\Delta$  |
| \varepsilon |   @e   | $\epsilon$  |    E     |        |     E     |
|   \theta    |   @t   |  $\theta$   |  \Theta  |   @T   | $\Theta$  |
|  \vartheta  |   :t   | $\vartheta$ |          |        |           |
|    \iota    |   @i   |   $\iota$   |  kappa   |   @k   | $\kappa$  |
|   \lambda   |   @l   |  $\lambda$  | \Lambda  |   @L   | $\Lambda$ |
|     \mu     |   mu   |    $\mu$    |    M     |        |     M     |
|     \nu     |   nu   |    $\nu$    |    N     |        |     N     |
|     \pi     |   pi   |    $\pi$    |   \Pi    |   Pi   |   $\Pi$   |
|    \rho     |  rho   |   $\rho$    |    P     |        |     P     |
|   \sigma    |   @s   |  $\sigma$   |  \Sigma  |   @S   | $\Sigma$  |
|    \tau     |  tau   |   $\tau$    |    T     |        |     T     |
|   \varphi   |   :p   |  $\varphi$  |   \Phi   |        |  $\Phi$   |
|    \psi     |  psi   |   $\psi$    |   \Psi   |        |  $\Psi$   |
|   \omega    | @o/ome |  $\omega$   |  \Omega  | @O/Ome | $\Omega$  |
|  \upsilon   |   @u   | $\upsilon$  | \Upsilon |        | \Upsilon  |
|             |        |             |  \zeta   |   @z   |  $\zeta$  |
### 02数学符号

#### 00来源

|            简写             |                                           显示                                            | 说明            | 状态  |
| :-----------------------: | :-------------------------------------------------------------------------------------: | ------------- | :-: |
|           avec            |                                         \vec{a}                                         | 向量            |  ✅  |
|            sr             |                                          ^{2}                                           |               |  ✅  |
|            cb             |                                          ^{3}                                           |               |  ✅  |
|            rd             |                                          ^{n}                                           |               |  ✅  |
|             _             |                                         `_{n}`                                          |               |  ✅  |
|            sts            |                                     $a_\text{Text}$                                     |               |     |
|           conj            |                                         $a^{*}$                                         | 转置            |     |
|            bf             |                                      $\mathbf{A}$                                       | 粗体            |     |
|            rm             |                                      $\mathrm{A}$                                       | 正体            |     |
|           ahat            |                                        $\hat{a}$                                        |               |     |
|           abar            |                                        $\bar{a}$                                        |               |  ✅  |
|           adot            |                                        $\dot{a}$                                        | 低优先级          |     |
|          atilde           |                                       $\tilde{a}$                                       |               |     |
|           aund            |                                     $\underline{a}$                                     |               |     |
|            .,             |                                  $\boldsymbol{\alpha}$                                  | 将前面的字母加粗      |     |
|            ===            |                                        $\equiv$                                         |               |     |
|      !=,>=,<=,>>,<<,      |                                 \neq,\geq,\leq,\gg,\ll                                  |               |  ✅  |
|           simm            |                                         $\sim$                                          |               |     |
|           simeq           |                                        $\simeq$                                         |               |     |
|           prop            |                                        $\propto$                                        | 正相关           |  ✅  |
|            <->            |                                    $\leftrightarrow$                                    |               |     |
|        ->,!>,=>,=<        |                             \to,\mapsto,\implies,\impliedby                             |               |  ✅  |
| LL,HH,<br>CC,RR,<br>ZZ,NN | $\mathcal{L}$,$\mathcal{H}$,<br>$\mathbb{C}$,$\mathbb{R}$,<br>$\mathbb{Z}$,$\mathbb{N}$ |               |     |
|          par+Tab          |                            \frac{ \partial y }{ \partial x }                            |               |  ✅  |
|         paab+Tab          |                            \frac{ \partial a }{ \partial b }                            |               |  ✅  |
|            ddt            |                                      \frac{d}{dt}                                       |               |  ✅  |
|        int,int+Tab        |                                       \int \, dx                                        | +Tab显示dx      |  ✅  |
|           dint            |                              \int_{\infty}^{-\infty} \, dx                              | 带上下限的积分       |  ✅  |
|      oint,iint,iiint      |                                   \oint,\iint,\iiint                                    |               |  ✅  |
|           infi            |                              \int_{-\infty}^{\infty} \, dx                              | 上下限为\infty的积分 |  ✅  |
|            kbt            |                                        $k_{B}T$                                         | 物理学常用         |     |
|           msun            |                                       $M_{\odot}$                                       | 太阳质量          |     |
|            dag            |                                      $^{\dagger}$                                       | dagger        |     |
|            o+             |                                        $\oplus$                                         | 张量积           |     |
|            ox             |                                        $\otimes$                                        |               |     |
|            bra            |                                        $\bra{x}$                                        |               |     |
|            ket            |                                        $\ket{x}$                                        |               |     |
|            brk            |                                   $\braket{ x \\ y }$                                   |               |     |
|           outer           |                                 $\ket{\psi} \bra{\psi}$                                 |               |     |
|            sq             |                                       \sqrt{ a }                                        |               |  ✅  |
|            lim            |                                 $\lim_{ n \to \infty }$                                 |               |  ✅  |
|            //             |                                       \frac{a}{b}                                       |               |  ✅  |
|            ee             |                                         e^{ n }                                         |               |  ✅  |
|           invs            |                                         a^{-1}                                          |               |  ✅  |
|            a1             |                                          a_{1}                                          |               |  ✅  |
|            xnn            |                                          x_{n}                                          |               |  ✅  |
|            xii            |                                          x_{i}                                          |               |  ✅  |
|            xp1            |                                         x_{n+1}                                         |               |  ✅  |
|            ooo            |                                         \infty                                          |               |  ✅  |
|            sum            |                                          \sum                                           |               |     |
|           prod            |                                          \prod                                          |               |     |
|           +-,-+           |                                       $\pm$,$\mp$                                       |               |  ✅  |
|            ...            |                                          \dots                                          | \dots         |     |
|         nabl,del          |                                        $\nabla$                                         |               |     |
|            xx             |                                        $\times$                                         | \times        |  ✅  |
|            **             |                                         $\cdot$                                         | \cdot         |  ✅  |
|           para            |                                        \parallel                                        | 平行            |     |
|            and            |                                          \cap                                           |               |     |
|            orr            |                                          \cup                                           |               |     |
|            inn            |                                           \in                                           |               |     |
|           notin           |                                         \not\in                                         |               |     |
|           sub=            |                                        \subseteq                                        |               |     |
|           sup=            |                                        \supseteq                                        |               |     |
|           eset            |                                        \emptyset                                        |               |     |
|            set            |                                        \{ 1,2 \}                                        | 集合{}          |     |
|          exists           |                                         \exists                                         | 防止\si被识别      |     |
|            pu             |                                  \pu{ 10 KJ.mol^{-1} }                                  | 书写带单位的物理量     |     |
|            cee            |                                    \ce{ H2+O2->H2O }                                    | 用于书写化学学方程式    |     |
|          he4,he3          |                               `{}^{4}_{2}He,{}^{3}_{2}He`                               | 快速书写核素        |     |
|            iso            |                                      {}^{16}_{4}C                                       | 书写自定义核素       |     |
|            avg            |                                   \langle a,b \rangle                                   | 平均值           |     |
|           norm            |                                    \lvert a,b\rvert                                     | 绝对值           |  ✅  |
|           Norm            |                                    \lVert a,b \rVert                                    | 范数            |     |
|           ceil            |                                     \lceil a \rceil                                     | 上取整           |     |
|           floor           |                                    \lfloor a \rfloor                                    | 下取整           |     |
|            mod            |                                           \\                                            | `a,b\\`       |     |
#### 01基础符号

| 序号  |       简写        | 显示                              | 说明          |
| :-: | :-------------: | ------------------------------- | ----------- |
|  1  |       sr        | ^{2}                            |             |
|  2  |       cb        | ^{3}                            |             |
|  3  |       rd        | ^{n}                            |             |
|  4  |       ee        | $e^{ n }$                       |             |
|  5  |      invs       | $a^{-1}$                        |             |
|  6  |       a1        | $a_{1}$                         |             |
|  7  |        _        | `_{n}`                          |             |
|  8  |       xnn       | $x_{n}$                         |             |
|  9  |       xp1       | $x_{n+1}$                       |             |
| 10  |       xii       | $x_{i}$                         |             |
| 11  |      abar       | $\bar{a}$                       |             |
| 12  |     `a`vec      | $\vec{a}$                       | 向量；`a`可以被替换 |
| 13  |       rm        | $\mathrm{A}$                    | 正体          |
| 14  |       //        | $\frac{a}{b}$                   |             |
| 15  |       xx        | $\times$                        | \times      |
| 16  |      +-,-+      | $\pm$,$\mp$                     |             |
| 17  |       sq        | $\sqrt{ a }$                    |             |
| 18  | !=,>=,<=,>>,<<, | \neq,\geq,\leq,\gg,\ll          |             |
| 19  |      norm       | \lvert a,b\rvert                | 绝对值         |
| 20  |   ->,!>,=>,=<   | \to,\mapsto,\implies,\impliedby |             |

| 序号  |  简写  | 显示        | 说明    |
| :-: | :--: | --------- | ----- |
| 21  | prop | $\propto$ | 正相关   |
| 22  |  **  | $\cdot$   | \cdot |
| 23  | ...  | $\dots$   | \dots |
#### 02微积分

| 序号  |       简写        | 显示                                | 说明            |
| :-: | :-------------: | --------------------------------- | ------------- |
|  1  |       lim       | \lim_{ n \to \infty }             |               |
|  2  |       ooo       | \infty                            |               |
|  3  |       ddt       | \frac{d}{dt}                      |               |
|  4  |   int,int+Tab   | \int \, dx                        | +Tab显示dx      |
|  5  |      dint       | \int_{\infty}^{-\infty} \, dx     | 带上下限的积分       |
|  6  | oint,iint,iiint | \oint,\iint,\iiint                |               |
|  7  |      infi       | \int_{-\infty}^{\infty} \, dx     | 上下限为\infty的积分 |
|  8  |    par+`Tab`    | \frac{ \partial y }{ \partial x } |               |
|  9  |    paab+Tab     | \frac{ \partial a }{ \partial b } |               |
| 10  |    nabl,del     | $\nabla$                          |               |

#### 03线代

| 序号  | 简写  | 显示  | 说明  |
| :-: | :-: | --- | --- |
|  1  |     |     |     |
|  2  |     |     |     |
|  3  |     |     |     |
