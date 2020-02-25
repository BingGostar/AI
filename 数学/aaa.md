5. **二次型及其标准形**
    * **二次型**
        含有 $n$ 个变量 $x_{1},x_{2},\cdots,x_{n}$ 的二次齐次函数，称为**二次型**
        >$f=a_{11}x_{1}^{2}+a_{12}x_{1}x_{2}+\cdots+ a_{1n}x_{1}x_{n}+a_{21}x_{2}x_{1}+a_{22}x_{2}^{2}+\cdots+ a_{2n}x_{2}x_{n}+\cdots+a_{n1}x_{n}x_{1}+a_{n2}x_{n}x_{2}+\cdots+ a_{nn}x_{n}x_{n}$
        >取 $a_{ij} = a_{ji}$
        >$f = \sum \limits^{n}_{i,j=1} a_{ij}x_{i}x_{j}$

        对于二次型，寻求可逆线性变换
        >$\left\lbrace\begin{array}{l} x_{1}=c_{11}y_{1}+c_{12}y_{2}+\cdots+c_{1n}y_{n} \\ x_{2}=c_{21}y_{1}+c_{22}y_{2}+\cdots+c_{2n}y_{n} \\ \cdots \\ x_{n}=c_{n1}y_{1}+c_{n2}y_{2}+\cdots+c_{nn}y_{n}\end{array}\right.$
        >可以理解为 $x_{i}$ 是另一个变量 $y_{i}$ 的线性组合，注意 $C=(c_{ij})$ 不是对称矩阵，

        使二次型只含平方项（将可逆线性变换带入二次型）
        >$f=k_{1}y_{1}^{2}+k_{2}y_{2}^{2}+\cdots+k_{n}y_{n}^{2}$


        如果只含平方的二次型，称为二次型的**标准形**
        >$f=k_{1}y_{1}^{2}+k_{2}y_{2}^{2}+\cdots+k_{n}y_{n}^{2}$

        如果标准形的系数 $k_{1},k_{2},\cdots,k_{n}$ 只在 $1,-1,0$ 三个数中取值，称为二次型的**规范性**
        >$f=y_{1}^{2}+\cdots+y_{p}^{2}-y_{p+1}^{2}-\cdots-y_{r}^{2}$

    * **二次型的矩阵表示为**
        >$f=(x_{1},x_{2},\cdots,x_{n})\left|\begin{array}{l}a_{11}x_{1}+a_{12}x_{2}+\cdots+ a_{1n}x_{n} \\ a_{21}x_{1}+a_{22}x_{2}+\cdots+ a_{2n}x_{n} \\ \vdots \\ a_{n1}x_{1}+a_{n2}x_{2}+\cdots+ a_{nn}x_{n} \end{array}\right|=(x_{1},x_{2},\cdots,x_{n})\left|\begin{array}{l}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\vdots&\vdots&&\vdots\\a_{n1}&a_{n2}&\cdots&a_{nn}\end{array}\right| \left|\begin{array}{l}x_{1}\\x_{2}\\\vdots\\x_{n}\end{array}\right|$

        >$$A=\left|\begin{array}{l}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\vdots&\vdots&&\vdots\\a_{n1}&a_{n2}&\cdots&a_{nn}\end{array}\right|, \ \ \ x = \left|\begin{array}{l}x_{1}\\x_{2}\\\vdots\\x_{n}\end{array}\right|$$

        二次型记作，矩阵 $A$ 是对称矩阵
        >$$f=x^{T}Ax$$

        >注意区分相似矩阵 $P^{-1}AP=B$ 的概念，$P$ 为矩阵
        
        例如：$f=x^{2}-3z^{2}-4xy+yz$
        >$f=(x,y,z)\left|\begin{array}{l} 1&-2&0\\-2&0&\frac{1}{2}\\0&\frac{1}{2}&-3 \end{array}\right| \left|\begin{array}{l} x\\y\\z \end{array}\right|$

        任给一个二次型，就唯一确定一个对称阵，反之，一个对称阵也可以唯一确定一个二次型
        
    * **二次型变成标准型**
        **合同矩阵**
        >设 $A$ 和 $B$ 是 $n$ 阶矩阵，若有可逆矩阵 $C$，使 $B=C^{T}AC$，则称矩阵 $A$ 与 $B$ 合同

        **标准形变换**
        >$x=Cy$
        >$f = x^{T}Ax$
        >上式带入下式
        >$f= x^{T}Ax=(Cy)^{T}ACy = y^{T}(C^{T}AC)y$
        >如果要将二次型变成标准形，则
        >$f = y^{T}(C^{T}AC)y = k_{1}y_{1}^{2}+k_{2}y_{2}^{2}+\cdots+k_{n}y_{n}^{2}$
        >$=(y_{1})$

        记 $C=(c_{ij})$，可逆变换 $x=Cy$
        >$f=x^{T}Ax=(Cy)^{T}ACy = y^{T}(C^{T}AC)y$