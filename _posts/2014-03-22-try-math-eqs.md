---
layout: post
title:  "Math, Chinese, Gist and Code Highlight with Jekyll"
date:   2014-03-22 18:41:09
categories: demo
mathjax: true
languages:
  - matlab
  - r
---

# Math Equations Demo

$$ \begin{aligned} \dot{x} & = \sigma(y-x) \\ \dot{y} & = \rho x - y - xz \\ \dot{z} & = -\beta z + xy \end{aligned} $$

source code in $\LaTeX$:

{% highlight latex %}
\begin{aligned} \dot{x} & = \sigma(y-x) \\ 
\dot{y} & = \rho x - y - xz \\ 
\dot{z} & = -\beta z + xy \end{aligned}
{% endhighlight %}

# Test Chinese

测试中文：你好！
:heart_eyes:
:smile:

Notice the 絵文字(えもじ, Emoji) icons~!
haha~

# highlight.js Demo

## Python
{% highlight python %}
def spam(i, j, k):
	return i * j - k
{% endhighlight %}

## Ruby
{% highlight ruby %}
def foo
  puts 'foo'
end
{% endhighlight %}


## Gist Demo
{% gist 10532853 %}
点击左下角的文件名可以在Github上查看改段代码（**评论**和**查看历史**）。在Github上修改也会**自动更新**到这里。

## highlight.js R code.

{% highlight r linenos %}
#  3.5
setwd("D:/")
a = read.table("m-intc7308.txt", head = T)
# 调整成时间序列数据
ts1 = ts(data = a[[2]], start = 1973, frequency = 12)	
lts1 = log(1 + ts1)
# 转化成对数收益率
acf(lts1)
# 观察 ARIMA 模型的阶数 (定阶)
pacf(lts1)
# acf 定 MA(q) 的阶数, pacf 定 AR(p) 的阶数
# 检验是否存在条件异方差
plot(lts1^2)
# 检验是否存在条件异方差
Box.test(lts1^2)										
myspec = ugarchspec(variance.model=list(garchOrder = c(1,1)), 
    mean.model=list(armaOrder = c(0,0)))
# 建立 GARCH 模型
myfit = ugarchfit(myspec, lts1)							
myfit
# 向前 5 步预测
fc = ugarchforecast(myfit, lts1, n.ahead = 5)			
fc
# Now try a very very very long long long long long long long long long long long long long long long long long long long long long long line.
{% endhighlight %}

It seems that very limited keywords/commands are recognized. Various user defined functions available in addon packages, like `ugarchfit`, are not expected to be recognized, but what about `setwd`?