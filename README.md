# RAL_new
基于主动强化学习的上下位词标注<br/>
agent1挑选数据簇，agent2决定人工打标/机器打标<br/>
训练时先预训练好agent1，然后训练agent2，此时agent1不再更新<br/>
<br/>
各文件<br/>
.json<br/>
A_train_newest：训练过程中供打标的数据集<br/>
A_test_newest：训练过程中供测试分类器效果的数据集<br/>
B_train_newest：测试过程中供打标的数据集<br/>
embedding & embedding：数据集中所有词的词向量，前者维数为50，后者为25；经过验证，50维数比较高，故采用后者<br/>
center：训练过程中各簇中有标签数据中心点的变化<br/>
<br/>
.png<br/>
pic_3 - pic_7：聚类效果（通过主成分降维），从3类到7类；由于主成分分布得比较均匀，2维上可能看不出效果<br/>
<br/>
.py<br/>
cluster: 试看一下聚类的效果<br/>
agent：agent1  agent2：agent2<br/>
data：负责数据集的读取，存储，维护数据是否打标以及标签<br/>
embedding：负责读入词向量<br/>
env：环境 <br/>
model：分类器<br/>
state：管理两个agent的状态特征<br/>
train & test & main<br/>
<br/>
.pkl
预训练好的agent1模型
