---
layout: post
title: "简单递归之分解质因数"
date: 2016-11-01
excerpt: "Prime!"
tags: [C++]
comments: true
---

<a href="http://codevs.cn/wiki/solution/?problem_id=1792" style="font-size=25px;">原题。</a>

### 这道题目其实想了有一段时间。因为是要分解出所有的质因子，和之前的一道很水的分解两个不一样。

### 后来想了想，发现可以用递归。先求一个质数，再判断另一个是不是质数，不是就回归。实现代码如下：

{% highlight C++ %}

#include<cstdio>

int a[10000000];
int m, i=1, h;
void f(int n)
{
	for(int j=2;j<=n/2;j++)
	 if(n%j==0)
	 {
	 	a[i]=j;
	 	i++;
	 	return f(n/j);
	 }
	 else if(j==n/2)
	 {
	 	a[i]=n;
	 }
}
int main()
{
	scanf("%d", &m);
	f(m);
	printf("%d=", m);
	for(h=1;h<=i;h++)
	{
		if(h==i)
		 printf("%d", a[h]);
		else
		 printf("%d*", a[h]);
	}
	return 0;
}

{% endhighlight %}

