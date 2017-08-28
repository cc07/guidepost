# EMA 15 t+2

### Structure

* Input

* 2D Convolution (filters=64, kernel_size=[8, 8], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 4], padding='SAME')

* 2D Convolution (filters=128, kernel_size=[4, 4], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 2], padding='SAME')

* 2D Convolution (filters=128, kernel_size=[3, 3], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 1], padding='SAME')

* 2D Convolution (filters=64, kernel_size=[8, 8], strides=[1, 1], padding='SAME') + kernel_regularizer (scale=0.1)
* batch_norm
* max_pooling2d (pool_size=2, strides=[1, 8], padding='SAME')

* BasicLSTMCell (num_units=64)
* DropoutWrapper (keep_prob=0.6)

* fc (64)
* fc (32)

### Optimizer

AdamOptimizer

### Expectation



### Result

### Conclusion
