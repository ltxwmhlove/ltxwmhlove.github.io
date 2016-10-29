---
layout: post
title: "Judge Odd or Even."
date: 2016-10-26
excerpt: "Even And Odd"
tags: [C++]
comments: true
---

对于一个数的奇偶性判断，看似简单。但当数字特别大的时候，就需要另想方法了。

稍微有些经验的人，应该都会想到字符串吧。

### 简单的奇偶判断

{% highlight c++ %}
#include <stdio.h>
#include <iostream>

int main()
{
	int n;
	scanf("%d",&n);
	
	if(n%2==0)
	{
		printf("even");
	}
	
	else printf("odd");
	
	return 0;
}
{% endhighlight %}

### 数据较大时的奇偶判断。

#### 思想就是求最后一位数能否被2整除。

{% highlight c++ %}
#include<stdio.h>

#include<string.h>

int main ()

{

    char n[10000];

    scanf("%s",n);

    if(n[strlen(n)-1]%2==0)

    printf("even");

    else

    printf("odd");

    return 0;

}
{% endhighlight %}