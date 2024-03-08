pytorch



tensor：

torch.tensor([]

,dtype=torch.int)

torch.zeros(1,3)

torch.ones(1,3)

torch.empty(2,3)

torch.arrange(1,10)

torch.randn(1,3)

torch.randn_like(y)

matmul,@.以及广播和numpy一样



torch.bmm 



torch.view并不实际改变x形状

reshape直接改变形状



可以和array互换格式

可以直接x.numpy()



数据处理（data.sum(dim=1))

x[0,0,0].item()





linear=nn.Linear(4,2)

nn.Linear(x) 

linear.parameters() 返回对应参数值



(4,2,4)和（4,2）形状可以想乘，把第一个当成batchsize(和numpy不同之处 )





block=nn.Sequential(nn.Linear(4,2),nn.Sigmoid())

block(input)



import torch.optim as optim

model=MultilayerPercetion(5,3)

adam=Optim.Adam(model.parameters(), lr=1e-1)

loss_function=nn.BCELoss()

y_pred=model(x)

loss_function(y_pred,y).item()



例子

for epoch in range(nepoch):

adam.zero_grad()

y_pred=model(x)

loss=loss_function(y_pred,y)

print("Epoch  {epoch}:   training_loss:   {loss}")

loss.backward()

adam.step()