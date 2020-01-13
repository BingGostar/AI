### **相似矩阵与二次型**
1. **向量的内积、长度及正交性**
    * **内积**
        设有 $n$ 维向量 $x=\left|\begin{array}{l}x_{1}\\x_{2}\\ \vdots\\x_{n}\end{array}\right|,y=\left|\begin{array}{l}y_{1}\\y_{2}\\ \vdots\\y_{n}\end{array}\right|$
        $[x,y]$ 称为向量 $x$ 与 $y$ 的内积，内积的结果是一个实数
        >$$[x,y] = x_{1}y_{1}+x_{2}y_{2}+\cdots+x_{n}y_{n}$$

        >$$[x,y] = x^{T}y$$

    * **施瓦兹不等式**
        >$$[x,y]^{2} \leq [x,x][y,y]$$

    * **数量积**
        解析几何中，向量内积等于数量积
        >$$x\cdot y = |x||y|\cos \theta$$

        在空间直角坐标系中
        >$$(x_{1},x_{2},x_{3})\cdot(y_{1},y_{2},y_{3}) = x_{1}y_{1}+x_{2}y_{2}+x_{3}y_{3}$$

    * **向量的长度（范数）**
        >$$||x|| = \sqrt {[x,x]} = \sqrt {x_{1}^{2}+x_{2}^{2}+\cdots+x_{n}^{2}}$$

    * **向量间的夹角**
        >$$\theta = arc \cos \frac{[x,y]}{||x|| \ ||y||}$$

    * **正交**
        如果两个向量的内积 $[x,y]=0$ 时，称向量 $x$ 与 $y$ 正交，在解析几何中表现为垂直

    * **正交、线性无关**：若 $n$ 维向量 $a_{1},a_{2},\cdots,a_{r}$ 是一组两两正交的非零向量，则 $a_{1},a_{2},\cdots,a_{r}$ 线性无关
        注意：线性无关的一组向量，两两之间不一定正交
        >反证法
        >假设 $\lambda_{1}a_{1}+\lambda_{2}a_{2}+\cdots+\lambda_{r}a_{r} = 0$
        >以 $a_{1}^{T}$ 左乘上式两端。因为两两正交，所以 $a_{1}^{T}a_{i} = 0$，故得
        >$\lambda_{1}a_{1}^{T}a_{1} = 0$
        >因为 $a_{1}^{T}a_{1} \neq 0$，所以 $\lambda_{1} = 0$，同理可得 $\lambda_{2} = 0,\cdots,\lambda_{r}=0$
        >所以违背线性相关定理，则线性不相关

    * **规范正交基**
        设 $n$ 维向量 $e_{1},e_{2},\cdots,e_{r}$ 是向量空间 $V(V \in R^{n})$ 的一个基，如果 $e_{1},e_{2},\cdots,e_{r}$ 两两正交，且都是单位向量，则称 $e_{1},e_{2},\cdots,e_{n}$ 是 $V$ 的一个**规范正交基**
        空间 $V$ 中任一向量都能用规范正交基线性表示
        >$$a=\lambda_{1}e_{1}+\lambda_{2}e_{2}+\cdots+\lambda_{r}e_{r}$$

    * **规范正交化**
        设 $a_{1},\cdots,a_{r}$ 是向量空间 $V$ 中的一个基，要求得 $V$ 中的一个规范正交基，就是找到一组两两正交的单位向量 $e_{1},\cdots,e_{r}$，使 $e_{1},\cdots,e_{r}$ 与 $a_{1},\cdots,a_{r}$ 等价，这样的问题称把 $a_{1},\cdots,a_{r}$ 这个基规范正交化
        施密特正交化
        >$b_{1} = a_{1}$
        >$b_{2} = a_{2} - \frac{[b_{1},a_{2}]}{[b_{1},b_{1}]}b_{1}$
        >$\cdots$
        >$b_{r} = a_{r} - \frac{[b_{1},a_{r}]}{[b_{1},b_{1}]}b_{1} - \frac{[b_{2},a_{r}]}{[b_{2},b_{2}]}b_{2} - \cdots - \frac{[b_{r-1},a_{r}]}{[b_{r-1},b_{r-1}]}b_{r-1}$
        >然后进行单位化
        >$e_{1} = \frac{b_{1}}{||b_{1}||},e_{2} = \frac{b_{2}}{||b_{2}||},\cdots,e_{r} = \frac{b_{r}}{||b_{r}||}$
            
    * **正交矩阵**
        如果 $n$ 阶矩阵 $A$ 满足 $A^{T}A = E(A^{-1}=A^{T})$，则称 $A$ 为正交矩阵
        >$\left|\begin{array}{l} a_{1}^{T} \\ a_{2}^{T} \\ \vdots \\ a_{n}^{T} \end{array}\right| (a_{1},a_{2},\cdots,a_{n}) = E$
        >$(a_{i}^{T}a_{j})=(\delta_{ij})$
        >当 $i=j$ 时等于1，当 $i\neq j$ 时等于0
        
        正交矩阵的充要条件是矩阵 $A$ 的列向量（行向量）都是单位向量，且两两正交
        
    * **正交变换**
        若 $P$ 为正交矩阵，则线性变换 $y=Px$ 是正交变换，则有
        >$||y|| = \sqrt{y^{T}y} = \sqrt{x^{T}P^{T}Px} = \sqrt{x^{T}x} = ||x||$

        以上说明了正交变换可以保持向量**变换后的长度不变**

