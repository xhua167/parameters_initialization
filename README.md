# parameters_initialization


# 0初始化          
在神经网络中，0初始化是不可以的，在bp的时候每个神经元是一样的。而且每以层神经网络学到的东西也是一样的。        

# 对w随机初始化
目前常用的就是随机初始化，即W随机初始化。但是随机初始化也有缺点，np.random.randn()其实是一个均值为0，方差为1的高斯分布中采样。当神经网络的层数增多时，会发现越往后面的层的激活函数（使用tanH）的输出值几乎都接近于0。              

# Xavier initialization
Xavier initialization是 Glorot 等人为了解决随机初始化的问题提出来的另一种初始化方法，他们的思想倒也简单，就是尽可能的让输入和输出服从相同的分布，这样就能够避免后面层的激活函数的输出值趋向于0。Xavier对于tanh的效果很好，对于relu就无力了。            

# He initialization
一种正对relu的初始化方法。        
