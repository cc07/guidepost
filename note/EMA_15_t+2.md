# EMA 15 t+2

### Structure

1 Input

2 2D Convolution (filters=64, kernel_size=[8, 8], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 4], padding='SAME')

3 2D Convolution (filters=128, kernel_size=[4, 4], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 2], padding='SAME')

4 2D Convolution (filters=128, kernel_size=[3, 3], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 1], padding='SAME')

5 2D Convolution (filters=64, kernel_size=[8, 8], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 8], padding='SAME')

6 BasicLSTMCell (num_units=64)
* DropoutWrapper (keep_prob=0.6)

7 fc (64)
8 fc (32)

### Optimizer

AdamOptimizer

### Expectation

The model will be able to forecast the two step ahead of EMA15 (10 periods).  

### Result

The highest out-of-sample testing was merely at 70% correct, which is far from a satisfying result. The overfitting problem was seriously affecting the performance.

### Conclusion

It could be a wrong question's problem, either we add more relevant inputs to expect some improvement or to seek for an alternative goal.