2. **特征值与特征向量**
    * **定义**
        设 $A$ 是 $n$ 阶矩阵，$x$ 是 $n$ 维非零向量，$\lambda$ 是实数
        >$$Ax=\lambda x$$

        称 $\lambda$ 是矩阵 $A$ 的**特征值**，向量 $x$ 是对应于特征值的**特征向量**
        可改写成
        >$$(A-\lambda E)x = 0$$

    * **特征值和特征向量的解法**
        上述齐次方程组有非零解的充要条件是系数矩阵**行列式等于零**
        >$$|A-\lambda E|=0$$

        即
        >$$\left|\begin{array}{l} a_{11}-\lambda & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22}-\lambda & \cdots & a_{2n} \\ \vdots & \vdots & & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nn}-\lambda \end{array}\right| = 0$$

        **特征多项式**
        上式左端的行列式 $|A-\lambda E|$ 是以 $\lambda$ 为未知数的 $n$ 次多项式，记作 $f(\lambda)$，称为矩阵 $A$ 的特征多项式
        \
        显然 $A$ 的特征值就是特征方程的解，其解的个数为 $n$
        设 $n$ 阶矩阵 $A=(a_{ij})$ 特征值为 $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$，则
        >$\lambda_{1}+\lambda_{2}+\cdots+\lambda_{n} = a_{11}+a_{22}+\cdots+a_{nn}$
        >$\lambda_{1}\lambda_{2}\cdots\lambda_{n} = |A|$

        设 $\lambda=\lambda_{i}$ 为矩阵 $A$ 的一个特征值，则方程 $(A-\lambda_{i}E)x=0$ 的非零解 $x=p_{i}$ 是 $A$ 对应于特征值 $\lambda_{i}$ 的特征向量
        \
        例：求矩阵 $\left|\begin{array}{l} -1&1&0\\-4&3&0\\1&0&2 \end{array}\right|$ 的特征值与特征向量
        >$|A-\lambda E|=\left|\begin{array}{l} -1-\lambda&1&0\\-4&3-\lambda&0\\1&0&2-\lambda \end{array}\right| = (2-\lambda)(1-\lambda)^{2} = 0$
        >$A$ 的特征值为 $\lambda_{1}=2,\lambda_{2}=\lambda_{3}=1$
        >当 $\lambda_{1}=2$ 时，解方程 $(A-2E)x=0$
        >$A-2E = \left|\begin{array}{l} -3&1&0\\-4&1&0\\1&0&0 \end{array}\right| \xrightarrow[]{r} \left|\begin{array}{l} 1&0&0\\0&1&0\\0&0&0\end{array}\right|$
        >基础解系 $p_{1} = \left|\begin{array}{l} 0\\0\\1 \end{array}\right|$，所以对应于 $\lambda_{1}=2$ 的特征向量为 $kp_{1}(k \neq 0)$
        >当 $\lambda_{2}=\lambda_{3}=1$ 时，解方程 $(A-2E)x=0$
        >$A-2E = \left|\begin{array}{l} -2&1&0\\-4&2&0\\1&0&1 \end{array}\right| \xrightarrow[]{r} \left|\begin{array}{l} 1&0&1\\0&1&2\\0&0&0\end{array}\right|$
        >基础解系 $p_{2} = \left|\begin{array}{l} -1\\-2\\1 \end{array}\right|$，所以对应于 $\lambda_{2}=\lambda_{3}=1$ 的特征向量为 $kp_{2}(k \neq 0)$

    * **一些性质**
        设 $\lambda$ 是方阵 $A$ 的特征值
        >(1) $\lambda^{2}$ 是方阵 $A^{2}$ 的特征值，同理 $\lambda^{k}$ 是方阵 $A^{k}$ 的特征值
        >(2) 当 $A$ 可逆时(注意区分 $A-\lambda E$ 不可逆)，$\frac{1}{\lambda}$ 是 $A^{-1}$ 的特征值
        >(3) 设 $\psi(A)=a_{0}E+a_{1}A+\cdots+a_{m}A^{m}$ 是矩阵 $A$ 的多项式，$\psi(\lambda)=a_{0}+a_{1}\lambda+\cdots+a_{m}\lambda^{m}$ 是 $\lambda$ 的多项式，则 $\psi(\lambda)$ 是 $\psi(A)$ 的特征值

        例：设3阶矩阵 $A$ 的特征值为 $1,-1,2$，求 $A^{*}+3A-2E$ 的特征值
        >因为 $A$ 的特征值全不为 $0$，所以 $A$ 可逆。所以 $A^{*}=|A|A^{-1}$，又因为 $|A|=\lambda_{1}\lambda_{2}\lambda_{3}=-2$
        >$A^{*}+3A-2E = -2A^{-1}+3A-2E = \psi(A)$
        >则 $\psi(\lambda) = -2\frac{1}{\lambda}+3\lambda-2$
        >特征值为 $\psi(1)=-1,\psi(-1)=-3,\psi(2)=3$
        
    * **不同特征值对应不同特征向量 线性无关**
        设 $\lambda_{1},\lambda_{2},\cdots,\lambda_{m}$ 是方阵 $A$ 的 $m$ 个特征值，$p_{1},p_{2},\cdots,p_{m}$ 依次是与之对应的特征向量。如果 $\lambda_{1},\lambda_{2},\cdots,\lambda_{m}$ 各不相等，则 $p_{1},p_{2},\cdots,p_{m}$ **线性无关**
        \
        例：设 $\lambda_{1}$ 和 $\lambda_{2}$ 是矩阵 $A$ 的两个不同特征值，其对应的特征向量依次为 $p_{1}$ 和 $p_{2}$，那么 $p_{1}+p_{2}$ 是不是 $A$ 的特征向量？
        >有 $Ap_{1}=\lambda_{1}p_{1}, Ap_{2}=\lambda_{2}p_{2}$
        >$A(p_{1}+p_{2}) = \lambda_{1}p_{1} + \lambda_{2}p_{2}$
        >假设 $p_{1}+p_{2}$ 是 $A$ 的特征向量，那么存在一个数 $\lambda$ 使得 $A(p_{1}+p_{2}) = \lambda(p_{1}+p_{2})$
        >根据上面两式可得
        >$\lambda(p_{1}+p_{2}) = \lambda_{1}p_{1} + \lambda_{2}p_{2}$ 即 $(\lambda_{1}-\lambda)p_{1}+(\lambda_{2}-\lambda)p_{2} = 0$
        >根据定理可知 $p_{1},p_{2}$ 线性无关，所以上式只能 $\lambda_{1}-\lambda = \lambda_{2}-\lambda = 0$
        >即 $\lambda_{1}=\lambda_{2}$，与题设矛盾，所以 $p_{1}+p_{2}$ 不是 $A$ 的特征向量

