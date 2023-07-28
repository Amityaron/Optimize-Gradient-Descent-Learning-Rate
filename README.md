### Optimize-Gradient-Descent-Learning-Rate
Optimize Gradient Descent Learning Rate:
* Using descent algorithm for $f(x,y)$ with Iterative Gradient Descent Algorithm:
* $f(x,y)=100\cdot(y-x)^2+(1-x)^2$
* $Z_0$ = Initial guess
 $$Z_{n+1}=Z_{n}-\alpha\cdot\nabla f(Z_{n})$$ 
 To find the optimal α of the function with [Golden Section Search Algorithm](https://en.wikipedia.org/wiki/Golden-section_search) on the interval $[0,1]$

**Golden Section Search Algorithm procedure:**  <br />
$g(\alpha) = f(Z^{n} - \alpha \cdot \nabla f(Z^{n}))$
The iterative algorithm get $g(\alpha),[m,M],tolerance$. <br />
1. Calculate the points $x_1=M-\varphi*(M-m)$  and $x_2=m+\varphi*(M-m)$ when $\varphi=\frac{1+\sqrt{5}}{2}$. <br />
2. Calculate $f(x_1)$  and $f(x_2)$. <br />
3. If $f(x_2)>f(x_1)$ update the boundaries and the points: $M=x_2$ and $x_2=x_1$ and $x_1=M-\varphi*(M-m)$. <br />
4. Otherwise if $f(x_2)\le(x_1)$ update the boundaries and the points: $m=x_1$ and $x_2=m+\varphi*(M-m)$. <br />
5. Repeat step 2,4 until $|M-m|\le{tolerance}$. <br />
6. return $\frac{|M-m|}{2}$ <br />

 
<img src="https://github.com/Amityaron/Optimize-Gradient-Descent-Learning-Rate/blob/main/lab5%20.png" width="60%" height="30%">
