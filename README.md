## ChromPoly 色数多项式

<font size = 4 style="font-family:微软雅黑">

### 一、概述

本程序旨在求解给定图的色数多项式(chromatic Polynomial)，项目名称由此而来。

### 二、环境及编译

- 编译器：g++ (GCC) 4.8.1

- 操作系统：仅在Windows 10下测试编译成功，但其他操作系统应当同样可以编译通过。

在目录下使用命令行执行

`g++ -o ChromPoly ChromPoly.cpp`

即可生成可执行文件ChromPoly.exe。

### 三、问题说明

考查无向图G = (V, E)。G的一个k-染色（coloring）是从V到[1, k]的一个映射： 

π: V → {1, 2, ..., k}

而且满足 

∀ v, u ∈ V, π(v) ≠ π(u) if (v, u) ∈ E 

简而言之，就是将所有顶点归入不超过k个等价类，且保证相邻顶点不属同类。若将图G和k视作变量，则可用函数CP(G, k)表示图G的k-染色（方案）数。而对任一图G，该函数都是k的多项式形式，称作色多项式（chromatic polynomial）。

本题即是要求给定图的色数多项式。

### 四、输入格式

第一行为图的顶点数n与图的边数m。

以下每一行(u,v)表示图中的一条边，且保证满足0<=u,v<n。保证图中不含回边。

### 五、输出格式

n+1行，每一行表示该图色多项式各项的系数（依k的次数由低向高排列）。

</font>