3. **相似矩阵**
    * **定义**
        设 $A,B$ 都是 $n$ 阶相似矩阵，若有可逆矩阵 $P$，使
        >$$P^{-1}AP=B$$

        则称 $B$ 是 $A$ 的**相似矩阵**，对 $A$ 进行上述运算又称**相似变换**

    * **相似矩阵的特征值相同**
        若 $n$ 阶矩阵 $A$ 与 $B$ 相似，则 $A$ 与 $B$ 的特征多项式相同，从而 $A$ 与 $B$ 的**特征值相同**
        >$|B-\lambda E| = |P^{-1}AP - P^{-1}(\lambda E)P| = |P^{-1}(A-\lambda E)P|  = |P^{-1}||A-\lambda E||P| = |A-\lambda E|$

        **推论**
        若 $n$ 阶矩阵 $A$ 与对角阵 $\Lambda = \left|\begin{array}{l} \lambda_{1}&&&\\&\lambda_{2}&&\\&&\ddots&\\&&&\lambda_{n} \end{array}\right|$ 相似，则 $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ 是 $A$ 的 $n$ 个特征值
        >因为 $\lambda_{1},\lambda_{2},\cdots,\lambda_{n}$ 是对角矩阵 $\Lambda$ 的 $n$ 个特征值，由之前定理可知也是 $A$ 的特征值

    * **对角化**
        * **第二章的可逆矩阵性质**
            >$A = P\Lambda P^{-1},A^{k} = P\Lambda^{k} P^{-1}$

            对于 $A$ 的多次多项式
            >$\varphi(A) = P\varphi(\Lambda)P^{-1}$

            对于对角阵 $\Lambda$
            >$\Lambda^{k} = \left|\begin{array}{l} \lambda_{1}^{k}&&&\\&\lambda_{2}^{k}&&\\&&\ddots&\\&&&\lambda_{n}^{k} \end{array}\right|,\varphi(\Lambda)=\left|\begin{array}{l} \varphi(\lambda_{1})&&&\\&\varphi(\lambda_{2})&&\\&&\ddots&\\&&&\varphi(\lambda_{n}) \end{array}\right|$

        * **定义**
            对 $n$ 阶矩阵 $A$，寻求相似变换矩阵 $P$，使 $P^{-1}AP = \Lambda$ 为对角阵，称为把矩阵 $A$ **对角化**

            设 $f(\lambda)$ 是矩阵 $A$ 的特征多项式，则 $f(A)=O$
            >若 $A$ 与对角阵相似
            >则有可逆矩阵使 $P^{-1}AP = \Lambda = diag(\lambda_{1},\lambda_{2},\cdots,\lambda_{n})$
            >其中 $\lambda_{i}$ 为 $A$ 的特征值，所以 $f(\lambda_{i}) = 0$
            >$A = P\Lambda P^{-1}$
            >$f(A) = Pf(\Lambda)P^{-1} = P \left|\begin{array}{l} f(\lambda_{1})&&\\&\ddots&\\&&f(\lambda_{n}) \end{array}\right| P^{-1} = POP^{-1} = O$

        * **对角化的充要条件**
            $P^{-1}AP = \Lambda$
            >矩阵 $P$ 用列向量表示 $P=(p_{1},p_{2},\cdots,p_{n})$
            >因为 $P^{-1}AP = \Lambda$ 所以 $AP=P\Lambda$ 即
            >$A(p_{1},p_{2},\cdots,p_{n}) = p_{1},p_{2},\cdots,p_{n} \left|\begin{array}{l} \lambda_{1}&&&\\&\lambda_{2}&&\\&&\ddots&\\&&&\lambda_{n} \end{array}\right|=(\lambda_{1}p_{1},\lambda_{2}p_{2},\cdots,\lambda_{n}p_{n})$
            >所以 $Ap_{i} = \lambda_{i}p_{i} \ (i=1,2,\cdots,n)$
            >可见 $\lambda_{i}$ 是矩阵 $A$ 的特征值，$p_{i}$ 是特征值对应的特征向量
            >为了保证 $P$ 可逆，特征向量集 $p_{1},p_{2},\cdots,p_{n}$ 必须线性无关

            $n$ 阶矩阵 $A$ 与对角阵相似的充要条件是 $A$ 有 $n$ 个**线性无关的特征向量**
            \
            如果 $n$ 阶矩阵 $A$ 的 $n$ 个特征值互不相等，则 $A$ 与对角阵相似
            **注意**：有重根时，基础解系向量的个数可能会有多个（基础解系向量线性无关），所以也会有 $n$ 个**线性无关的特征向量**，可以对角化
            \
            例：$A=\left|\begin{array}{l} 0&0&1\\1&1&x\\1&0&0 \end{array}\right|$，$x$ 为何值时，矩阵 $A$ 可以对角化
            >$|A-\lambda E| = \left|\begin{array}{l} -\lambda&0&1\\1&1-\lambda&x\\1&0&-\lambda \end{array}\right| = (1-\lambda)\left|\begin{array}{l} -\lambda&1\\1&-\lambda \end{array}\right| = -(\lambda-1)^{2}(\lambda+1)$
            >$\lambda_{1}=-1, \lambda_{2}=\lambda_{3}=1$
            >当 $\lambda_{1}=-1$ 时，行最简形 $\left|\begin{array}{l} 1&0&1\\0&1&\frac{1-x}{2}\\0&0&0 \end{array}\right|$，基础解集个数 $n-r=3-2=1$，所以对应的特征向量为一个
            >所以矩阵要能对角化，必须使 $\lambda_{2}=\lambda_{3}=1$ 有两个线性无关的解（两个线性无关特征向量）
            >当 $\lambda_{2}=\lambda_{3}=1$ 时，行最简形 $\left|\begin{array}{l} 1&0&-1\\0&0&x+1\\0&0&0 \end{array}\right|$，如果要得到两个基础解，那么 $R(A-E)=1$，则 $x+1=0,x=-1$

