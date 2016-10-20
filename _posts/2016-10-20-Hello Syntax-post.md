---
layout: post
title: "Hello C++!"
date: 2016-10-20.
excerpt: "Test Syntax Highlights"
tags: [C++]
comments: true
---

One Game One Life肯定会是我主要更新的内容。

但不能耽误学习啊！

我还会写写高数题目什么的吧。

有兴趣多来看看。

先测试一下代码高亮。

### Hello C++

{% highlight c++ %}
#include <iostream>

int main()
{
	std::cout<<"Hello C++!";
	return 0;
}

{% endhighlight %}


就这样结束感觉有点水。

那就再测试一下长代码吧。

###单词翻转

大概效果是输入I love you，输出you love I.

{% highlight c++ %}
#include <stdio.h>  
#include <string.h> 

int main(int argc,char *argv[])  
 {  
     char strings[100];  
     int i,t,n;  
   
     gets(strings);  
     n=strlen(strings);  
    
	 i=n-1;  
     while(i-->=0)  
     {  
         if(strings[i]==' ')  
         {  
             for(t=i+1;t<n;t++)  
            {  
                 printf("%c",strings[t]);  
             }  
             printf(" ");  
             n=i;  
         }  
     }  
    
  
     for(t=0;t<n;t++)  
     {  
         printf("%c",strings[t]);  
     }  
     printf("\n");  

     return 0;
}  

{% endhighlight %}

