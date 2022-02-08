# 正义之怒：肉搏职业数据流测评

## 测评的前提条件

只计算到前13级+神话4的数据，用于表示职业的前中期强度，至于13级以后，基本上都是成型了，如果还不能开启无双割草模式，那也太”后期“了。

### 关于BUG和房规

**原则上排除一切BUG，因为我没精力去实际测试全体职业和各种装备的适配性，也没这个必要去计算这些奇奇怪怪的BUG及其组合效果。**

BUG的定义：程序设计之外的错误。这里说的BUG是指与描述和设计意图不符合，产生了意料之外的其他增强或削弱效果---比如地狱烈焰射线的1.5倍伤害，附伤叠加之类。

房规的定义：跟桌面规则不符合，但是跟游戏里的描述一致，或者游戏里没有对此有特殊说明 --- 比如歌者、原怒者可以用专长选狂暴特技；比如自然低语和鳞拳魅上防叠加。

这里有几个特例：部分天生防御加值叠加、魔化防具BUG、行动自如免疫知命的恍惚、动物伙伴属性跟选择界面的描述不符、这些还是默认保留。魔化防具有利于重甲和无甲的平衡，因为重甲持盾可以额外吃到+5的AC【盾牌增强加值】。行动自如免疫恍惚，感觉挺有道理的。

排除的BUG如下：

1. 排除附伤叠加BUG --- 比如巨灵化身附带正义烙印、神圣公正破敌附魔的效果。
2. 排除要害打击、奋力冲锋和重击伤害等伤害乘算的BUG。
3. 排除变形效应叠加（多个巨灵化身）和体型效应叠加（比如伟岸+缩小）的BUG。
4. 排除两种武器训练叠加，多来源宿敌叠加，永饥寿衣、圣兽之爪的增强叠加的BUG。排除共享宿敌以后可以享受队友的视如仇寇的BUG。
5. 排除研究目标第一次攻击成功偷袭目标以后没有附加研究目标伤害的BUG。
6. 排除狐人变形BUG---这个即将修复了
7. 排除魔化武器、高等魔化武器跟武器原本加值叠加的BUG---跟TTT保持一致。排除魔牙和高等魔牙叠加的BUG。
8. 武僧拳头和天生武器不吃武器附魔的BUG---1.2版本狗子可以用圣战之刃打附伤了。
9. 啮咬攻击次数叠加的BUG，还有单天武动物伙伴变形以后的攻击次数极大增加的BUG。
10. 其他没举例的奇奇怪怪的或修复或者没修复的BUG，比如双持念刃，念袭要害打击，通过特定技巧让无甲不持盾获得魔化盾牌加值等。

### 游戏里有几个特殊的机制

1. 免疫精准伤害，100%护命这些，效果都是免疫偷袭造成的额外伤害，但是还是可以对其上研究目标和错乱之创。
2. 护命可以有概率免疫重击和偷袭造成的额外伤害，但是你重击了队友还是可以通过包抄或者抓准时机对其借机攻击的。只有免疫重击的敌人才可以无视重击威胁---就算骰20也不会进入重击确认那一步。
3. 幽冥附魔可以破虚体的免疫重击和免疫精准伤害。
4. 光能附魔效果可以跟空间斩叠加，也就是说敌人的接触防御的基础上，还要再减去一次盔甲类加值（护盾术、法师护甲、防御护腕、盔甲、魔化防具、盾牌/盔甲专攻之类）。--- 这个当成BUG也行。

## 评价标准

### 通用队伍和通用BUFF

通用队伍即为1个九环法师（无学派）+1个九环牧师（无领域），通用buff即九环法师和九环牧师可以提供的、目标可以为队友的buff。

### 常态、极限I、极限II状态

**常态**：队友给通用分钟级buff+自身分钟级buff和分钟级能力（例外：野蛮人狂暴和诗人/歌者的歌也算）所能达成的常态。

​	【注：对于自身的非分钟级buff和能力，如果多次使用可以实现持续时间大于分钟级BUFF 或 5个延时加速术，也视为常态】

**极限I**：在常态的基础上，用自身轮级buff和队友给的轮级buff所能达成的状态（比如队友给高等隐形术、祈祷术、荣光爆发之类）。

**极限II**：在极限I的基础上，自己在使用每天一次或几次的持续时间极短的能力所能达成的状态，比如烛台守卫、圣洁幸运之类。

### 完备度

表示达到常态、极限I、极限II，需要依赖队友多少个通用BUFF的支持。

