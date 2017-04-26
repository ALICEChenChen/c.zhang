Tensorflow

1.常用函数
在tensor的某一维度上求值的函数。如：
求最大值tf.reduce_max(input_tensor, reduction_indices=None, keep_dims=False, name=None)
求平均值tf.reduce_mean(input_tensor, reduction_indices=None, keep_dims=False, name=None)
  参数（1）input_tensor:待求值的tensor。
  参数（2）reduction_indices:在哪一维上求解。
  参数（3）（4）可忽略
举例说明：
