# MOBA-1v1
王者荣耀 1v1

- 作者：陈一凡、陈文盛(不分先后)
- dll: 19/11/24
- 大作业测评：17/11/24

## 目标实现：
1. 确保小兵最后是被我杀的(目前这个好像无法实现，还在问助教是否有小兵这个接口)
2. 当在敌人在我的范围的时候，我会打敌人（并且小兵不是需要被"最后一击"的时候）
3. 回家补血：兵线进到敌方的时候，且不足的时候回去补命

## 已实现：
1. 攻击策略(优势、对峙、劣势)
2. 获取血包的判断
3. 生命低于30%时，回到泉水补命
4. 打塔
5. 避免不必要的伤害
6. last_hit的优化，在没有我方小兵的时候，取补刀会减小奖励值
7. 常待在小兵的附近(让小兵当肉盾)

## 训练遇到的问题：

**5_33392**
问题：
1. 防御塔攻击：保持的距离设置过于保守，导致英雄不会主动攻击对方防御塔。
2. 血量管理：前期因没有及时获取血包，导致英雄血量持续偏低，过度保持与敌方距离，无法进行有效进攻。
3. 小兵攻击：在击杀小兵时，没有合理保持与小兵的安全距离，导致受到小兵攻击，血量损耗。

解决办法：
1. 防御塔的设置不要那么保守
2. 血量管理问题要增加一个机制关于回泉水

还在想如何解决：
1. 由于我们无法获得小兵的信息，所以小兵问题一直无法获得解决


