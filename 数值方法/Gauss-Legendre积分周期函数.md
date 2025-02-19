随着积分区间覆盖的周期越来越多，积分精度下降。

对一个分段函数积分，测试结果如下：

```
   Periods            5 Points           10 Points           20 Points              Theory
------------------------------------------------------------------------------------------
         1       -0.5390716132       -1.1034581015       -1.1318475808       -1.1415926536
         2       -1.4742651690       -1.0426639253       -1.1529849783       -1.1415926536
         3       -0.2663948329       -0.9594066852       -1.0780252246       -1.1415926536
         4       -0.8611500905       -0.5595567668       -1.2619508386       -1.1415926536
         5       -0.2697799065       -0.9132904614       -1.0521988267       -1.1415926536
         6       -0.5208775865       -1.5047843734       -1.0115137673       -1.1415926536
         7       -0.5951714924       -2.2568219383       -0.4384033120       -1.1415926536
         8       -0.4849419704       -0.8580550500       -1.7119300956       -1.1415926536
         9       -1.1999218212       -1.3917587434       -0.8404182333       -1.1415926536
        10       -0.6983090093       -0.4944981773       -0.8911395404       -1.1415926536
```

测试代码如下：

```cpp
#include <iostream>
#include <cmath>
#include <iomanip>
#include <valarray>
#include <tuple>  

using namespace std;  

tuple<valarray<double>, valarray<double>> gauss_legendre(int n, double a, double b, double EPS = 1e-10)
{
    std::valarray<double> x(n);
    std::valarray<double> w(n);
    double z, z1, p1, p2, p3, pp;
    int m = (n + 1) / 2;
    double xm = 0.5 * (b + a);
    double xl = 0.5 * (b - a);
    for (int i = 1; i <= m; i++) {
        z = cos(3.14159265358979323846 * (i - 0.25) / (n + 0.5));
        z1 = 0.0;
        do {
            p1 = 1.0;
            p2 = 0.0;
            for (int j = 1; j <= n; j++) {
                p3 = p2;
                p2 = p1;
                p1 = ((2.0 * j - 1.0) * z * p2 - (j - 1.0) * p3) / j;
            }
            pp = n * (z * p1 - p2) / (z * z - 1.0);
            z1 = z;
            z = z1 - p1 / pp;
        } while (fabs(z - z1) > EPS);
        x[i - 1] = xm - xl * z;
        x[n - i] = xm + xl * z;
        w[i - 1] = 2.0 * xl / ((1.0 - z * z) * pp * pp);
        w[n - i] = w[i - 1];
    }
    return std::make_tuple(x, w);
} 

// 带突变的周期函数
double complex_periodic(double x)
{
    // 将x映射到[0,2π]区间
    double mapped_x = std::fmod(x, 2*M_PI);
    if(mapped_x < 0) mapped_x += 2*M_PI;
    // 分段函数定义
    if(mapped_x <= M_PI)
    {
        return std::sin(mapped_x);
    }
    else
    {
        return -1.0;
    }
}

  

double gauss_legendre_integrate(int n_points, double a, double b)
{
    auto [nodes, weights] = gauss_legendre(n_points, -1, 1);
    double c1 = (b - a) / 2.0;
    double c2 = (b + a) / 2.0;
    double sum = 0.0;
    for(int i = 0; i < n_points; i++) {
        double x = c1 * nodes[i] + c2;
        sum += weights[i] * complex_periodic(x);
    }
    return c1 * sum;
}
  

int main() {
    const double PI = std::acos(-1.0);
    std::cout << std::setw(10) << "Periods"
              << std::setw(20) << "3 Points"
              << std::setw(20) << "5 Points"
              << std::setw(20) << "7 Points"
              << std::setw(20) << "10 Points"
              << std::setw(20) << "15 Points"
              << std::setw(20) << "20 Points"
              << std::setw(20) << "Theory" << "\n";
    std::cout << std::string(90,'-') << "\n"; 

    double theory = 2.0 - PI;
  
    for(int periods = 1; periods <= 10; periods++) {
        double res3 = gauss_legendre_integrate(3, 0, 2*PI*periods);
        double res5 = gauss_legendre_integrate(5, 0, 2*PI*periods);
        double res7 = gauss_legendre_integrate(7, 0, 2*PI*periods);
        double res10 = gauss_legendre_integrate(10, 0, 2*PI*periods);
        double res15 = gauss_legendre_integrate(15, 0, 2*PI*periods);
        double res20 = gauss_legendre_integrate(20, 0, 2*PI*periods);
        std::cout << std::fixed << std::setprecision(10)
                  << std::setw(10) << periods
                  << std::setw(20) << res3/periods
                  << std::setw(20) << res5/periods
                  << std::setw(20) << res7/periods
                  << std::setw(20) << res10/periods
                  << std::setw(20) << res15/periods
                  << std::setw(20) << res20/periods
                  << std::setw(20) << theory << "\n";
    }
    return 0;
}
```
