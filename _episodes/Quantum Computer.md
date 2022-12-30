# Quantum Computer

## Deutsch's algorithm

| 量子                               | Hilbert 空间      |      |
| ---------------------------------- | ----------------- | ---- |
| $|\phi\rangle,|0\rangle,|1\rangle$ | （列）向量，基    |      |
| $|0\rangle|1\rangle$               | 张量积            |      |
| 密度矩阵                           | 矩阵（Gram 矩阵） |      |
| 量子系统                           | 向量族            |      |
| （投影）测量系统                   | （投影）矩阵族    |      |
| $\langle\psi|\phi\rangle$          | 内积              |      |



## QuTip， Python实现

### states

```py
state = basis(2, 0)  # |0>
state.dag() # <0|

qutip.bra("10")  # |10>
'''Quantum object: dims = [[1, 1], [2, 2]], shape = (1, 4), type = bra
Qobj data =
[[0. 0. 1. 0.]]'''

qutip.bra("121",3)
'''Quantum object: dims = [[1, 1, 1], [3, 3, 3]], shape = (1, 27), type = bra
Qobj data =
[[0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 0. 1. 0. 0. 0. 0. 0. 0. 0.
  0. 0. 0.]]'''

qutip.bra("12",[3,4])
'''Quantum object: dims = [[1, 1], [3, 4]], shape = (1, 12), type = bra
Qobj data =
[[0. 0. 0. 0. 0. 0. 1. 0. 0. 0. 0. 0.]]'''
```



### gates, operators, matrices

```python
# matrix
identity(2)  # 1

# the spin operators
sigmax() # x gate
sigmay() # y gate
sigmaz() # z gate
hadamard_transform(N=1) # Hadamard gate

toffoli() # Toffoli gate
```

### Saving and Loading Result Objects

```python
qsave(result, 'filename')
stored_result = qload('filename')
```



### states

```python

```



