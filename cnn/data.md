# Trial 1:

CNN(
  (conv1): Conv2d(1, 10, kernel_size=(5, 5), stride=(1, 1))
  (pool1): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv2): Conv2d(10, 16, kernel_size=(5, 5), stride=(1, 1))
  (pool2): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv3): Conv2d(16, 16, kernel_size=(5, 5), stride=(1, 1))
  (global_average): AvgPool2d(kernel_size=(3, 3), stride=(3, 3), padding=0)
  (dense1): Linear(in_features=5888, out_features=512, bias=True)
  (dropout1): Dropout(p=0.2, inplace=False)
  (dense2): Linear(in_features=512, out_features=512, bias=True)
  (dropout2): Dropout(p=0.2, inplace=False)
  (dense3): Linear(in_features=512, out_features=152, bias=True)
)- 3 CNN layers

Epoch [1] = time 82.6s | loss: 4.427 | val loss: 4.423
Epoch [2] = time 120.0s | loss: 4.270 | val loss: 4.009
Epoch [3] = time 100.4s | loss: 3.745 | val loss: 3.569
Epoch [4] = time 85.8s | loss: 3.376 | val loss: 3.311
Epoch [5] = time 84.3s | loss: 3.099 | val loss: 3.165
Epoch [6] = time 82.8s | loss: 2.838 | val loss: 3.075
Epoch [7] = time 84.4s | loss: 2.587 | val loss: 3.076
Epoch [8] = time 77.1s | loss: 2.308 | val loss: 3.080
Epoch [9] = time 78.0s | loss: 2.061 | val loss: 3.252
Epoch [10] = time 86.5s | loss: 1.803 | val loss: 3.421


# Trial 2 (increased dropout from 0.2 to 0.4)

CNN(
  (conv1): Conv2d(1, 10, kernel_size=(5, 5), stride=(1, 1))
  (pool1): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv2): Conv2d(10, 16, kernel_size=(5, 5), stride=(1, 1))
  (pool2): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv3): Conv2d(16, 16, kernel_size=(5, 5), stride=(1, 1))
  (global_average): AvgPool2d(kernel_size=(3, 3), stride=(3, 3), padding=0)
  (dense1): Linear(in_features=5888, out_features=512, bias=True)
  (dropout1): Dropout(p=0.4, inplace=False)
  (dense2): Linear(in_features=512, out_features=512, bias=True)
  (dropout2): Dropout(p=0.4, inplace=False)
  (dense3): Linear(in_features=512, out_features=152, bias=True)
)

Epoch [1] = time 88.3s | loss: 4.426 | val loss: 4.408
Epoch [2] = time 87.7s | loss: 4.313 | val loss: 4.217
Epoch [3] = time 85.8s | loss: 3.968 | val loss: 3.710
Epoch [4] = time 84.0s | loss: 3.583 | val loss: 3.432
Epoch [5] = time 86.4s | loss: 3.297 | val loss: 3.192
Epoch [6] = time 80.4s | loss: 3.071 | val loss: 3.058
Epoch [7] = time 83.5s | loss: 2.864 | val loss: 2.993
Epoch [8] = time 83.7s | loss: 2.683 | val loss: 2.923
Epoch [9] = time 83.3s | loss: 2.505 | val loss: 2.922
Epoch [10] = time 84.3s | loss: 2.286 | val loss: 2.910
Epoch [11] = time 83.0s | loss: 2.103 | val loss: 2.957
Epoch [12] = time 83.8s | loss: 1.956 | val loss: 3.038
Epoch [13] = time 83.8s | loss: 1.774 | val loss: 3.153
Epoch [14] = time 83.4s | loss: 1.633 | val loss: 3.168
Epoch [15] = time 83.0s | loss: 1.505 | val loss: 3.201


# Trial 3 (decrease kernel size and use stride=2)

CNN(
  (conv1): Conv2d(1, 10, kernel_size=(3, 3), stride=(2, 2))
  (pool1): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv2): Conv2d(10, 16, kernel_size=(3, 3), stride=(2, 2))
  (pool2): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv3): Conv2d(16, 16, kernel_size=(3, 3), stride=(2, 2))
  (global_average): AvgPool2d(kernel_size=(3, 3), stride=(3, 3), padding=0)
  (dense1): Linear(in_features=96, out_features=512, bias=True)
  (dropout1): Dropout(p=0.6, inplace=False)
  (dense2): Linear(in_features=512, out_features=512, bias=True)
  (dropout2): Dropout(p=0.6, inplace=False)
  (dense3): Linear(in_features=512, out_features=152, bias=True)
)

