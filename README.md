# Track2 净土保卫战 test pull

![image](./1.png)
<center> 自动化系学生科协</center>

## 游戏背景

随着我国工农业的迅速发展，人们的生活水平的提高，对水质量的要求越来越高。但因水土流失、水源污染等因素的影响，地表水成分逐渐趋于复杂，有机成分增多，饮用水处理难度增大。同时，由于水体受到污染，导致水体富营养化，藻类过量繁殖，产生难闻的臭味和有害的藻毒素。对日常饮用水带来了极大的危害，不仅严重影响着人群健康水平，同时也是我国生态文明建设的巨大挑战。在此背景之下，响应各方要求的碧水保卫战应运而生。

为了打好碧水保卫战，解决水体富营养化问题成为了当务之急，科学家们构造了一种净水细胞DA-I，作为生物防治体系的一把尖刀，该细胞可以很好地吸收水体中的营养物质来让自身成长，同时该种细胞拥有强大的增殖能力，可以通过快速的分裂来产生更多的同类细胞，快速提升净水效率。但是，在长江某富营养化水域中，存在着一些特别的营养物质，该种营养物质会对DA-I型细胞造成损伤，一度使当地的水体防治陷入困境。但是，科学家们经过艰苦的研究和夜以继日的努力，推出了DA-II型细胞，该型细胞不仅拥有DA-I型的所有优点，还可以针对有害型营养物质做出特定应激反应来保护自身，水体富营养化问题的解决指日可待……

## 赛题概述

本分赛区（第17届自动化系新生C语言大赛）赛题为碧水保卫战，属于回合制对战类3d界面游戏。

参赛选手编写AI代码作为一方势力参加碧水保卫混战，本次大赛采用多AI（16个）同图竞技的赛制，各势力间处于永战状态。各个选手通过操纵细胞，通过移动、分裂和喷吐等基本操作方式来吸收水体环境中的富营养物质或吞噬其他选手的细胞从而使自身增长，同时抵御恶劣环境的干扰。从而获取最终比赛的胜利。

![image](./4.png)
<center> 比赛三维地图</center>

## 规则介绍

## 细胞

游戏中玩家操控细胞吞噬周遭的一切事物,包含营养物质与小于自己的细胞,具体的操作可分为三类
- 移动: 细胞朝指定方向移动,速度与加速度与自身半径大小成反比
- 喷吐: 细胞朝指定方向喷吐部份自体组织,喷吐出的物质为营养物质, 特别地当喷吐出的物质触碰到刺型营养物质将导致刺型营养物质遭到击退
- 分裂: 细胞朝指定方向分裂为两个面积相同的细胞, 若玩家细胞数超过6个,则无法进行分裂
- 死亡: 若一个细胞遭到吞噬或遭受火网与飓风攻击导致半径小于6时,该细胞死亡


## 营养物质

- 普通营养物质：细胞可以吞噬小于自身体积的普通营养物质,并获得相等面积的奖励
- 刺型营养物质：细胞可以吞噬小于自身体积的刺型营养物质,并获得其[面积 / 2]的奖励, 并且在吞噬后细胞将一分为六,包含一颗大细胞与五颗小细胞

![image](./3.png)

<center> 碰到刺型营养物质分裂 / 刺型营养物质(红)与普通营养物质(白)</center>

## 游戏事件

- 下雨: 普通营养物质的刷新率大幅度增加
- 飓风: 在700回合时触发, 从地图角落生成并随机移动, 在飓风半径内的细胞每回合将损失4%面积
- 火网: 在800回合时触发, 逐步往中心收拢, 在火网外围的细胞每回合将损失4%面积
- 重生: 当玩家的最后一个细胞死亡时,在地图随机地点重生,每个玩家有3次重生机会

![image](./2.png)

<center> (左上)飓风 (右上)下雨 (左下)火网 (右下)火网</center>

## 结算方式与获胜条件

当到达1000回合或场上只剩下一个玩家时游戏结束,玩家的得分 = 总面积 + 吞噬的其他玩家细胞面积 * 500，积分最高的玩家获胜

## 详细规则

请选手加入[FC17门户网站](http://140.143.170.135:3000/#/)下载选手包获取详细比赛资源。
