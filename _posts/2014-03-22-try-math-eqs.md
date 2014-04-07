---
layout: post
title:  "Try Math inside jekyll!"
date:   2014-03-22 18:41:09
categories: test
mathjax: true
languages:
  - matlab
  - r
---

# Test math equations


$$ \begin{aligned} \dot{x} & = \sigma(y-x) \\ \dot{y} & = \rho x - y - xz \\ \dot{z} & = -\beta z + xy \end{aligned} $$

source code in $\LaTeX$:

{% highlight latex %}
\begin{aligned} \dot{x} & = \sigma(y-x) \\ 
\dot{y} & = \rho x - y - xz \\ 
\dot{z} & = -\beta z + xy \end{aligned}
{% endhighlight %}


# Test code highlight

### Python

{% highlight python %}
def spam(i, j, k):
	return i * j - k
{% endhighlight %}

### Ruby

{% highlight ruby %}
def foo
  puts 'foo'
end
{% endhighlight %}


# Test Chinese

测试中文：你好！
:heart_eyes:
:smile:

Notice the Emoji icons~!
haha