Epoch [11] = time 29.5s | loss: 3.539 | val loss: 3.496
Epoch [12] = time 29.7s | loss: 3.480 | val loss: 3.434
Epoch [13] = time 31.8s | loss: 3.448 | val loss: 3.412
Epoch [14] = time 32.7s | loss: 3.407 | val loss: 3.370
Epoch [15] = time 32.3s | loss: 3.355 | val loss: 3.326
Epoch [16] = time 32.0s | loss: 3.319 | val loss: 3.303
Epoch [17] = time 31.6s | loss: 3.274 | val loss: 3.276
Epoch [18] = time 30.5s | loss: 3.244 | val loss: 3.230
Epoch [19] = time 31.2s | loss: 3.215 | val loss: 3.233
Epoch [20] = time 32.5s | loss: 3.173 | val loss: 3.211
Epoch [21] = time 31.1s | loss: 3.148 | val loss: 3.187
Epoch [22] = time 30.4s | loss: 3.127 | val loss: 3.155
Epoch [23] = time 34.2s | loss: 3.101 | val loss: 3.147
Epoch [24] = time 31.8s | loss: 3.073 | val loss: 3.133
Epoch [25] = time 32.6s | loss: 3.041 | val loss: 3.140
Epoch [26] = time 31.3s | loss: 3.023 | val loss: 3.090
Epoch [27] = time 33.1s | loss: 3.004 | val loss: 3.079
Epoch [28] = time 30.7s | loss: 2.969 | val loss: 3.065
Epoch [29] = time 31.0s | loss: 2.941 | val loss: 3.077
Epoch [30] = time 34.4s | loss: 2.929 | val loss: 3.049
Epoch [31] = time 29.7s | loss: 2.903 | val loss: 3.039
Epoch [32] = time 30.1s | loss: 2.894 | val loss: 3.058
Epoch [33] = time 30.2s | loss: 2.881 | val loss: 3.036
Epoch [34] = time 30.1s | loss: 2.860 | val loss: 3.038
Epoch [35] = time 29.3s | loss: 2.855 | val loss: 3.000
Epoch [36] = time 31.6s | loss: 2.811 | val loss: 3.032
Epoch [37] = time 31.9s | loss: 2.815 | val loss: 3.006
Epoch [38] = time 31.9s | loss: 2.774 | val loss: 3.000
Epoch [39] = time 36.6s | loss: 2.778 | val loss: 3.018
Epoch [40] = time 35.0s | loss: 2.769 | val loss: 2.993
Epoch [41] = time 30.5s | loss: 2.751 | val loss: 2.990
Epoch [42] = time 30.6s | loss: 2.729 | val loss: 2.994
Epoch [43] = time 31.0s | loss: 2.723 | val loss: 3.011
Epoch [44] = time 30.8s | loss: 2.689 | val loss: 2.971
Epoch [45] = time 31.2s | loss: 2.688 | val loss: 2.991
Epoch [46] = time 31.3s | loss: 2.685 | val loss: 2.976
Epoch [47] = time 31.6s | loss: 2.655 | val loss: 2.990
Epoch [48] = time 31.4s | loss: 2.653 | val loss: 2.985
Epoch [49] = time 31.2s | loss: 2.633 | val loss: 2.971
Epoch [50] = time 31.3s | loss: 2.626 | val loss: 2.982
Epoch [51] = time 31.1s | loss: 2.625 | val loss: 2.960
Epoch [52] = time 31.4s | loss: 2.599 | val loss: 2.980
Epoch [53] = time 31.6s | loss: 2.603 | val loss: 2.972
Epoch [54] = time 31.4s | loss: 2.573 | val loss: 2.981
Epoch [55] = time 31.7s | loss: 2.584 | val loss: 2.958
Epoch [56] = time 31.5s | loss: 2.558 | val loss: 2.956
Epoch [57] = time 31.3s | loss: 2.545 | val loss: 2.969
Epoch [58] = time 30.9s | loss: 2.537 | val loss: 2.952
Epoch [59] = time 31.8s | loss: 2.542 | val loss: 2.952
Epoch [60] = time 31.6s | loss: 2.524 | val loss: 2.953
Epoch [61] = time 32.1s | loss: 2.515 | val loss: 2.960
Epoch [62] = time 32.0s | loss: 2.519 | val loss: 2.948
Epoch [63] = time 31.2s | loss: 2.497 | val loss: 2.952
Epoch [64] = time 32.0s | loss: 2.484 | val loss: 2.959
Epoch [65] = time 31.9s | loss: 2.485 | val loss: 2.945
Epoch [66] = time 31.5s | loss: 2.477 | val loss: 2.948
Epoch [67] = time 31.3s | loss: 2.481 | val loss: 2.946
Epoch [68] = time 32.2s | loss: 2.442 | val loss: 2.962
Epoch [69] = time 31.7s | loss: 2.437 | val loss: 2.973
Epoch [70] = time 29.2s | loss: 2.467 | val loss: 2.951

