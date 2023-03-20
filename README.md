# algo_assignment_1
## Reference papers
20220130-信达证券-信达证券衍生品研究系列之三：股指期货基差收敛研究与对冲优化策略

数据见‘数据及结果.zip’中的ICdata.csv
## contributions and thoughts
本篇研报实际上就是在研究基差收敛的因子，我将研报中提及的影响股指期货收敛速度的三个因素：
- 当前合约的年化基差水平
- 指数的预期收益
- 不同月份合约的基差结构

按照研报中的数据与思路分别与综合进行了复现，复现结果详见ipynb文件或者‘数据及结果.zip’
复现的结果表明，在各个影响因素中，基差收敛的速度主要受两个因素的影响：当前合约的年化基差水平及基差的期限结构。
当前合约的年化基差越约小，即贴水程度越大，其基差收敛越快。同理，基差贴水程度越小，其收敛越慢。
前合约的年化基差相对下季月合约年化基差越小，即该合约贴水幅度更高，其基差收敛速度越快；当前合约年化
基差相对下季月合约越大，即该合约贴水幅度更小，其基差收敛速度越慢。

与研报有出入的部分在于第二个因子：指数的预期收益。
未来收益率该因素存在正向关系但根据p与t值的检验显示该关系不显著。
除此之外，我采用了和研报相同的时间段与目标对象，虽然变量之间的关系并无差别，但复现的数据结果与研报有出入。
猜测与研报中基差首先消除了成份股分红对基差的影响而我并未对股息进行处理，另清洗数据过程也可能不同。

我并未对研报中的对冲优化策略进行复现，闲暇时或者下次作业复现最低贴水策略。
## Relevant coding
基差分析.ipynb
