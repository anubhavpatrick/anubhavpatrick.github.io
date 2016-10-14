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

<strong> Patterns and Designs Presentation<strong><br>
<a href="http://anubhavpatrick.github.io/Patterns\ and\ Design\ using\ C\ Language.pptx"> Click here to download presentation on patterns and designs </a><br>

<strong> Recursion Presentation </strong>
<a href="ttp://anubhavpatrick.github.io/Recursion.pptx"> Click here to download presentation on Recursion </a><br>
<h3> Assignment 3.1 Programming Solution </h3><br>
WAP to find out whether a given number is a multiple of 11 or not.<br>
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	int num;
	printf("Enter a number\n");
	scanf("%d",&num);
	if(num%11==0)
		printf("Number is divisible by 11\n");
	else
		printf("Number is not divisible by 11\n");
}
{% endhighlight %}
WAP to take three angles of a triangle as input and find out whether the triangle formed is a valid triangle or not.<br>
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	float a1,a2,a3;
	printf("Enter three angles of the triangle: ");
	scanf("%f%f%f",&a1,&a2,&a3);
	if((a1+a2+a3)==180)
		printf("Valid Triangle\n");
	else
		printf("Invalid Triangle\n");
}
{% endhighlight %}
WAP to solve the roots of a quadratic equation. Roots are given by<br>
𝑥=(−𝑏±(𝑏^2−4𝑎𝑐)^1/2)/2𝑎<br>
Check if the term b^2-4ac < 0 then roots are imaginary. Display appropriate message on the screen. Otherwise find the roots and display them to the user.
{% highlight c linenos %}
#include<stdio.h>
#include<math.h>
void main()
{
	float a,b,c,det,r1,r2;
	printf("Enter the values of a, b and c\n");
	scanf("%f%f%f",&a,&b,&c);
	det=b*b-4*a*c;
	if(det<0)
		printf("Roots are imaginary\n");
	else
	{
		r1=(-b+sqrt(det))/2*a;
		r2=(-b-sqrt(det))/2*a;
		printf("Roots are %f and %f\n",r1,r2);
	}
}
{% endhighlight %}
WAP in C to read an integer number from keyboard, add 1 to it if the number read is even, again add 1 to it if the number is less than 20, otherwise keep the number unchanged and print the final result.
[Hint: You have to use nested if]<br>
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	int num;
	printf("Enter a number\n");
	scanf("%d",&num);
	if(num%2==0)
	{
		num=num+1;
		if(num<20)
			num=num+1;
	}
	printf("Num is now %d\n",num);
}

{% endhighlight %}
WAP to calculate hospital bill according to following conditions:<br>
a. If age<=10 No charge<br>
b. If age>=11 and age<=40 100 Rs<br>
c. If age>=41 and age<=60 75 Rs<br>
d. If age>=61 50 Rs<br>
{% highlight c linenos %}
#include<stdio.h>
int main()
{
	int age,bill;
	printf("Enter age: ");
	scanf("%d",&age);
	if(age<=10)
		bill=0;
	else if(age<=40)
		bill=100;
	else if(age<=60)
		bill=75;
	else
		bill=50;
	printf("Hospital Bill is %d\n",bill);
	return 0;
}
{% endhighlight %}

WAP using switch statement to calculate area of circle, rectangle and triangle. You must ask the user for a choice e.g., 1 for area of circle, 2 for area of rectangle and 3 for area of a triangle. Based on the choice of the user, you must perform the necessary operation. <br>
{% highlight c linenos %}
#include<stdio.h>
#define PI 22.0/7.0
void main()
{
	int choice;
	float r,areaCircle,l,b,areaRect,base,h,areaTriangle;
	printf("Enter your choice:\n");
	printf("1. To find area of circle\n");
	printf("2. To find area of rectangle\n");
	printf("3. To find area of trangle\n");
	scanf("%d",&choice);
	switch(choice)
	{
		case 1: printf("Enter radius: ");
				scanf("%f",&r);
				areaCircle=PI*r*r;
				printf("Area of circle is %f\n",areaCircle);
				break;
		case 2: printf("Enter length and breadth: ");
				scanf("%f%f",&l,&b);
				areaRect=l*b;
				printf("Area of rectangle is %f\n",areaRect);
				break;
		case 3: printf("Enter base and height: ");
				scanf("%f%f",&base,&h);
				areaTriangle=0.5*base*h;
				printf("Area of triangle is %f\n",areaTriangle);
				break;
		default: printf("Sorry wrong choice\n");

	}
}

{% endhighlight %}
<h3> Assignment 3.2 Programming Solution </h3><br>
WAP to find out whether a number is prime number.<br>
{% highlight c linenos %}
#include<stdio.h>
#include<stdlib.h>
void main()
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
}

