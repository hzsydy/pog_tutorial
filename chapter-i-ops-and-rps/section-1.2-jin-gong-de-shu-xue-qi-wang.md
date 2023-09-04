# 例：西线进攻的数学期望

#### 太长不看版

* 除非至少使得火力提升两级，不然带着(a)或c进攻在op交换上是亏的。
* 带着(a)或c防御在op交换上几乎总是亏的，有战壕的时候更严重；sr军支撑西线在大多数时候是智障行为。

\==========================================

首先，大家都很熟悉这张pog army fire table：

| Fire value |   1  |  2  |  3  |  4  |  5  | 6-8 | 9-11 | 12-14 |  15  |  16+ |
| :--------: | :--: | :-: | :-: | :-: | :-: | :-: | :--: | :---: | :--: | :--: |
|      1     |   0  |  1  |  1  |  2  |  2  |  3  |   3  |   4   |   4  |   5  |
|      2     |   1  |  1  |  2  |  2  |  3  |  3  |   4  |   4   |   5  |   5  |
|      3     |   1  |  2  |  2  |  3  |  3  |  4  |   4  |   5   |   5  |   7  |
|      4     |   1  |  2  |  3  |  3  |  4  |  4  |   5  |   5   |   7  |   7  |
|      5     |   2  |  3  |  3  |  4  |  4  |  5  |   5  |   7   |   7  |   7  |
|      6     |   2  |  3  |  4  |  4  |  5  |  5  |   7  |   7   |   7  |   7  |
|    Avg.    | 1.16 |  2  | 2.5 |  3  | 3.5 |  4  | 4.66 |  5.33 | 5.83 | 6.33 |

因此，立得：

> Theorem 1.2.1 每提高一级火力，期望上对对方多造成约0.5\~0.66伤害。

\=======================================================

然而，众所周知，pog有特别的吃伤害规则，which我们形象的称之为“跳弹”：

> （在尽可能的吸收伤害之后，）不足耐久值的伤害会被吸收，不造成任何伤害。

这条规则也是大家喷pog魔幻的一个重要论据——伤害是离散而不是连续的这件事情使人非常难以理解。然而，这条规则是pog的数学模型的基础，它构成了我们所看到的，pog式的一战——可以说是过程魔幻而结果科学的典型案例了。

根据跳弹规则，易得：

> Lemma 1.2.1 对于一个至少包含(a)或c的堆叠，该堆叠遭到对方k火力攻击时，受损的分布和期望如下表：

| Fire value | 2 | 3   | 4 | 5   | 6-8 | 9-11 | 12-14 | 15   | 16+  |
| ---------- | - | --- | - | --- | --- | ---- | ----- | ---- | ---- |
| 1          | 1 | 1   | 2 | 2   | 3   | 3    | 4     | 4    | 5    |
| 2          | 1 | 2   | 2 | 3   | 3   | 4    | 4     | 5    | 5    |
| 3          | 2 | 2   | 3 | 3   | 4   | 4    | 5     | 5    | 7    |
| 4          | 2 | 3   | 3 | 4   | 4   | 5    | 5     | 7    | 7    |
| 5          | 3 | 3   | 4 | 4   | 5   | 5    | 7     | 7    | 7    |
| 6          | 3 | 4   | 4 | 5   | 5   | 7    | 7     | 7    | 7    |
| Avg.       | 2 | 2.5 | 3 | 3.5 | 4   | 4.66 | 5.33  | 5.83 | 6.33 |

> Lemma 1.2.2 对于一个只含a的西线堆叠（这意味着所有成员都是正面朝上的3防集团军），该堆叠受损的分布和期望如下表：

| Fire value | 2 | 3   | 4 | 5   | 6-8 | 9-11 | 12-14 | 15 | 16+  |
| ---------- | - | --- | - | --- | --- | ---- | ----- | -- | ---- |
| 1          | 0 | 0   | 0 | 0   | 3   | 3    | 3     | 3  | 3    |
| 2          | 0 | 0   | 0 | 3   | 3   | 3    | 3     | 3  | 3    |
| 3          | 0 | 0   | 3 | 3   | 3   | 3    | 3     | 3  | 7    |
| 4          | 0 | 3   | 3 | 3   | 3   | 3    | 3     | 7  | 7    |
| 5          | 3 | 3   | 3 | 3   | 3   | 3    | 7     | 7  | 7    |
| 6          | 3 | 3   | 3 | 3   | 3   | 7    | 7     | 7  | 7    |
| Avg.       | 1 | 1.5 | 2 | 2.5 | 3   | 3.66 | 4.33  | 5  | 5.66 |

对比两张表，立得：

> Theorem 1.2.2 你的堆叠中只要含有(a)或c，期望上你每受到/发起一次攻击就会多受到约1点伤害。

（如1.1所述，1伤害相当于半op）

注意到这个值比0.66伤害要大。因此，我们有：

> &#x20;Corollary 1. 除非至少使得火力提升两级，不然带着(a)或c进攻在op交换上是亏的。

\============================================================

除此之外，pog有另一条和跳弹一样重要的规则，叫抵消撤退。

> （在地形允许，或者有战壕且没被cc取消的情况下），防守方可以额外损失一级step来negate retreat。

POG是一个宽度游戏。很多地方都是寸土不让的——最典型的是色当。因此，在这种地方，我们要考虑抵消撤退带来的额外损失。例如，如果进攻方打出5：4战果，则防守方将会损8——除了损5之外，为了抵消一级再损3。

计算过程略。我们制作了如下表：

> Lemma 1.2.3 对于一个aac/aa(a)堆叠，该堆叠被进攻时防守方损失平均期望随进攻方和防守方火力的变化如下：

| Def Fire | 6A   | 9A   | 12A  | 15A  |
| -------- | ---- | ---- | ---- | ---- |
| Atk 5A   | 3.94 | 3.81 | 3.66 | 3.58 |
| 6A       | 4.77 | 4.55 | 4.33 | 4.16 |
| 9A       | 5.61 | 5.36 | 5.11 | 4.91 |
| 12A      | 6.44 | 6.16 | 5.88 | 5.66 |
| 15A      | 7.05 | 6.78 | 6.5  | 6.25 |
| 16A      | 7.66 | 7.38 | 7.11 | 6.83 |



> Lemma 1.2.4 对于一个aaa堆叠，该堆叠被进攻时防守方损失平均期望随进攻方和防守方火力的变化如下：

![我实在懒得打了总之你们看这张图吧](<../.gitbook/assets/image (5).png>)

于是，立得：

> Theorem 1.2.3 对于aac（或aaa-，下同），为了防守战壕并抵消撤退，每被进攻一次就要额外承受1伤害。
>
> Theorem 1.2.4 对于aaa，为了防守战壕并抵消撤退，每被进攻一次要多承受0.2-0.6不等的伤害。

总结四条th，我们立得：

> Corollary 2.  带着(a)或c防御在op交换上几乎总是亏的。

除此之外，这还意味着sr军支撑西线在大多数时候是智障行为。