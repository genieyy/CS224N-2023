numpy：实际上调用了c和c++

和list直接转换：

numpy.array(np.array)

x.shape



np.max(x,axis=1,keepdims=True)

np.sort(x)(计算每个sort并相加)

np.sum(x，axis=)

np.matmul========@

np.dot(对于一维向量，对应位置元素相乘并相加所有元素；对于矩阵，等同于矩阵乘法）



索引：x[np.array([1,2]), :]

布尔索引：

比较x[x>0.5]



扩展维度：

x[: , : , np.newaxis]或者（2，）->(2, 1)



### numpy广播功能：

 [0,0,0]+[1]=[1,1,1]

不同的一个维度为1，其他相同