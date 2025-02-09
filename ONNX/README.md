# ONNX Format

Open Neural Network eXchange (ONNX) is an open standard format for representing machine learning models. 


#### Example: Conv-2d layer
```
graph (name=graph):
  input (name='input', shape=(1, 1, 28, 28), type=float32)
  output (name='output', shape=(1, 32, 28, 28), type=float32)

  node (name='Conv_0', op_type='Conv'):
    input: ['input', 'conv.weight', 'conv.bias']
    output: ['output']
    attributes: {'kernel_shape': [3, 3], 'pads': [1, 1, 1, 1], 'strides': [1, 1]}

  initializer:
    - name: 'conv.weight', shape=(32, 1, 3, 3), type=float32
    - name: 'conv.bias', shape=(32,), type=float32
``` 

References:
 - https://github.com/onnx/tutorials
 - https://pytorch.org/tutorials/beginner/onnx/intro_onnx.html 