使用队友N个BUFF以达到某种状态A，记为（A|N）。

### 装备依赖度

某个装备栏只能放特定装备：比如战士的手套栏必备<（次级）决斗手套>，对战士来说确实强化了战力，但是其他职业的手套位可以装备其他强力手套（如果有，比如<圣兽之爪>---虽然这里当成BUG排除了），对于自身也有其他加成。又比如武僧可以穿<秩序长袍>，但是其他职业可以穿<招摇撞骗>，效果其实不差。

### 支援能力

即维持自身基本战力的同时，给队友的额外支援，包括法术位（比如加速术、祈祷术、高等隐形术）和职业能力（比如歌者的狂暴战歌）。

### 通用开卡

人类种族，主力就是19力量开局，主敏就是19敏开局

### 通用战斗系专长和专长优先级

#### 专长优先级

**远程和双持**：双持系/远程系＞借机流＞AB转换为伤害的专长 = 粉碎防御系列 = 其他必要专长 = 战士专长系列

**双手**：AB转换为伤害的专长＞借机流＞双手顺势斩系列＞粉碎防御系列 = 其他必要专长 = 战士专长系列

**天生武器**：因为强度基于BUG ---啮咬叠加，不考虑这个BUG的话，天生武器实在是弱的可怜（指上限），不做评价。

#### 通用战斗系专长汇总

借机流：包抄、战斗反射、抓准时机、精通重击

**双手**顺势斩系列：顺势斩、强力顺势斩、终势斩、精通终势斩

**双持**系列：双武器战斗、精通双武器战斗、高等双武器战斗，双斩

**远程**系列：近程射击、精准射击、快速射击、多重射击

粉碎防御系列：武器专攻、炫目武技（双手游侠/杀手可以无视这个先决条件）、粉碎防御

AB转换为伤害的专长：猛力攻击，食人鱼打击、致命瞄准

战士专长系列：武器专精，高等武器专攻，高等武器专精

敏系额外专长：武器娴熟（游荡者会送），优雅挥砍/优雅刺击

其他必要专长：精通先攻，熟练偷袭者

### 武器和装备

| 等级  | 武器   | 腰带                        |      |      |
| ----- | ------ | --------------------------- | ---- | ---- |
| 1-3   | 精制品 | 无                          |      |      |
| 4-6   | +1     | 无                          |      |      |
| 7-10  | +2     | 8级后+4巨力腰带和+2敏捷腰带 |      |      |
| 11-13 | +3     | +4巨力腰带和+4敏捷腰带      |      |      |

## 次要评价标准

先攻、豁免、AC、血量和免疫，不会给详细的数据，只是给个大概的描述。

## 参赛选手

**力双手模板** ---标准武器为1d10，斩矛

| 等级 | AB   | 伤害   | 所需BUFF         | 力量调整值 | 武器骰 | 体型调整值 | 武器加值 |
| ---- | ---- | ------ | ---------------- | ---------- | ------ | ---------- | -------- |
| 1    | 5    | 2d8+7  | 变巨术           | 21（5）    | 2d8    | -1         | 精制品   |
| 2    | 5    | 2d8+7  | 变巨术           | 21（5）    | 2d8    | -1         | 精制品   |
| 3    | 7    | 2d8+10 | 变巨术，牛之蛮力 | 25（7）    | 2d8    | -1         | 精制品   |
| 4    | 8    | 2d8+13 | 变巨术，牛之蛮力 | 26（8）    | 2d8    | -1         | +1       |
| 5    | 8    | 2d8+13 | 变巨术，牛之蛮力 | 26（8）    | 2d8    | -1         | +1       |
| 6    | 8    | 2d8+13 | 变巨术，牛之蛮力 | 26（8）    | 2d8    | -1         | +1       |
| 7    | 9    | 2d8+14 | 变巨术，牛之蛮力 | 26（8）    | 2d8    | -1         | +2       |
| 8    | 9    | 2d8+14 | 变巨术，牛之蛮力 | 27（8）    | 2d8    | -1         | +2       |
| 9    | 9    | 2d8+14 | 变巨术           | 27（8）    | 2d8    | -1         | +2       |
| 10   | 9    | 2d8+14 | 变巨术           | 27（8）    | 2d8    | -1         | +2       |
| 11   | 10   | 2d8+15 | 变巨术           | 27（8）    | 2d8    | -1         | +3       |
| 12   | 11   | 2d8+16 | 变巨术           | 28（9）    | 2d8    | -1         | +3       |
| 13   | 12   | 3d8+19 | 伟岸雄姿         | 32（11）   | 3d8    | -2         | +3       |

