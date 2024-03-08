few-shot, zero-shot, and rlhf

zero-shot:预训练后直接问答获得答案

few-shot，also called in-context learning, model frozen 



zero-shot and few-shot can have chain-of-thought



chatgpt:

prompt finetune 30k tasks（指令微调）

训练奖励模型：一般30k-50k数据

rlhf



幻觉：使用强化学习导致编造事实

所以模型需要PPO，惩罚项，防止距离指令微调后的模型太远





NLG：

对于开放性问题，适合用decoder模型



防止答案由重复字符组成：

n-gram blocking(不好)

重复受到loss惩罚

transformer关注不同的词



大小模型decode冲突



decoding生成波动文本：

topk:

重点：处理尾端概率->topp，p可变（依然计算所有概率） ，根据entropy改变分布（-logp(x))，或设置threshold，删除特别小的概率项

temperature:softmax的exp中每一项除以p



teacherforcing:正确答案继续输入（训练时）

studentforcing：上一步答案继续输入（一般是generation时）

导致暴露偏差：scheduled sampling(1-p的概率选择tf, p概率选择sf, p逐渐增大)，或者dagger,纯粹模型生成的结果丢进训练集





生成句子的loss,通过计算词语余弦相似度，向量距离等（使用bert的embedding)

或者聚类统计之后，计算距离（MAUVE)

