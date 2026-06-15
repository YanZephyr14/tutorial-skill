# LaTeX 公式语法教程

> 从零开始，掌握写数学公式的核心技能

---

## 📑 目录

- [1. 什么是 LaTeX？](#1-什么是-latex)
- [2. 核心概念](#2-核心概念)
- [3. 快速上手](#3-快速上手)
- [4. 常用符号详解](#4-常用符号详解)
  - [4.1 希腊字母](#41-希腊字母)
  - [4.2 运算符](#42-运算符)
  - [4.3 分数与根号](#43-分数与根号)
  - [4.4 上标与下标](#44-上标与下标)
  - [4.5 括号与定界符](#45-括号与定界符)
  - [4.6 求和、积分、极限](#46-求和积分极限)
  - [4.7 箭头](#47-箭头)
  - [4.8 矩阵](#48-矩阵)
- [5. 完整工作流程](#5-完整工作流程)
- [6. 公式组装：从简单到复杂](#6-公式组装从简单到复杂)
- [7. 实际使用场景](#7-实际使用场景)
  - [7.1 数学基础](#71-数学基础)
  - [7.2 物理学](#72-物理学)
  - [7.3 数据科学与机器学习](#73-数据科学与机器学习)
  - [7.4 化学与经济学](#74-化学与经济学)
  - [7.5 概率统计与线性代数](#75-概率统计与线性代数)
  - [7.6 微积分](#76-微积分)
- [8. 常见问题](#8-常见问题)
- [9. 快速参考卡片](#9-快速参考卡片)
- [附录：记忆口诀大全](#附录记忆口诀大全)

---

## 1. 什么是 LaTeX？

### 一句话定义

LaTeX（读作"拉泰赫"）是一种**数学公式的书写语言**，你用特定的文字描述公式，它帮你渲染成漂亮的数学符号。

### 一个类比

| 生活中的例子 | LaTeX 的对应 |
|-------------|-------------|
| 你用拼音打字 | 你用 LaTeX 代码写公式 |
| 输入法把拼音变成汉字 | LaTeX 把代码变成漂亮的数学符号 |
| 你不需要知道汉字的笔画顺序 | 你不需要手动调整公式的大小和位置 |

**类比：** LaTeX 就像数学公式的"输入法"——你告诉它你想写什么，它帮你排版得漂漂亮亮的。

### 核心价值

- **一次学会，到处使用**：Markdown、Word、PPT、网页都能用
- **公式永远好看**：自动处理大小、间距、对齐
- **写起来快**：熟练后比鼠标点快 10 倍

---

## 2. 核心概念

### 2.1 两种数学模式

就像说话有"低声说"和"大声说"两种方式，LaTeX 写公式也有两种模式：

| 模式 | 用途 | 写法 | 示例 |
|------|------|------|------|
| **行内公式** | 在文字中间插入公式 | `$公式$` | 这是一个公式 $E=mc^2$ 在文字中间 |
| **行间公式** | 公式独占一行，更醒目 | `$$公式$$` | 这是独立的一行：$$E=mc^2$$ |

**类比：**
- 行内公式 = 在句子中夹一个数学符号（像这样：$x+1$）
- 行间公式 = 公式单独站一行，像写在黑板上一样醒目

### 2.2 保留字符

LaTeX 中有一些字符有特殊含义，不能直接输入：

| 字符 | 含义 | 想显示它？用这个 |
|------|------|-----------------|
| `$` | 进入/退出数学模式 | `\$` |
| `%` | 注释（后面的不显示） | `\%` |
| `_` | 下标 | `\_` |
| `^` | 上标 | `\^` |
| `{` | 分组开始 | `\{` |
| `}` | 分组结束 | `\}` |
| `\` | 命令开始 | `\backslash` |
| `#` | 参数标记 | `\#` |
| `&` | 表格对齐 | `\&` |
| `~` | 不换行空格 | `\~` |

**记忆技巧：** 大部分特殊字符，前面加个 `\` 就能显示它本身。

### 2.3 基本规则

1. **字母变变量**：数学模式里，`abc` 会显示为斜体的 $abc$（表示变量）
2. **空格被忽略**：`a b c` 和 `abc` 显示效果一样
3. **用命令加空格**：`\,`（小空格）、`\;`（中空格）、`\quad`（大空格）

---

## 3. 快速上手

### 你的第一个公式

```
$E = mc^2$
```

显示效果：$E = mc^2$

### 逐行解释

| 代码 | 含义 |
|------|------|
| `$` | 开始行内公式 |
| `E` | 字母 E（会显示为斜体变量） |
| `=` | 等号（直接输入） |
| `m` | 字母 m |
| `c` | 字母 c |
| `^2` | 上标，表示"平方" |
| `$` | 结束行内公式 |

### 试试看：5 个最简单的公式

```latex
$x + y = z$          # 加法
$a - b = c$          # 减法
$x \times y = z$     # 乘法（用 \times）
$a \div b = c$       # 除法（用 \div）
$x^2 + y^2 = z^2$    # 平方
```

显示效果：
- $x + y = z$
- $a - b = c$
- $x \times y = z$
- $a \div b = c$
- $x^2 + y^2 = z^2$

### ✏️ 小练习

**练习 1：** 写出"10 除以 2 等于 5"的 LaTeX 公式

<details>
<summary>查看答案</summary>

```latex
$10 \div 2 = 5$
```

显示效果：$10 \div 2 = 5$

</details>

**练习 2：** 写出"a 的 3 次方"的 LaTeX 公式

<details>
<summary>查看答案</summary>

```latex
$a^3$
```

显示效果：$a^3$

</details>

---

## 4. 常用符号详解

### 4.1 希腊字母

数学里经常用希腊字母表示变量，比如 $\alpha$、$\beta$、$\pi$。

**类比：** 希腊字母就像数学里的"特殊符号"，用来表示特定的数学概念。

#### 小写希腊字母

| 符号 | 代码 | 常见用途 |
|------|------|---------|
| $\alpha$ | `\alpha` | 角度、系数 |
| $\beta$ | `\beta` | 角度、系数 |
| $\gamma$ | `\gamma` | 角度、伽马函数 |
| $\delta$ | `\delta` | 微小变化量 |
| $\epsilon$ | `\epsilon` | 极小正数 |
| $\zeta$ | `\zeta` | 黎曼ζ函数 |
| $\eta$ | `\eta` | 效率 |
| $\theta$ | `\theta` | 角度 |
| $\lambda$ | `\lambda` | 特征值、波长 |
| $\mu$ | `\mu` | 均值、摩擦系数 |
| $\nu$ | `\nu` | 频率 |
| $\pi$ | `\pi` | 圆周率 3.14159... |
| $\rho$ | `\rho` | 密度 |
| $\sigma$ | `\sigma` | 标准差 |
| $\tau$ | `\tau` | 时间常数 |
| $\phi$ | `\phi` | 黄金比例、角度 |
| $\psi$ | `\psi` | 波函数 |
| $\omega$ | `\omega` | 角频率 |

#### 大写希腊字母

| 符号 | 代码 | 常见用途 |
|------|------|---------|
| $\Delta$ | `\Delta` | 变化量 |
| $\Theta$ | `\Theta` | 角度 |
| $\Lambda$ | `\Lambda` | 宇宙常数 |
| $\Pi$ | `\Pi` | 乘积 |
| $\Sigma$ | `\Sigma` | 求和 |
| $\Phi$ | `\Phi` | 磁通量 |
| $\Psi$ | `\Psi` | 波函数 |
| $\Omega$ | `\Omega` | 电阻单位、立体角 |

**注意：** 大写希腊字母就是把首字母大写，比如 `\Delta`、`\Theta`。但不是所有希腊字母都有大写形式（比如 `\Alpha` 就是普通的 A）。

#### 🧠 记忆口诀

**常用希腊字母速记：**

| 字母 | 代码 | 记忆方法 |
|------|------|---------|
| $\alpha$ | `\alpha` | **阿尔法**，直接音译 |
| $\beta$ | `\beta` | **贝塔**，直接音译 |
| $\gamma$ | `\gamma` | **伽马**，直接音译 |
| $\delta$ | `\delta` | **德尔塔**，直接音译 |
| $\pi$ | `\pi` | **派**，最熟悉的圆周率 |
| $\sigma$ | `\sigma` | **西格玛**，统计学常用 |
| $\theta$ | `\theta` | **西塔**，角度常用 |
| $\lambda$ | `\lambda` | **兰姆达**，物理常用 |
| $\omega$ | `\omega` | **欧米伽**，最后一个希腊字母 |

**口诀：** "阿尔法贝塔伽马德尔塔，派西格玛西塔兰姆达欧米伽"

**大写规律：** 大写 = 首字母大写（`\Delta`、`\Theta`、`\Sigma`），像英语句子首字母大写一样。

### ✏️ 小练习

**练习 1：** 写出"圆周率 $\pi$ 约等于 3.14"

<details>
<summary>查看答案</summary>

```latex
$\pi \approx 3.14$
```

显示效果：$\pi \approx 3.14$

</details>

**练习 2：** 写出"标准差 $\sigma$ 的平方"

<details>
<summary>查看答案</summary>

```latex
$\sigma^2$
```

显示效果：$\sigma^2$

</details>

---

### 4.2 运算符

#### 基本运算符

| 符号 | 代码 | 说明 |
|------|------|------|
| $+$ | `+` | 加号 |
| $-$ | `-` | 减号 |
| $\pm$ | `\pm` | 正负号 |
| $\mp$ | `\mp` | 负正号 |
| $\times$ | `\times` | 乘号 |
| $\cdot$ | `\cdot` | 点乘 |
| $\div$ | `\div` | 除号 |
| $*$ | `*` | 星号 |

**类比：**
- `\times` = 手写体的 ×（小学用的）
- `\cdot` = 点 ·（高等数学常用，表示点乘）

#### 比较运算符

| 符号 | 代码 | 说明 |
|------|------|------|
| $=$ | `=` | 等于 |
| $\neq$ | `\neq` | 不等于 |
| $<$ | `<` | 小于 |
| $>$ | `>` | 大于 |
| $\leq$ | `\leq` | 小于等于 |
| $\geq$ | `\geq` | 大于等于 |
| $\ll$ | `\ll` | 远小于 |
| $\gg$ | `\gg` | 远大于 |
| $\approx$ | `\approx` | 约等于 |
| $\equiv$ | `\equiv` | 恒等于 |
| $\sim$ | `\sim` | 相似于 |
| $\propto$ | `\propto` | 正比于 |

**记忆技巧：**
- `le` = less or equal（小于等于）
- `ge` = greater or equal（大于等于）
- `ne` = not equal（不等于）
- `approx` = approximately（大约）

#### 🧠 记忆口诀

**比较运算符速记：**

| 符号 | 代码 | 记忆方法 |
|------|------|---------|
| $\neq$ | `\neq` | **ne** = not equal（不等于） |
| $\leq$ | `\leq` | **le** = less or equal（小于等于） |
| $\geq$ | `\geq` | **ge** = greater or equal（大于等于） |
| $\approx$ | `\approx` | **approx**imately（大约） |
| $\equiv$ | `\equiv` | **equiv**alent（等价） |
| $\sim$ | `\sim` | **sim**ilar（相似） |
| $\propto$ | `\propto` | **pro**por**t**ional（正比） |

**口诀：** "ne不等，le小ge大，approx约等equiv恒"

**运算符速记：**

| 符号 | 代码 | 记忆方法 |
|------|------|---------|
| $\pm$ | `\pm` | **p**lus **m**inus（加减） |
| $\times$ | `\times` | **times**（乘以） |
| $\div$ | `\div` | **div**ide（除以） |
| $\cdot$ | `\cdot` | **cdot** = center dot（中心点） |

**口诀：** "pm加减，times乘，div除，cdot点乘"

#### 集合运算符

| 符号 | 代码 | 说明 |
|------|------|------|
| $\in$ | `\in` | 属于 |
| $\notin$ | `\notin` | 不属于 |
| $\subset$ | `\subset` | 子集 |
| $\subseteq$ | `\subseteq` | 子集或等于 |
| $\cup$ | `\cup` | 并集 |
| $\cap$ | `\cap` | 交集 |
| $\emptyset$ | `\emptyset` | 空集 |
| $\forall$ | `\forall` | 任意 |
| $\exists$ | `\exists` | 存在 |

### ✏️ 小练习

**练习 1：** 写出"x 不等于 0"

<details>
<summary>查看答案</summary>

```latex
$x \neq 0$
```

显示效果：$x \neq 0$

</details>

**练习 2：** 写出"a 属于集合 A"

<details>
<summary>查看答案</summary>

```latex
$a \in A$
```

显示效果：$a \in A$

</details>

---

### 4.3 分数与根号

#### 分数

**类比：** 分数就像把一个东西切成几块，`\frac{分子}{分母}`。

| 效果 | 代码 | 说明 |
|------|------|------|
| $\frac{1}{2}$ | `\frac{1}{2}` | 二分之一 |
| $\frac{a}{b}$ | `\frac{a}{b}` | a 除以 b |
| $\frac{x+1}{x-1}$ | `\frac{x+1}{x-1}` | 分子分母都可以是表达式 |

**进阶用法：**

| 效果 | 代码 | 说明 |
|------|------|------|
| $\dfrac{1}{2}$ | `\dfrac{1}{2}` | 强制大号分数（行内也显示大） |
| $\tfrac{1}{2}$ | `\tfrac{1}{2}` | 强制小号分数（适合行内） |
| $\cfrac{1}{1+\cfrac{1}{2}}$ | `\cfrac{1}{1+\cfrac{1}{2}}` | 连分数 |

**类比：**
- `\frac` = 自动选择大小
- `\dfrac` = 强制大号（display）
- `\tfrac` = 强制小号（text）

#### 根号

**类比：** 根号就像开一个"盒子"，把东西装进去。

| 效果 | 代码 | 说明 |
|------|------|------|
| $\sqrt{x}$ | `\sqrt{x}` | 平方根 |
| $\sqrt[3]{x}$ | `\sqrt[3]{x}` | 立方根 |
| $\sqrt[n]{x}$ | `\sqrt[n]{x}` | n 次方根 |
| $\sqrt{x^2+y^2}$ | `\sqrt{x^2+y^2}` | 根号里可以放表达式 |

**记忆技巧：** `\sqrt` = square root（平方根），加 `[n]` 就是 n 次根。

#### 🧠 记忆口诀

**分数根号速记：**

| 结构 | 代码 | 记忆方法 |
|------|------|---------|
| 分数 | `\frac{分子}{分母}` | **frac**tion（分数） |
| 平方根 | `\sqrt{x}` | **sq**uare **r**oot（平方根） |
| n次根 | `\sqrt[n]{x}` | 加 `[n]` 指定次数 |

**口诀：** "frac分数两花括，sqrt根号后面跟"

**类比：**
- `\frac{a}{b}` = 把 a 放上面，b 放下面（像切蛋糕）
- `\sqrt{x}` = 把 x 装进根号盒子里

### ✏️ 小练习

**练习 1：** 写出"根号 2"

<details>
<summary>查看答案</summary>

```latex
$\sqrt{2}$
```

显示效果：$\sqrt{2}$

</details>

**练习 2：** 写出"三分之二"

<details>
<summary>查看答案</summary>

```latex
$\frac{2}{3}$
```

显示效果：$\frac{2}{3}$

</details>

**练习 3：** 写出"根号下 x 的平方加 y 的平方"

<details>
<summary>查看答案</summary>

```latex
$\sqrt{x^2 + y^2}$
```

显示效果：$\sqrt{x^2 + y^2}$

</details>

---

### 4.4 上标与下标

**类比：**
- 上标 = 写在右上角（像"平方""立方"）
- 下标 = 写在右下角（像脚注）

#### 基本用法

| 效果 | 代码 | 说明 |
|------|------|------|
| $x^2$ | `x^2` | x 的平方 |
| $x^n$ | `x^n` | x 的 n 次方 |
| $x_i$ | `x_i` | x 下标 i |
| $x_{ij}$ | `x_{ij}` | 下标多个字符用花括号 |
| $x^2_i$ | `x^2_i` | 同时有上标和下标 |
| $x_i^2$ | `x_i^2` | 顺序无所谓 |
| $x^{2y}$ | `x^{2y}` | 上标多个字符用花括号 |

**重要规则：**
- **单个字符**：直接写 `x^2`
- **多个字符**：必须用花括号 `x^{2y}`

**错误示例：**
- ❌ `x^2y` → 显示为 $x^2y$（只有 2 是上标）
- ✅ `x^{2y}` → 显示为 $x^{2y}$（2y 都是上标）

#### 特殊上标/下标

| 效果 | 代码 | 说明 |
|------|------|------|
| $x'$ | `x'` | 一阶导数（撇号） |
| $x''$ | `x''` | 二阶导数 |
| $\dot{x}$ | `\dot{x}` | 一阶导数（点号，牛顿记法） |
| $\ddot{x}$ | `\ddot{x}` | 二阶导数（点号） |
| $\hat{x}$ | `\hat{x}` | 估计值 |
| $\bar{x}$ | `\bar{x}` | 平均值 |
| $\vec{x}$ | `\vec{x}` | 向量 |

**类比：**
- $x'$ = "x 一撇"（拉格朗日记法，表示导数）
- $\dot{x}$ = "x 上面一点"（牛顿记法，表示对时间求导）

#### 🧠 记忆口诀

**上下标速记：**

| 结构 | 代码 | 记忆方法 |
|------|------|---------|
| 上标 | `x^2` | `^` 像向上的箭头 ↑ |
| 下标 | `x_i` | `_` 像向下的箭头 ↓ |
| 多字符上标 | `x^{2y}` | 花括号包裹多个字符 |
| 多字符下标 | `x_{ij}` | 花括号包裹多个字符 |

**口诀：** "^上_下，多个花括装"

**错误警示：**
- ❌ `x^2y` → 只有 2 是上标
- ✅ `x^{2y}` → 2y 都是上标

**记忆：** 花括号 `{}` 就像"袋子"，把多个字符装在一起变成一个整体。

### ✏️ 小练习

**练习 1：** 写出"x 下标 1 的平方"

<details>
<summary>查看答案</summary>

```latex
$x_1^2$
```

显示效果：$x_1^2$

</details>

**练习 2：** 写出"y 的 n+1 次方"

<details>
<summary>查看答案</summary>

```latex
$y^{n+1}$
```

显示效果：$y^{n+1}$

</details>

---

### 4.5 括号与定界符

**类比：** 括号就像"容器"，把东西装起来。LaTeX 会自动调整括号大小来适应内容。

#### 基本括号

| 效果 | 代码 | 说明 |
|------|------|------|
| $(x)$ | `(x)` | 小括号 |
| $[x]$ | `[x]` | 中括号 |
| $\{x\}$ | `\{x\}` | 大括号（需要转义） |

#### 自动调整大小

| 效果 | 代码 | 说明 |
|------|------|------|
| $(\frac{1}{2})$ | `(\frac{1}{2})` | 默认大小 |
| $\left(\frac{1}{2}\right)$ | `\left(\frac{1}{2}\right)` | 自动适应高度 |

**类比：**
- `\left` = 左括号开始，自动变大
- `\right` = 右括号结束，自动变大

**重要：** `\left` 和 `\right` 必须成对出现！

#### 特殊定界符

| 效果 | 代码 | 说明 |
|------|------|------|
| $\lfloor x \rfloor$ | `\lfloor x \rfloor` | 向下取整 |
| $\lceil x \rceil$ | `\lceil x \rceil` | 向上取整 |
| $\|x\|$ | `\|x\|` | 绝对值 |
| $\|x\|$ | `\|x\|` | 范数 |
| $\langle x \rangle$ | `\langle x \rangle` | 尖括号 |

### ✏️ 小练习

**练习 1：** 写出"x 的绝对值"

<details>
<summary>查看答案</summary>

```latex
$|x|$ 或 $\|x\|$
```

显示效果：$|x|$ 或 $\|x\|$

</details>

**练习 2：** 写出"根号下 a+b 的整体平方"

<details>
<summary>查看答案</summary>

```latex
$\left( \sqrt{a+b} \right)^2$
```

显示效果：$\left( \sqrt{a+b} \right)^2$

</details>

---

### 4.6 求和、积分、极限

**类比：**
- 求和 $\sum$ = 把一堆数加起来（像用计算器按 +）
- 积分 $\int$ = 求曲线下的面积（像用尺子量面积）
- 极限 $\lim$ = 看看"无限接近"时会怎样

#### 求和

| 效果 | 代码 | 说明 |
|------|------|------|
| $\sum_{i=1}^n$ | `\sum_{i=1}^n` | i 从 1 到 n |
| $\sum_{i=1}^n x_i$ | `\sum_{i=1}^n x_i` | x_i 的和 |
| $\sum_{i=1}^n i^2$ | `\sum_{i=1}^n i^2` | i 的平方的和 |

**结构：** `\sum_{下界}^{上界} 表达式`

**类比：** 就像写"从 1 加到 n"，$\sum$ 是"Σ"（希腊字母 sigma），数学里表示"求和"。

#### 积分

| 效果 | 代码 | 说明 |
|------|------|------|
| $\int$ | `\int` | 不定积分 |
| $\int_a^b$ | `\int_a^b` | 从 a 到 b 的定积分 |
| $\int_a^b f(x)dx$ | `\int_a^b f(x)dx` | 完整的定积分 |
| $\iint$ | `\iint` | 二重积分 |
| $\iiint$ | `\iiint` | 三重积分 |
| $\oint$ | `\oint` | 曲线积分 |

**结构：** `\int_{下限}^{上限} 被积函数 \, dx`

**注意：** `\,` 是一个小空格，让 dx 和被积函数分开，看起来更清楚。

#### 极限

| 效果 | 代码 | 说明 |
|------|------|------|
| $\lim_{x \to 0}$ | `\lim_{x \to 0}` | x 趋近于 0 |
| $\lim_{x \to \infty}$ | `\lim_{x \to \infty}` | x 趋近于无穷 |
| $\lim_{x \to 0} \frac{\sin x}{x}$ | `\lim_{x \to 0} \frac{\sin x}{x}` | 完整的极限表达式 |

**结构：** `\lim_{趋近条件} 表达式`

**类比：** $\lim$ 就是问"当 x 无限接近某个值时，函数会变成多少？"

#### 🧠 记忆口诀

**求和积分极限速记：**

| 结构 | 代码 | 记忆方法 |
|------|------|---------|
| 求和 | `\sum_{下}^{上}` | **sum** = 求和，$\sum$ 是希腊字母 sigma |
| 积分 | `\int_{下}^{上}` | **int**egral = 积分，$\int$ 像一条蛇 |
| 极限 | `\lim_{条件}` | **lim**it = 极限 |
| 乘积 | `\prod_{下}^{上}` | **prod**uct = 乘积，$\prod$ 是大写 pi |

**口诀：** "sum求和sigma蛇，int积分蛇弯弯，lim极限limit，prod乘积pi大"

**结构规律：** 都是 `\命令_{下界}^{上界} 表达式`

**类比：**
- $\sum$ = 把一堆数加起来（像用计算器按 +）
- $\int$ = 求曲线下的面积（像用尺子量面积）
- $\lim$ = 看看"无限接近"时会怎样
- $\prod$ = 把一堆数乘起来（像用计算器按 ×）

#### 其他常见运算

| 效果 | 代码 | 说明 |
|------|------|------|
| $\prod_{i=1}^n$ | `\prod_{i=1}^n` | 连乘 |
| $\coprod_{i=1}^n$ | `\coprod_{i=1}^n` | 副乘积 |

### ✏️ 小练习

**练习 1：** 写出"从 i=1 到 10 的 i 的和"

<details>
<summary>查看答案</summary>

```latex
$\sum_{i=1}^{10} i$
```

显示效果：$\sum_{i=1}^{10} i$

</details>

**练习 2：** 写出"x 趋近于 0 时，sin(x)/x 的极限"

<details>
<summary>查看答案</summary>

```latex
$\lim_{x \to 0} \frac{\sin x}{x}$
```

显示效果：$\lim_{x \to 0} \frac{\sin x}{x}$

</details>

**练习 3：** 写出"从 0 到 1 的 x 平方的定积分"

<details>
<summary>查看答案</summary>

```latex
$\int_0^1 x^2 \, dx$
```

显示效果：$\int_0^1 x^2 \, dx$

</details>

---

### 4.7 箭头

**类比：** 箭头就像"指向"，告诉读者"从这里到那里"。

#### 基本箭头

| 效果 | 代码 | 说明 |
|------|------|------|
| $\rightarrow$ 或 $\to$ | `\rightarrow` 或 `\to` | 右箭头 |
| $\leftarrow$ 或 $\gets$ | `\leftarrow` 或 `\gets` | 左箭头 |
| $\leftrightarrow$ | `\leftrightarrow` | 双向箭头 |
| $\Rightarrow$ | `\Rightarrow` | 双线右箭头（推出） |
| $\Leftarrow$ | `\Leftarrow` | 双线左箭头 |
| $\Leftrightarrow$ | `\Leftrightarrow` | 双线双向箭头（等价） |

#### 长箭头

| 效果 | 代码 | 说明 |
|------|------|------|
| $\longrightarrow$ | `\longrightarrow` | 长右箭头 |
| $\longleftarrow$ | `\longleftarrow` | 长左箭头 |
| $\Longrightarrow$ | `\Longrightarrow` | 长双线右箭头 |

#### 特殊箭头

| 效果 | 代码 | 说明 |
|------|------|------|
| $\mapsto$ | `\mapsto` | 映射到 |
| $\uparrow$ | `\uparrow` | 上箭头 |
| $\downarrow$ | `\downarrow` | 下箭头 |

**类比：**
- $\to$ = "变成"（单线箭头，表示过程）
- $\Rightarrow$ = "推出"（双线箭头，表示逻辑推理）
- $\Leftrightarrow$ = "等价于"（双向双线）
- $\mapsto$ = "映射到"（表示 f(x) = y 中 x 对应 y）

#### 🧠 记忆口诀

**箭头速记：**

| 符号 | 代码 | 记忆方法 |
|------|------|---------|
| $\to$ | `\to` | **to** = 到（最简单的右箭头） |
| $\gets$ | `\gets` | **get**s = 得到（左箭头） |
| $\Rightarrow$ | `\Rightarrow` | **R**ight **arrow** 大写 = 双线（推出） |
| $\Leftarrow$ | `\Leftarrow` | **L**eft **arrow** 大写 = 双线 |
| $\Leftrightarrow$ | `\Leftrightarrow` | **L**eft **R**ight **arrow** 大写 = 双向双线（等价） |
| $\mapsto$ | `\mapsto` | **map**s **to** = 映射到 |

**口诀：** "to右gets左，大写双线推出，mapsto映射到"

**单双线区别：**
- 单线 $\to$ = 过程、变化（A 变成 B）
- 双线 $\Rightarrow$ = 逻辑推理（A 推出 B）
- 双向双线 $\Leftrightarrow$ = 等价（A 等价于 B）

### ✏️ 小练习

**练习 1：** 写出"a 推出 b"

<details>
<summary>查看答案</summary>

```latex
$a \Rightarrow b$
```

显示效果：$a \Rightarrow b$

</details>

**练习 2：** 写出"x 映射到 x 的平方"

<details>
<summary>查看答案</summary>

```latex
$x \mapsto x^2$
```

显示效果：$x \mapsto x^2$

</details>

---

### 4.8 矩阵

**类比：** 矩阵就像一个"表格"，把数字按行列排列。

#### 基本语法

矩阵用 `\begin{类型}...\end{类型}` 包裹，元素之间用 `&` 分隔，行之间用 `\\` 换行。

```latex
\begin{matrix}
  a & b \\
  c & d
\end{matrix}
```

显示效果：
$$
\begin{matrix}
a & b \\
c & d
\end{matrix}
$$

#### 不同括号的矩阵

| 类型 | 代码 | 显示效果 | 说明 |
|------|------|---------|------|
| 无括号 | `\begin{matrix}...\end{matrix}` | $\begin{matrix} a & b \\ c & d \end{matrix}$ | 基础矩阵 |
| 小括号 | `\begin{pmatrix}...\end{pmatrix}` | $\begin{pmatrix} a & b \\ c & d \end{pmatrix}$ | 圆括号矩阵 |
| 中括号 | `\begin{bmatrix}...\end{bmatrix}` | $\begin{bmatrix} a & b \\ c & d \end{bmatrix}$ | 方括号矩阵 |
| 大括号 | `\begin{Bmatrix}...\end{Bmatrix}` | $\begin{Bmatrix} a & b \\ c & d \end{Bmatrix}$ | 花括号矩阵 |
| 单竖线 | `\begin{vmatrix}...\end{vmatrix}` | $\begin{vmatrix} a & b \\ c & d \end{vmatrix}$ | 行列式 |
| 双竖线 | `\begin{Vmatrix}...\end{Vmatrix}` | $\begin{Vmatrix} a & b \\ c & d \end{Vmatrix}$ | 范数 |

#### 示例

**2×2 矩阵：**
```latex
\begin{pmatrix}
  1 & 2 \\
  3 & 4
\end{pmatrix}
```

显示效果：
$$
\begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}
$$

**3×3 矩阵：**
```latex
\begin{bmatrix}
  a_{11} & a_{12} & a_{13} \\
  a_{21} & a_{22} & a_{23} \\
  a_{31} & a_{32} & a_{33}
\end{bmatrix}
```

显示效果：
$$
\begin{bmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{bmatrix}
$$

**带省略号的矩阵：**
```latex
\begin{pmatrix}
  a_{11} & a_{12} & \cdots & a_{1n} \\
  a_{21} & a_{22} & \cdots & a_{2n} \\
  \vdots & \vdots & \ddots & \vdots \\
  a_{n1} & a_{n2} & \cdots & a_{nn}
\end{pmatrix}
```

显示效果：
$$
\begin{pmatrix}
a_{11} & a_{12} & \cdots & a_{1n} \\
a_{21} & a_{22} & \cdots & a_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n1} & a_{n2} & \cdots & a_{nn}
\end{pmatrix}
$$

**省略号说明：**
| 符号 | 代码 | 方向 |
|------|------|------|
| $\cdots$ | `\cdots` | 水平省略（横着的点） |
| $\vdots$ | `\vdots` | 垂直省略（竖着的点） |
| $\ddots$ | `\ddots` | 对角线省略（斜着的点） |

#### 条件表达式（cases）

**类比：** 条件表达式就像"如果...那么..."的数学写法。

```latex
f(x) = \begin{cases}
  x^2 & \text{if } x \geq 0 \\
  -x  & \text{if } x < 0
\end{cases}
```

显示效果：
$$
f(x) = \begin{cases}
x^2 & \text{if } x \geq 0 \\
-x  & \text{if } x < 0
\end{cases}
$$

**注意：** `\text{}` 用来在里面写普通文字（不会变成斜体）。

#### 🧠 记忆口诀

**矩阵速记：**

| 类型 | 代码 | 记忆方法 |
|------|------|---------|
| 无括号 | `\begin{matrix}` | **matrix** = 矩阵（基础款） |
| 小括号 | `\begin{pmatrix}` | **p**arentheses matrix（圆括号矩阵） |
| 中括号 | `\begin{bmatrix}` | **b**racket matrix（方括号矩阵） |
| 大括号 | `\begin{Bmatrix}` | **B**ig brace matrix（花括号矩阵） |
| 行列式 | `\begin{vmatrix}` | **v**ertical bar matrix（竖线矩阵） |
| 范数 | `\begin{Vmatrix}` | **V**ertical bar matrix（双竖线矩阵） |
| 条件 | `\begin{cases}` | **cases** = 情况（条件表达式） |

**口诀：** "matrix基础款，p圆b方B花，v单V双cases条件"

**省略号速记：**

| 符号 | 代码 | 方向 | 记忆方法 |
|------|------|------|---------|
| $\cdots$ | `\cdots` | 水平 | **c**enter **dots**（中心点，横着） |
| $\vdots$ | `\vdots` | 垂直 | **v**ertical **dots**（垂直点，竖着） |
| $\ddots$ | `\ddots` | 对角线 | **d**iagonal **dots**（对角线点，斜着） |

**口诀：** "cdots横，vdots竖，ddots斜对角"

### ✏️ 小练习

**练习 1：** 写出一个 2×2 的单位矩阵（对角线是 1，其他是 0）

<details>
<summary>查看答案</summary>

```latex
\begin{pmatrix}
  1 & 0 \\
  0 & 1
\end{pmatrix}
```

显示效果：
$$
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

</details>

**练习 2：** 写出绝对值的定义

<details>
<summary>查看答案</summary>

```latex
|x| = \begin{cases}
  x  & \text{if } x \geq 0 \\
  -x & \text{if } x < 0
\end{cases}
```

显示效果：
$$
|x| = \begin{cases}
x  & \text{if } x \geq 0 \\
-x & \text{if } x < 0
\end{cases}
$$

</details>

---

## 5. 完整工作流程

从"我想写一个公式"到"公式显示出来"的完整流程：

```
┌─────────────────────────────────────────────────────────┐
│  1. 确定你要写什么公式                                      │
│     例如：x 的平方加 y 的平方等于 z 的平方                    │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  2. 拆解公式结构                                           │
│     - 变量：x, y, z                                       │
│     - 运算：加法 +, 等于 =                                 │
│     - 上标：平方 ^2                                       │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  3. 转换成 LaTeX 代码                                      │
│     $x^2 + y^2 = z^2$                                    │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  4. 输入到支持 LaTeX 的地方                                 │
│     - Markdown 编辑器（Typora、Obsidian 等）               │
│     - Word（插入 → 公式）                                  │
│     - 网页（MathJax、KaTeX）                               │
│     - LaTeX 编辑器（Overleaf）                             │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  5. 查看渲染效果                                           │
│     显示：x² + y² = z²                                    │
└─────────────────────────────────────────────────────────┘
```

### 常用工具推荐

| 工具 | 用途 | 特点 |
|------|------|------|
| **Typora** | Markdown 编辑器 | 所见即所得，支持 LaTeX |
| **Obsidian** | 笔记软件 | 支持 LaTeX，适合知识管理 |
| **Overleaf** | 在线 LaTeX 编辑器 | 专业写论文，实时预览 |
| **Mathpix** | 公式识别 | 拍照识别公式，转成 LaTeX |
| **Detexify** | 符号查找 | 手画符号，告诉你代码 |

---

## 6. 公式组装：从简单到复杂

> 复杂公式 = 简单公式的组合。学会拆解，就能写出任何公式。

### 6.1 公式组装的基本思路

**类比：** 写公式就像搭积木——先有小块，再拼成大块。

```
┌─────────────────────────────────────────────────────────┐
│  1. 识别公式中的"积木块"                                   │
│     - 变量：x, y, z                                       │
│     - 运算：+, -, ×, ÷                                    │
│     - 结构：分数、根号、上下标                               │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  2. 先写最简单的部分                                       │
│     例如：先写 x^2                                        │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  3. 逐步添加复杂结构                                       │
│     - 加分数：\frac{x^2}{y}                               │
│     - 加根号：\sqrt{\frac{x^2}{y}}                        │
│     - 加上下标：\sqrt{\frac{x^2_1}{y_2}}                  │
└─────────────────────────────────────────────────────────┘
                           ↓
┌─────────────────────────────────────────────────────────┐
│  4. 检查配对和完整性                                        │
│     - 花括号是否配对？                                      │
│     - 上下标是否正确？                                      │
└─────────────────────────────────────────────────────────┘
```

### 6.2 实战拆解：二次方程求根公式

**目标公式：** $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$

**拆解步骤：**

| 步骤 | 操作 | 代码 | 显示效果 |
|------|------|------|---------|
| 1 | 写变量 x 等于 | `x =` | $x =$ |
| 2 | 写分数结构 | `\frac{}{2a}` | $\frac{}{2a}$ |
| 3 | 写分子：-b ± 根号 | `\frac{-b \pm \sqrt{}}{2a}` | $\frac{-b \pm \sqrt{}}{2a}$ |
| 4 | 写根号内容：b²-4ac | `\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}` | $\frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ |

**完整代码：**
```latex
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
```

### 6.3 实战拆解：正态分布公式

**目标公式：** $f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

**拆解步骤：**

| 步骤 | 操作 | 代码 | 显示效果 |
|------|------|------|---------|
| 1 | 写 f(x) = | `f(x) =` | $f(x) =$ |
| 2 | 写前面的分数 | `\frac{1}{\sigma\sqrt{2\pi}}` | $\frac{1}{\sigma\sqrt{2\pi}}$ |
| 3 | 写 e 的指数 | `e^{-\frac{(x-\mu)^2}{2\sigma^2}}` | $e^{-\frac{(x-\mu)^2}{2\sigma^2}}$ |
| 4 | 组合起来 | 完整代码 | 完整公式 |

**完整代码：**
```latex
f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
```

**拆解要点：**
- `\frac{1}{\sigma\sqrt{2\pi}}` = 前面的系数（分数 + 根号）
- `e^{...}` = 指数函数
- `-\frac{(x-\mu)^2}{2\sigma^2}` = 指数部分（负号 + 分数）

### 6.4 实战拆解：矩阵运算

**目标公式：** $A \mathbf{x} = \mathbf{b}$，其中 $A = \begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix}$

**拆解步骤：**

| 步骤 | 操作 | 代码 | 显示效果 |
|------|------|------|---------|
| 1 | 写 A x = b | `A \mathbf{x} = \mathbf{b}` | $A \mathbf{x} = \mathbf{b}$ |
| 2 | 写矩阵 | `\begin{pmatrix}...\end{pmatrix}` | 矩阵 |
| 3 | 写矩阵元素 | `a_{11} & a_{12} \\ a_{21} & a_{22}` | 元素 |

**完整代码：**
```latex
A = \begin{pmatrix}
  a_{11} & a_{12} \\
  a_{21} & a_{22}
\end{pmatrix}
```

**显示效果：**
$$
A = \begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix}
$$

**要点：**
- `\mathbf{x}` = 粗体向量（不是斜体）
- `a_{11}` = 下标 11（用花括号包裹多个字符）
- `&` = 列分隔符
- `\\` = 换行符

### 6.5 实战拆解：多行对齐公式

**目标：** 推导过程的多行对齐显示

**目标效果：**
$$
\begin{aligned}
(a+b)^2 &= (a+b)(a+b) \\
        &= a^2 + ab + ba + b^2 \\
        &= a^2 + 2ab + b^2
\end{aligned}
$$

**拆解步骤：**

| 步骤 | 操作 | 代码 |
|------|------|------|
| 1 | 开始 aligned 环境 | `\begin{aligned}` |
| 2 | 第一行，等号前加 & | `(a+b)^2 &= (a+b)(a+b) \\` |
| 3 | 第二行，等号对齐 | `&= a^2 + ab + ba + b^2 \\` |
| 4 | 第三行 | `&= a^2 + 2ab + b^2` |
| 5 | 结束环境 | `\end{aligned}` |

**完整代码：**
```latex
\begin{aligned}
  (a+b)^2 &= (a+b)(a+b) \\
          &= a^2 + ab + ba + b^2 \\
          &= a^2 + 2ab + b^2
\end{aligned}
```

**要点：**
- `&` 是对齐点，放在等号前面
- `\\` 是换行符
- 缩进只是为了可读性，不影响显示

### 6.6 组装技巧总结

| 技巧 | 说明 | 示例 |
|------|------|------|
| **由内向外** | 先写最里面的部分，再包外层 | 先写 `x^2`，再写 `\sqrt{x^2}` |
| **先结构后内容** | 先写框架，再填内容 | 先写 `\frac{}{}`，再填分子分母 |
| **善用占位符** | 用 `?` 先占位，最后替换 | `\frac{?}{?}` → `\frac{a}{b}` |
| **检查配对** | 每个 `{` 都要有 `}` | 用编辑器的括号匹配功能 |

### ✏️ 组装练习

**练习 1：** 组装公式 $\sum_{i=1}^{n} \frac{x_i - \bar{x}}{n-1}$

<details>
<summary>查看答案</summary>

**拆解步骤：**
1. 先写求和：`\sum_{i=1}^{n}`
2. 再写分数：`\frac{x_i - \bar{x}}{n-1}`
3. 组合：`\sum_{i=1}^{n} \frac{x_i - \bar{x}}{n-1}`

**完整代码：**
```latex
$\sum_{i=1}^{n} \frac{x_i - \bar{x}}{n-1}$
```

</details>

**练习 2：** 组装公式 $\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$

<details>
<summary>查看答案</summary>

**拆解步骤：**
1. 先写积分：`\int_{-\infty}^{\infty}`
2. 再写被积函数：`e^{-x^2} dx`
3. 写等号和结果：`= \sqrt{\pi}`
4. 组合：`\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}`

**完整代码：**
```latex
$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$
```

</details>

**练习 3：** 组装公式 $\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e$

<details>
<summary>查看答案</summary>

**拆解步骤：**
1. 先写极限：`\lim_{n \to \infty}`
2. 写括号部分：`\left(1 + \frac{1}{n}\right)^n`
3. 写等号和结果：`= e`
4. 组合：`\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e`

**完整代码：**
```latex
$\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e$
```

**要点：**
- `\left(` 和 `\right)` 让括号自动适应高度
- `^n` 在 `\right)` 后面，表示整个括号的 n 次方

</details>

---

## 7. 实际使用场景

### 7.1 数学基础

#### 场景 1：数学作业/论文

**需求：** 写出二次方程的求根公式

**LaTeX 代码：**
```latex
x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}
```

**显示效果：**
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**解析：**
- `\frac{分子}{分母}` = 分数
- `\pm` = 正负号
- `\sqrt{}` = 根号
- `b^2 - 4ac` = 判别式

---

#### 场景 2：Markdown 笔记

**需求：** 记录概率论中的贝叶斯公式

**LaTeX 代码：**
```latex
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
```

**显示效果：**
$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

**解析：**
- `P(A|B)` = 在 B 发生的条件下 A 发生的概率
- `\cdot` = 点乘（表示乘法）
- 分子分母结构清晰

---

### 7.2 物理学

#### 场景 3：物理公式

**需求：** 写出爱因斯坦的质能方程

**LaTeX 代码：**
```latex
E = mc^2
```

**显示效果：**
$$E = mc^2$$

**需求：** 写出薛定谔方程

**LaTeX 代码：**
```latex
i\hbar\frac{\partial}{\partial t}\Psi = \hat{H}\Psi
```

**显示效果：**
$$i\hbar\frac{\partial}{\partial t}\Psi = \hat{H}\Psi$$

**解析：**
- `i` = 虚数单位
- `\hbar` = 约化普朗克常数
- `\frac{\partial}{\partial t}` = 对时间的偏导数
- `\Psi` = 波函数（大写希腊字母）
- `\hat{H}` = 哈密顿算符（帽子表示算符）

---

### 7.3 数据科学与机器学习

#### 场景 4：机器学习/数据科学

**需求：** 写出线性回归的损失函数（均方误差）

**LaTeX 代码：**
```latex
L(\theta) = \frac{1}{2n}\sum_{i=1}^{n}(h_\theta(x^{(i)}) - y^{(i)})^2
```

**显示效果：**
$$L(\theta) = \frac{1}{2n}\sum_{i=1}^{n}(h_\theta(x^{(i)}) - y^{(i)})^2$$

**解析：**
- `L(\theta)` = 损失函数，参数是 $\theta$
- `\frac{1}{2n}` = 分数
- `\sum_{i=1}^{n}` = 从 i=1 到 n 求和
- `h_\theta(x^{(i)})` = 假设函数
- `(x^{(i)})` = 第 i 个样本（上标用花括号）
- `y^{(i)}` = 第 i 个标签

---

#### 场景 5：深度学习

**需求：** 写出 Softmax 函数

**LaTeX 代码：**
```latex
\text{Softmax}(z_i) = \frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}}
```

**显示效果：**
$$\text{Softmax}(z_i) = \frac{e^{z_i}}{\sum_{j=1}^{K} e^{z_j}}$$

**解析：**
- `\text{Softmax}` = 普通文字（不会变成斜体）
- `e^{z_i}` = e 的 z_i 次方
- `\sum_{j=1}^{K}` = 从 j=1 到 K 求和

---

#### 场景 6：物理学 — 力学

**需求：** 写出牛顿第二定律

**LaTeX 代码：**
```latex
\vec{F} = m\vec{a}
```

**显示效果：**
$$\vec{F} = m\vec{a}$$

**解析：**
- `\vec{F}` = 向量 F（力是矢量）
- `m` = 质量
- `\vec{a}` = 向量 a（加速度是矢量）

---

**需求：** 写出万有引力定律

**LaTeX 代码：**
```latex
F = G\frac{m_1 m_2}{r^2}
```

**显示效果：**
$$F = G\frac{m_1 m_2}{r^2}$$

**解析：**
- `G` = 引力常数
- `\frac{m_1 m_2}{r^2}` = 分数（两质量乘积除以距离平方）
- `m_1`、`m_2` = 下标表示不同物体

---

**需求：** 写出动能公式

**LaTeX 代码：**
```latex
E_k = \frac{1}{2}mv^2
```

**显示效果：**
$$E_k = \frac{1}{2}mv^2$$

**解析：**
- `E_k` = 动能（E 下标 k）
- `\frac{1}{2}` = 二分之一
- `mv^2` = 质量乘以速度的平方

---

#### 场景 7：物理学 — 电磁学

**需求：** 写出库仑定律

**LaTeX 代码：**
```latex
F = k\frac{q_1 q_2}{r^2}
```

**显示效果：**
$$F = k\frac{q_1 q_2}{r^2}$$

**需求：** 写出麦克斯韦方程组（散度形式）

**LaTeX 代码：**
```latex
\begin{aligned}
  \nabla \cdot \vec{E} &= \frac{\rho}{\epsilon_0} \\
  \nabla \cdot \vec{B} &= 0 \\
  \nabla \times \vec{E} &= -\frac{\partial \vec{B}}{\partial t} \\
  \nabla \times \vec{B} &= \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}
\end{aligned}
```

**显示效果：**
$$
\begin{aligned}
\nabla \cdot \vec{E} &= \frac{\rho}{\epsilon_0} \\
\nabla \cdot \vec{B} &= 0 \\
\nabla \times \vec{E} &= -\frac{\partial \vec{B}}{\partial t} \\
\nabla \times \vec{B} &= \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial \vec{E}}{\partial t}
\end{aligned}
$$

**解析：**
- `\nabla` = 纳布拉算子（梯度、散度、旋度）
- `\cdot` = 点乘（散度）
- `\times` = 叉乘（旋度）
- `\epsilon_0` = 真空介电常数
- `\mu_0` = 真空磁导率
- `\frac{\partial}{\partial t}` = 对时间的偏导数

---

#### 场景 8：物理学 — 量子力学

**需求：** 写出海森堡不确定性原理

**LaTeX 代码：**
```latex
\Delta x \cdot \Delta p \geq \frac{\hbar}{2}
```

**显示效果：**
$$\Delta x \cdot \Delta p \geq \frac{\hbar}{2}$$

**解析：**
- `\Delta x` = 位置的不确定度
- `\Delta p` = 动量的不确定度
- `\hbar` = 约化普朗克常数
- `\geq` = 大于等于

---

**需求：** 写出薛定谔方程（含时形式）

**LaTeX 代码：**
```latex
i\hbar\frac{\partial}{\partial t}\Psi(\vec{r},t) = \hat{H}\Psi(\vec{r},t)
```

**显示效果：**
$$i\hbar\frac{\partial}{\partial t}\Psi(\vec{r},t) = \hat{H}\Psi(\vec{r},t)$$

**解析：**
- `i` = 虚数单位
- `\Psi(\vec{r},t)` = 波函数（依赖位置和时间）
- `\hat{H}` = 哈密顿算符（帽子表示算符）

---

### 7.4 化学与经济学

#### 场景 9：化学

**需求：** 写出化学反应方程式

**LaTeX 代码：**
```latex
\text{2H}_2 + \text{O}_2 \rightarrow \text{2H}_2\text{O}
```

**显示效果：**
$$\text{2H}_2 + \text{O}_2 \rightarrow \text{2H}_2\text{O}$$

**解析：**
- `\text{2H}_2` = 2个氢分子（下标 2 表示双原子）
- `\rightarrow` = 反应箭头
- `\text{2H}_2\text{O}` = 2个水分子

**技巧：** 化学式用 `\text{}` 包裹，避免字母变成斜体变量。

---

**需求：** 写出理想气体状态方程

**LaTeX 代码：**
```latex
PV = nRT
```

**显示效果：**
$$PV = nRT$$

**需求：** 写出阿伦尼乌斯方程（反应速率常数）

**LaTeX 代码：**
```latex
k = A e^{-\frac{E_a}{RT}}
```

**显示效果：**
$$k = A e^{-\frac{E_a}{RT}}$$

**解析：**
- `k` = 反应速率常数
- `A` = 指前因子
- `E_a` = 活化能（E 下标 a）
- `R` = 气体常数
- `T` = 温度

---

#### 场景 10：经济学

**需求：** 写出复利公式

**LaTeX 代码：**
```latex
A = P\left(1 + \frac{r}{n}\right)^{nt}
```

**显示效果：**
$$A = P\left(1 + \frac{r}{n}\right)^{nt}$$

**解析：**
- `A` = 最终金额
- `P` = 本金
- `r` = 年利率
- `n` = 每年复利次数
- `t` = 年数
- `\left(` 和 `\right)` = 自动调整大小的括号

---

**需求：** 写出边际成本函数

**LaTeX 代码：**
```latex
MC(q) = \frac{dC(q)}{dq}
```

**显示效果：**
$$MC(q) = \frac{dC(q)}{dq}$$

**解析：**
- `MC(q)` = 边际成本（Marginal Cost）
- `C(q)` = 总成本函数
- `\frac{dC(q)}{dq}` = 对产量 q 求导

---

**需求：** 写出消费者剩余

**LaTeX 代码：**
```latex
CS = \int_0^{Q^*} D(q) \, dq - P^* Q^*
```

**显示效果：**
$$CS = \int_0^{Q^*} D(q) \, dq - P^* Q^*$$

**解析：**
- `CS` = 消费者剩余（Consumer Surplus）
- `Q^*` = 均衡数量（星号表示均衡）
- `D(q)` = 需求函数
- `P^*` = 均衡价格

---

### 7.5 概率统计与线性代数

#### 场景 11：概率论与统计

**需求：** 写出贝叶斯定理

**LaTeX 代码：**
```latex
P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}
```

**显示效果：**
$$P(A|B) = \frac{P(B|A) \cdot P(A)}{P(B)}$$

---

**需求：** 写出正态分布的概率密度函数

**LaTeX 代码：**
```latex
f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}
```

**显示效果：**
$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$

**解析：**
- `\mu` = 均值
- `\sigma` = 标准差
- `\sigma^2` = 方差
- `e^{...}` = 指数函数

---

**需求：** 写出期望和方差公式

**LaTeX 代码：**
```latex
\begin{aligned}
  E[X] &= \sum_{i=1}^{n} x_i p_i \\
  \text{Var}(X) &= E[(X - \mu)^2] = E[X^2] - (E[X])^2
\end{aligned}
```

**显示效果：**
$$
\begin{aligned}
E[X] &= \sum_{i=1}^{n} x_i p_i \\
\text{Var}(X) &= E[(X - \mu)^2] = E[X^2] - (E[X])^2
\end{aligned}
$$

**解析：**
- `E[X]` = 期望
- `\text{Var}(X)` = 方差（用 `\text{}` 包裹函数名）
- `\sum_{i=1}^{n}` = 求和
- `p_i` = 概率

---

#### 场景 12：线性代数

**需求：** 写出矩阵乘法

**LaTeX 代码：**
```latex
C_{ij} = \sum_{k=1}^{n} A_{ik} B_{kj}
```

**显示效果：**
$$C_{ij} = \sum_{k=1}^{n} A_{ik} B_{kj}$$

**解析：**
- `C_{ij}` = 矩阵 C 的第 i 行第 j 列元素
- `A_{ik}` = 矩阵 A 的第 i 行第 k 列元素
- `B_{kj}` = 矩阵 B 的第 k 行第 j 列元素

---

**需求：** 写出特征值和特征向量

**LaTeX 代码：**
```latex
A\vec{v} = \lambda\vec{v}
```

**显示效果：**
$$A\vec{v} = \lambda\vec{v}$$

**解析：**
- `A` = 矩阵
- `\vec{v}` = 特征向量
- `\lambda` = 特征值

---

**需求：** 写出矩阵的行列式

**LaTeX 代码：**
```latex
\det(A) = \begin{vmatrix}
  a_{11} & a_{12} & a_{13} \\
  a_{21} & a_{22} & a_{23} \\
  a_{31} & a_{32} & a_{33}
\end{vmatrix}
```

**显示效果：**
$$
\det(A) = \begin{vmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{vmatrix}
$$

**解析：**
- `\det(A)` = 矩阵 A 的行列式
- `\begin{vmatrix}...\end{vmatrix}` = 行列式（单竖线矩阵）

---

### 7.6 微积分

#### 场景 13：微积分

**需求：** 写出链式法则

**LaTeX 代码：**
```latex
\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}
```

**显示效果：**
$$\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx}$$

---

**需求：** 写出泰勒展开

**LaTeX 代码：**
```latex
f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n
```

**显示效果：**
$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x-a)^n$$

**解析：**
- `f^{(n)}(a)` = f 在 a 点的 n 阶导数
- `n!` = n 的阶乘
- `(x-a)^n` = (x-a) 的 n 次方

---

**需求：** 写出格林公式

**LaTeX 代码：**
```latex
\oint_C (L\,dx + M\,dy) = \iint_D \left(\frac{\partial M}{\partial x} - \frac{\partial L}{\partial y}\right) dx\,dy
```

**显示效果：**
$$\oint_C (L\,dx + M\,dy) = \iint_D \left(\frac{\partial M}{\partial x} - \frac{\partial L}{\partial y}\right) dx\,dy$$

**解析：**
- `\oint_C` = 沿闭合曲线 C 的积分
- `\iint_D` = 在区域 D 上的二重积分
- `\frac{\partial M}{\partial x}` = 偏导数

---

## 8. 常见问题

### Q1：行内公式和行间公式有什么区别？

**A：**
- **行内公式** `$...$`：在文字中间，高度会被压缩
- **行间公式** `$$...$$`：独占一行，显示完整高度

**示例：**
- 行内：$\sum_{i=1}^n x_i$（上下标在旁边）
- 行间：
$$\sum_{i=1}^n x_i$$
（上下标在正上方正下方）

**建议：** 复杂公式（有求和、积分、矩阵）用行间公式，简单的用行内。

---

### Q2：为什么我的公式不显示？

**A：** 检查以下几点：

1. **是否在数学模式里？** 公式必须在 `$...$` 或 `$$...$$` 里面
2. **花括号是否配对？** 每个 `{` 都要有对应的 `}`
3. **命令拼写是否正确？** `\sqr` 不行，要 `\sqrt`
4. **特殊字符是否转义？** 显示 `{` 要用 `\{`

---

### Q3：怎么在公式里写中文？

**A：** 用 `\text{}` 包裹中文：

```latex
$\text{速度} = \frac{\text{距离}}{\text{时间}}$
```

显示效果：$\text{速度} = \frac{\text{距离}}{\text{时间}}$

---

### Q4：怎么调整公式的大小？

**A：** 一般不需要手动调整。如果确实需要：

- `\displaystyle`：强制大号（行内公式用）
- `\textstyle`：强制小号
- `\scriptstyle`：更小
- `\scriptscriptstyle`：最小

**示例：**
```latex
行内：$\sum_{i=1}^n x_i$
强制大号：$\displaystyle\sum_{i=1}^n x_i$
```

---

### Q5：怎么对齐多个公式？

**A：** 使用 `aligned` 环境：

```latex
\begin{aligned}
  a &= b + c \\
  d &= e + f + g \\
  h &= i
\end{aligned}
```

显示效果：
$$
\begin{aligned}
a &= b + c \\
d &= e + f + g \\
h &= i
\end{aligned}
$$

**说明：** `&` 是对齐点（通常放在等号前面），`\\` 是换行。

---

### Q6：`\times` 和 `\cdot` 有什么区别？

**A：**
- $\times$（`\times`）= 手写体的乘号，小学常用
- $\cdot$（`\cdot`）= 点乘，高等数学常用

**类比：**
- `3 × 4 = 12`（小学写法）
- $\vec{a} \cdot \vec{b}$（向量点乘）

---

### Q7：怎么写多行公式？

**A：** 使用 `aligned` 或 `cases`：

**多行对齐公式：**
```latex
\begin{aligned}
  f(x) &= x^2 + 2x + 1 \\
       &= (x+1)^2
\end{aligned}
```

显示效果：
$$
\begin{aligned}
f(x) &= x^2 + 2x + 1 \\
     &= (x+1)^2
\end{aligned}
$$

**条件表达式：**
```latex
|x| = \begin{cases}
  x  & x \geq 0 \\
  -x & x < 0
\end{cases}
```

显示效果：
$$
|x| = \begin{cases}
x  & x \geq 0 \\
-x & x < 0
\end{cases}
$$

---

### Q8：常用的数学函数怎么写？

**A：** 用反斜杠命令：

| 函数 | 代码 | 显示 |
|------|------|------|
| sin | `\sin` | $\sin$ |
| cos | `\cos` | $\cos$ |
| tan | `\tan` | $\tan$ |
| log | `\log` | $\log$ |
| ln | `\ln` | $\ln$ |
| exp | `\exp` | $\exp$ |
| lim | `\lim` | $\lim$ |
| max | `\max` | $\max$ |
| min | `\min` | $\min$ |

**注意：** 这些命令会让函数名显示为正体（不是斜体），符合数学排版规范。

---

### Q9：怎么在 Word 里用 LaTeX？

**A：** Word 支持 LaTeX 语法：

1. 打开 Word
2. 插入 → 公式（或按 `Alt + =`）
3. 在公式编辑器中选择"LaTeX"模式
4. 输入 LaTeX 代码

**注意：** Word 对 LaTeX 的支持有限，复杂的公式可能需要 MathType。

---

### Q10：有没有快速查找符号的方法？

**A：** 有！

1. **Detexify**（https://detexify.kirelabs.org）
   - 手画符号，它告诉你代码

2. **LaTeX Symbol Search**
   - 网站搜索符号

3. **速查表**
   - 见本文第 9 节

---

## 9. 快速参考卡片

### 9.1 希腊字母速查

| 小写 | 代码 | 大写 | 代码 |
|------|------|------|------|
| $\alpha$ | `\alpha` | $A$ | `A` |
| $\beta$ | `\beta` | $B$ | `B` |
| $\gamma$ | `\gamma` | $\Gamma$ | `\Gamma` |
| $\delta$ | `\delta` | $\Delta$ | `\Delta` |
| $\epsilon$ | `\epsilon` | $E$ | `E` |
| $\zeta$ | `\zeta` | $Z$ | `Z` |
| $\eta$ | `\eta` | $H$ | `H` |
| $\theta$ | `\theta` | $\Theta$ | `\Theta` |
| $\iota$ | `\iota` | $I$ | `I` |
| $\kappa$ | `\kappa` | $K$ | `K` |
| $\lambda$ | `\lambda` | $\Lambda$ | `\Lambda` |
| $\mu$ | `\mu` | $M$ | `M` |
| $\nu$ | `\nu` | $N$ | `N` |
| $\xi$ | `\xi` | $\Xi$ | `\Xi` |
| $\pi$ | `\pi` | $\Pi$ | `\Pi` |
| $\rho$ | `\rho` | $P$ | `P` |
| $\sigma$ | `\sigma` | $\Sigma$ | `\Sigma` |
| $\tau$ | `\tau` | $T$ | `T` |
| $\upsilon$ | `\upsilon` | $\Upsilon$ | `\Upsilon` |
| $\phi$ | `\phi` | $\Phi$ | `\Phi` |
| $\chi$ | `\chi` | $X$ | `X` |
| $\psi$ | `\psi` | $\Psi$ | `\Psi` |
| $\omega$ | `\omega` | $\Omega$ | `\Omega` |

### 9.2 运算符速查

| 符号 | 代码 | 符号 | 代码 |
|------|------|------|------|
| $\pm$ | `\pm` | $\mp$ | `\mp` |
| $\times$ | `\times` | $\cdot$ | `\cdot` |
| $\div$ | `\div` | $\neq$ | `\neq` |
| $\leq$ | `\leq` | $\geq$ | `\geq` |
| $\ll$ | `\ll` | $\gg$ | `\gg` |
| $\approx$ | `\approx` | $\equiv$ | `\equiv` |
| $\sim$ | `\sim` | $\propto$ | `\propto` |
| $\in$ | `\in` | $\notin$ | `\notin` |
| $\subset$ | `\subset` | $\subseteq$ | `\subseteq` |
| $\cup$ | `\cup` | $\cap$ | `\cap` |
| $\emptyset$ | `\emptyset` | $\forall$ | `\forall` |
| $\exists$ | `\exists` | $\infty$ | `\infty` |

### 9.3 箭头速查

| 符号 | 代码 | 符号 | 代码 |
|------|------|------|------|
| $\to$ | `\to` | $\gets$ | `\gets` |
| $\rightarrow$ | `\rightarrow` | $\leftarrow$ | `\leftarrow` |
| $\Rightarrow$ | `\Rightarrow` | $\Leftarrow$ | `\Leftarrow` |
| $\leftrightarrow$ | `\leftrightarrow` | $\Leftrightarrow$ | `\Leftrightarrow` |
| $\longrightarrow$ | `\longrightarrow` | $\longleftarrow$ | `\longleftarrow` |
| $\mapsto$ | `\mapsto` | $\uparrow$ | `\uparrow` |
| $\downarrow$ | `\downarrow` | | |

### 9.4 结构速查

| 结构 | 代码 | 示例 |
|------|------|------|
| 上标 | `^` | `x^2` → $x^2$ |
| 下标 | `_` | `x_i` → $x_i$ |
| 分数 | `\frac{}{}` | `\frac{a}{b}` → $\frac{a}{b}$ |
| 根号 | `\sqrt{}` | `\sqrt{x}` → $\sqrt{x}$ |
| n次根 | `\sqrt[n]{}` | `\sqrt[3]{x}` → $\sqrt[3]{x}$ |
| 求和 | `\sum_{下}^{上}` | `\sum_{i=1}^n` → $\sum_{i=1}^n$ |
| 积分 | `\int_{下}^{上}` | `\int_0^1` → $\int_0^1$ |
| 极限 | `\lim_{条件}` | `\lim_{x\to 0}` → $\lim_{x\to 0}$ |
| 乘积 | `\prod_{下}^{上}` | `\prod_{i=1}^n` → $\prod_{i=1}^n$ |

### 9.5 括号速查

| 类型 | 代码 | 自动调整 |
|------|------|---------|
| 小括号 | `( )` | `\left( \right)` |
| 中括号 | `[ ]` | `\left[ \right]` |
| 大括号 | `\{ \}` | `\left\{ \right\}` |
| 绝对值 | `\| \|` | `\left| \right|` |
| 范数 | `\| \|` | `\left\| \right\|` |
| 向下取整 | `\lfloor \rfloor` | `\left\lfloor \right\rfloor` |
| 向上取整 | `\lceil \rceil` | `\left\lceil \right\rceil` |
| 尖括号 | `\langle \rangle` | `\left\langle \right\rangle` |

### 9.6 矩阵速查

| 类型 | 开始 | 结束 |
|------|------|------|
| 无括号 | `\begin{matrix}` | `\end{matrix}` |
| 小括号 | `\begin{pmatrix}` | `\end{pmatrix}` |
| 中括号 | `\begin{bmatrix}` | `\end{bmatrix}` |
| 大括号 | `\begin{Bmatrix}` | `\end{Bmatrix}` |
| 行列式 | `\begin{vmatrix}` | `\end{vmatrix}` |
| 范数 | `\begin{Vmatrix}` | `\end{Vmatrix}` |
| 条件 | `\begin{cases}` | `\end{cases}` |

---

## 📝 总结

### 核心要点

1. **数学模式**：公式必须在 `$...$` 或 `$$...$$` 里
2. **花括号分组**：多个字符作为整体时，用 `{}` 包裹
3. **命令以 `\` 开头**：所有 LaTeX 命令都以反斜杠开始
4. **自动调整**：用 `\left...\right` 让括号自动适应高度

### 学习建议

1. **从简单的开始**：先掌握 `x^2`、`\frac{a}{b}`、`\sqrt{x}`
2. **多写多练**：看到数学公式就想想怎么用 LaTeX 写
3. **善用工具**：Detexify 查符号，Overleaf 写论文
4. **不要死记**：常用的自然记住，不常用的查速查表

### 最后的话

LaTeX 公式语法就像学骑自行车——刚开始会觉得难，但一旦学会就忘不掉。现在你已经掌握了最核心的 80% 的语法，足以应对大部分公式需求。

剩下的 20%？遇到的时候再查就好了。🚀

---

*本教程生成于 2026 年 6 月 15 日*

---

## 附录：记忆口诀大全

> 把所有口诀集中在一起，方便快速查阅。

### 1. 希腊字母口诀

**常用字母速记：**
```
阿尔法贝塔伽马德尔塔
派西格玛西塔兰姆达欧米伽
```

**对应：** α β γ δ π σ θ λ ω

**大写规律：** 首字母大写（`\Delta`、`\Theta`、`\Sigma`）

---

### 2. 运算符口诀

**比较运算符：**
```
ne不等，le小ge大
approx约等equiv恒
```

**对应：** ≠ ≤ ≥ ≈ ≡

**基本运算符：**
```
pm加减，times乘
div除，cdot点乘
```

**对应：** ± × ÷ ·

---

### 3. 分数根号口诀

```
frac分数两花括
sqrt根号后面跟
```

**对应：** `\frac{分子}{分母}`、`\sqrt{x}`

---

### 4. 上下标口诀

```
^上_下，多个花括装
```

**对应：** `x^2`、`x_i`、`x^{2y}`、`x_{ij}`

---

### 5. 求和积分极限口诀

```
sum求和sigma蛇
int积分蛇弯弯
lim极限limit
prod乘积pi大
```

**对应：** ∑ ∫ lim ∏

**结构规律：** 都是 `\命令_{下界}^{上界} 表达式`

---

### 6. 箭头口诀

```
to右gets左
大写双线推出
mapsto映射到
```

**对应：** → ← ⇒ ↦

**单双线区别：**
- 单线 → = 过程、变化
- 双线 ⇒ = 逻辑推理
- 双向双线 ⇔ = 等价

---

### 7. 矩阵口诀

```
matrix基础款
p圆b方B花
v单V双cases条件
```

**对应：** matrix pmatrix bmatrix Bmatrix vmatrix Vmatrix cases

**省略号口诀：**
```
cdots横，vdots竖
ddots斜对角
```

**对应：** ⋯ ⋮ ⋱

---

### 8. 括号口诀

```
小括号直接打
大括号要转义
\left\right自动调
```

**对应：** `( )`、`\{ \}`、`\left( \right)`

---

### 9. 常见错误警示

| 错误 | 正确 | 原因 |
|------|------|------|
| `x^2y` | `x^{2y}` | 多字符要用花括号 |
| `\sqr{x}` | `\sqrt{x}` | 命令拼写错误 |
| `{x+1}` | `\{x+1\}` | 大括号要转义 |
| `\frac{a}{b` | `\frac{a}{b}` | 花括号不配对 |
| `$x^2` | `$x^2$` | 数学模式未闭合 |

---

### 10. 快速记忆技巧

**命令来源记忆：**
- `frac` = fraction（分数）
- `sqrt` = square root（平方根）
- `sum` = sum（求和）
- `int` = integral（积分）
- `lim` = limit（极限）
- `prod` = product（乘积）

**符号形状记忆：**
- `^` 像向上的箭头 → 上标
- `_` 像向下的箭头 → 下标
- `\` 像拐杖 → 命令开始
- `{}` 像袋子 → 包裹多个字符

**口诀总汇：**
```
阿尔法贝塔伽马德尔塔，派西格玛西塔兰姆达欧米伽
ne不等，le小ge大，approx约等equiv恒
pm加减，times乘，div除，cdot点乘
frac分数两花括，sqrt根号后面跟
^上_下，多个花括装
sum求和sigma蛇，int积分蛇弯弯，lim极限limit，prod乘积pi大
to右gets左，大写双线推出，mapsto映射到
matrix基础款，p圆b方B花，v单V双cases条件
cdots横，vdots竖，ddots斜对角
小括号直接打，大括号要转义，\left\right自动调
```

---

*附录完成。祝你学习愉快！🚀*
