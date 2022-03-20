三角函数

x[n] = Amplitube cos(frequency * n + phase)

对于连续信号来说, frequency 和 phase always可以等价转换的, 但是对于离散信号是不成立的, 因为在离散信号中 n always is integer, 并非总是能找到对应的点.

对于离散信号来说一定可以找到另一个 frequency 不同却相同的信号(例如frequency - 2*Pi), 但是对于连续信号不成立.

离散信号的周期并非一定是 2\*Pi/frequency, 因为要取整, 且离散信号并非一定有周期, 当frequency与Pi无法约去的时候, 2\*Pi/frequency 是一个无理数

复指数信号可以通过欧拉公司与三角函数信号进行转换, 所以也是基础信号之一

impulse is the derivative of the step. 单位脉冲函数式阶跃函数的导数.
