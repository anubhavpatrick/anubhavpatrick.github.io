---
layout: post
title:  "RCS 101 Unit 3"
date:   2016-10-05 09:15:36 +0530
categories: jekyll update
---

<strong> Assignment 3.1 </strong><br>
<a href="http://anubhavpatrick.github.io/RCS101Assignment3.1.pdf "> Click here to download assignment 3.1</a><br>
<br>

<strong> Assignment 3.2 </strong><br>
<a href="http://anubhavpatrick.github.io/RCS101Assignment3.2.pdf "> Click here to download assignment 3.2</a><br>
<br>

<strong>Unit 3 Notes </strong><br>
<a href="http://anubhavpatrick.github.io/RCS101Unit3Notes.pdf"> Click here to download Unit 3 Notes and Question Bank </a><br>


<h3> Assignment 3.2 Programming Solution </h3><br>
1. WAP to find out whether a number is prime number.<br>
{% highlight c %}
#include<stdio.h>
#include<stdlib.h>
int main()
{
	int i,n;
	printf("Enter a number: ");
	scanf("%d", &n);
	for(i=2;i<n;i++)
	{	
		if(n%i==0)
		{
			printf("%d is not a prime number\n",n);
			exit(0);//To terminate the prog
		}
	}
	printf("%d is a prime number\n",n);
	return 0;
}

{% endhighlight %}
2. WAP to find sum of digits of a number. <br>