4. **对称矩阵的对角化**
    * **对称矩阵的特征向量**
        设 $\lambda_{1},\lambda_{2}$ 是对称矩阵 $A$ 的两个特征值，$p_{1},p_{2}$ 是对应的**特征向量**，若 $\lambda_{1} \neq \lambda_{2}$，则 $p_{1}$ 与 $p_{2}$ **正交**
        >$\lambda_{1}p_{1}=Ap_{1},\lambda_{2}p_{2}=Ap_{2}$
        >因为 $A$ 对称，所以 $A=A^{T}$
        >$\lambda_{1}p_{1}^{T}=(\lambda_{1}p_{1})^{T} = (Ap_{1})^{T} = p_{1}^{T}A^{T} = p_{1}^{T}A$
        >两边乘以 $p_{2}$
        >$\lambda_{1}p_{1}^{T}p_{2} = p_{1}^{T}Ap_{2} = p_{1}^{T}(\lambda_{2}p_{2}) = \lambda_{2}p_{1}^{T}p_{2}$
        >$(\lambda_{1}-\lambda_{2})p_{1}^{T}p_{2}=0$
        >因为 $\lambda_{1} \neq \lambda_{2}$，所以 $p_{1}^{T}p_{2}=0$，那么 $p_{1}$ 与 $p_{2}$ 正交

    * **对称矩阵的对角化**
        设 $A$ 为 $n$ 阶对称矩阵，则必有正交矩阵 $P$，使 $P^{-1}AP = P^{T}AP = \Lambda$，其中 $\Lambda$ 是以 $A$ 的 $n$ 个特征值为为对角元的对角阵

        **推论**：设 $A$ 为 $n$ 阶对称矩阵，$\lambda$ 是 $A$ 的特征方程的 $k$ 重根，则矩阵 $A-\lambda E$ 的秩 $R(A-\lambda E) = n-k$，从而对应特征值 $\lambda$ 恰有 $k$ 个线性无关的特征向量

    * **对称阵对角化的步骤**
        (1) 求出 $A$ 的全部互不相等特征值 $\lambda_{1},\cdots,\lambda_{s}$




        