# Trial 4 (increase kernel size)

CNN(
  (conv1): Conv2d(1, 10, kernel_size=(5, 5), stride=(1, 2))
  (pool1): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv2): Conv2d(10, 16, kernel_size=(5, 5), stride=(1, 2))
  (pool2): MaxPool2d(kernel_size=2, stride=2, padding=0, dilation=1, ceil_mode=False)
  (conv3): Conv2d(16, 16, kernel_size=(5, 5), stride=(1, 2))
  (global_average): AvgPool2d(kernel_size=(3, 3), stride=(3, 3), padding=0)
  (dense1): Linear(in_features=512, out_features=512, bias=True)
  (dropout1): Dropout(p=0.6, inplace=False)
  (dense2): Linear(in_features=512, out_features=512, bias=True)
  (dropout2): Dropout(p=0.6, inplace=False)
  (dense3): Linear(in_features=512, out_features=152, bias=True)
)

Epoch [1] = time 54.3s | loss: 4.438 | val loss: 4.389
Epoch [2] = time 52.5s | loss: 4.350 | val loss: 4.323
Epoch [3] = time 49.3s | loss: 4.259 | val loss: 4.177
Epoch [4] = time 47.1s | loss: 4.105 | val loss: 3.976
Epoch [5] = time 49.8s | loss: 3.891 | val loss: 3.742
Epoch [6] = time 34.8s | loss: 3.691 | val loss: 3.545
Epoch [7] = time 33.9s | loss: 3.537 | val loss: 3.408
Epoch [8] = time 32.9s | loss: 3.411 | val loss: 3.326
Epoch [9] = time 33.8s | loss: 3.312 | val loss: 3.229
Epoch [10] = time 32.9s | loss: 3.208 | val loss: 3.178
Epoch [11] = time 33.0s | loss: 3.131 | val loss: 3.129
Epoch [12] = time 33.0s | loss: 3.063 | val loss: 3.054
Epoch [13] = time 34.7s | loss: 3.009 | val loss: 3.056
Epoch [14] = time 32.1s | loss: 2.934 | val loss: 2.972
Epoch [15] = time 32.8s | loss: 2.889 | val loss: 2.977
Epoch [16] = time 33.3s | loss: 2.860 | val loss: 2.906
Epoch [17] = time 33.5s | loss: 2.805 | val loss: 2.936
Epoch [18] = time 33.6s | loss: 2.779 | val loss: 2.887
Epoch [19] = time 38.8s | loss: 2.721 | val loss: 2.944
Epoch [20] = time 31.9s | loss: 2.683 | val loss: 2.877
Epoch [21] = time 33.4s | loss: 2.654 | val loss: 2.848
Epoch [22] = time 33.0s | loss: 2.630 | val loss: 2.801
Epoch [23] = time 44.0s | loss: 2.597 | val loss: 2.785
Epoch [24] = time 45.3s | loss: 2.560 | val loss: 2.795
Epoch [25] = time 45.7s | loss: 2.538 | val loss: 2.775
Epoch [26] = time 44.1s | loss: 2.502 | val loss: 2.755
Epoch [27] = time 46.5s | loss: 2.472 | val loss: 2.760
Epoch [28] = time 45.3s | loss: 2.446 | val loss: 2.753
Epoch [29] = time 44.7s | loss: 2.427 | val loss: 2.751
Epoch [30] = time 42.7s | loss: 2.405 | val loss: 2.753
Epoch [31] = time 45.9s | loss: 2.367 | val loss: 2.738
Epoch [32] = time 44.9s | loss: 2.355 | val loss: 2.735
Epoch [33] = time 47.1s | loss: 2.337 | val loss: 2.752
Epoch [34] = time 44.9s | loss: 2.313 | val loss: 2.741
Epoch [35] = time 44.9s | loss: 2.303 | val loss: 2.733
Epoch [36] = time 44.9s | loss: 2.268 | val loss: 2.734
Epoch [37] = time 45.7s | loss: 2.221 | val loss: 2.750
Epoch [38] = time 45.4s | loss: 2.227 | val loss: 2.728
Epoch [39] = time 46.4s | loss: 2.211 | val loss: 2.740
Epoch [40] = time 42.3s | loss: 2.187 | val loss: 2.746
Epoch [41] = time 40.9s | loss: 2.163 | val loss: 2.765
Epoch [42] = time 42.1s | loss: 2.155 | val loss: 2.789
Validation loss has been rising. Stopping