**敏双手模板** ---标准武器为1d10，精灵曲刃

【注：最早3级敏上伤，最晚是8级+神话2才能实现敏上伤；且序章最多3级，主角敏菜刀没猫之轻灵，除非主角自己是法师】

| 等级 | AB   | 伤害   | 所需BUFF         | 敏捷调整值 | 武器骰 | 体型调整值 | 武器加值 |
| ---- | ---- | ------ | ---------------- | ---------- | ------ | ---------- | -------- |
| 1    | 7    | 1d8    | 缩小术           | 21（5）    | 1d8    | +1         | 精制品   |
| 2    | 7    | 1d8    | 缩小术           | 21（5）    | 1d8    | +1         | 精制品   |
| 3    | 7    | 1d8+7  | 缩小术           | 21（5）    | 1d8    | +1         | 精制品   |
| 4    | 10   | 1d8+13 | 缩小术，猫之轻灵 | 26（8）    | 1d8    | +1         | +1       |
| 5    | 10   | 1d8+13 | 缩小术，猫之轻灵 | 26（8）    | 1d8    | +1         | +1       |
| 6    | 10   | 1d8+13 | 缩小术，猫之轻灵 | 26（8）    | 1d8    | +1         | +1       |
| 7    | 11   | 1d8+14 | 缩小术，猫之轻灵 | 26（8）    | 1d8    | +1         | +2       |
| 8    | 11   | 1d8+14 | 缩小术，猫之轻灵 | 27（8）    | 1d8    | +1         | +2       |
| 9    | 11   | 1d8+14 | 缩小术，猫之轻灵 | 27（8）    | 1d8    | +1         | +2       |
| 10   | 11   | 1d8+14 | 缩小术，猫之轻灵 | 27（8）    | 1d8    | +1         | +2       |
| 11   | 12   | 1d8+15 | 缩小术，猫之轻灵 | 27（8）    | 1d8    | +1         | +3       |
| 12   | 13   | 1d8+16 | 缩小术           | 28（9）    | 1d8    | +1         | +3       |
| 13   | 13   | 1d8+16 | 缩小术           | 28（9）    | 1d8    | +1         | +3       |

力双持模板---主手和副手可以不一致，所以统一当成1d6计算

| 等级 | AB   | 伤害   | 所需BUFF         | 力量调整值 | 武器骰 | 体型调整值 | 武器加值 |
| ---- | ---- | ------ | ---------------- | ---------- | ------ | ---------- | -------- |
| 1    | 3    | 2d6+7  | 变巨术           | 21（5）    | 2d6    | -1         | 精制品   |
| 2    | 3    | 2d6+7  | 变巨术           | 21（5）    | 2d6    | -1         | 精制品   |
| 3    | 5    | 2d6+10 | 变巨术，牛之蛮力 | 25（7）    | 2d6    | -1         | 精制品   |
| 4    | 6    | 2d6+13 | 变巨术，牛之蛮力 | 26（8）    | 2d6    | -1         | +1       |
| 5    | 6    | 2d6+13 | 变巨术，牛之蛮力 | 26（8）    | 2d6    | -1         | +1       |
| 6    | 6    | 2d6+13 | 变巨术，牛之蛮力 | 26（8）    | 2d6    | -1         | +1       |
| 7    | 7    | 2d6+14 | 变巨术，牛之蛮力 | 26（8）    | 2d6    | -1         | +2       |
| 8    | 7    | 2d6+14 | 变巨术，牛之蛮力 | 27（8）    | 2d6    | -1         | +2       |
| 9    | 7    | 2d6+14 | 变巨术           | 27（8）    | 2d6    | -1         | +2       |
| 10   | 7    | 2d6+14 | 变巨术           | 27（8）    | 2d6    | -1         | +2       |
| 11   | 8    | 2d6+15 | 变巨术           | 27（8）    | 2d6    | -1         | +3       |
| 12   | 9    | 2d6+16 | 变巨术           | 28（9）    | 2d6    | -1         | +3       |
| 13   | 10   | 3d6+19 | 伟岸雄姿         | 32（11）   | 3d6    | -2         | +3       |

敏双持模板---标准武器为反曲刀，1d4

敏单持模板---标准武器为穿甲剑，2d4

远程模板---标准武器为复合长弓，1d8

### 杀手

### 战士

### 原怒者

### 游侠

### 魔战士

### 歌者

### 先知

### 游荡者