{% endhighlight %}
WAP to find sum of digits of a number.
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	int n,r,sum=0;
	printf("Enter a number: ");
	scanf("%d",&n);
	while(n!=0)
	{	
		r=n%10; //Extracting the last digit
		sum=sum+r;	//Adding the digit
		n=n/10; //Reducing the length of the n by 1
		
	}
	printf("Sum of digits of is %d\n",sum);
}
{% endhighlight %}

WAP in ‘C’ that will read a positive number from the keyboard and print it in reverse
order.
E.g., 24578 output: 87542 <br>
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	int n,r,rev=0;
	printf("Enter a number: ");
	scanf("%d",&n);
	while(n!=0)
	{	
		r=n%10; //Extracting the last digit
		rev=rev*10+r;	//creating a new number using r
		n=n/10; //Reducing the length of the n by 1
		
	}
	printf("Reverse of number is %d\n",rev);
}
{% endhighlight %}

WAP to print sum of following series:
1/x + 1/(x^2) + 1/(x^3) ……………….. 1/(x^n)<br>
E.g., if the user enters x=2 and n=3
Your program should display => 0.875
<br>
{% highlight c linenos %}
#include<stdio.h>
#include<math.h>
void main()
{
	int x,n,i;
	float sum=0.0;
	printf("Enter the value of x: ");
	scanf("%d",&x);
	printf("Enter the value of n: ");
	scanf("%d",&n);
	for(i=1;i<=n;i++)
		sum=sum+1.0/pow(x,i);
	printf("Sum of series is: %f\n",sum);
}
{% endhighlight %}

WAP in C to print following pattern:<br>
1<br>
2 3<br>
4 5 6<br>
7 8 9 10
<br>
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	int i,j,count=1;
	for(i=1;i<=4;i++) //It controls rows
	{
		for(j=1;j<=i;j++) //It controls columns
		{
			printf("%d ",count);
			count++;
		}
		printf("\n");
	}
}
{% endhighlight %}
WAP to find out tax on an item @10% its cost. After the first item you must ask the user
whether he wants to continue by typing ‘Y’ through the keyword. If he types ‘Y’ then
again find the tax on second item and so on.
[Hint. Your loop needs to be executed atleast once according to question so use dowhile]
<br>
{% highlight c linenos %}
#include<stdio.h>
void main()
{
	float cost,tax;
	char choice;
	do //do-while loop will execute atleast once
	{ 
		printf("Enter cost of item: ");
		scanf("%f",&cost);
		tax=0.1*cost;
		printf("Tax on item is %f\n",tax);
		printf("Do you want to continue (Y/N)");
		scanf(" %c",&choice);
	}while(choice=='Y');
}
{% endhighlight %}

Write a C program to find the factorial of a given number using recursion
<br>
{% highlight c linenos %}
#include<stdio.h>
int fact(int n); //Function Decleration or Function Prototype
void main()
{
	int num,factorial;
	printf("Enter a number: ");
	scanf("%d",&num);
	factorial=fact(num); //Function Call
	printf("Factotial of %d is %d\n",num,factorial);
}
int fact(int num)// Function Definition
{
	int i,f=1;
	for(i=num;i>=1;i--)
		f=f*i;
	return f;
}
{% endhighlight %}

WAP to find GCD of a given number using functions and using recursion.<br>
<strong> Using Functions Only </strong>
<br>
{% highlight c linenos %}
#include<stdio.h>
int gcd(int p, int q);
void main()
{
	int x,y,g;
	printf("Enter 2 numbers: ");
	scanf("%d%d",&x,&y);
	if(x>y)
		g=gcd(x,y);
	else
		g=gcd(y,x);
	printf("GCD=%d\n",g);
}
int gcd(int p, int q)
{
	int r=1,g;
	while(r!=0)
	{
		r=p%q;
		if(r==0)
		{
			g=q;
			break;//To come out of the loop
		}
		p=q;
		q=r;
	}
	return g;
}
{% endhighlight %}
<strong> Using Recusrsion</strong>
{% highlight c linenos %}
#include<stdio.h>
int gcd(int p, int q);
void main()
{
	int x,y,g;
	printf("Enter 2 numbers: ");
	scanf("%d%d",&x,&y);
	if(x>y)
		g=gcd(x,y);
	else
		g=gcd(y,x);
	printf("GCD=%d\n",g);
	return 0;
}
int gcd(int p, int q)
{
	int r;
	r=p%q;
	if(r==0)
		return q;
	else
		return gcd(q,r);
}
{% endhighlight %}
