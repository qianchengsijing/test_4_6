# test_4_6
#include <stdio.h>

计算n的阶乘
int main()
{
	int i = 0;
	int n = 0;
	int ret = 1;
	scanf("%d",&n);
	for(i=1;i<=n;i++)
	{
		ret = ret*i;
	}
	printf("%d\n",ret);
	return 0;
}
计算1！+2！+3！+.....+n!
int main()
{
	第一种算法
	/*int i = 0;
	int n = 0;
	int ret = 1;
	int sum = 0;
	scanf("%d",&n);
	for(i=1;i<=n;i++)
	{
		ret *= i;
		sum += ret;
	}
	printf("%d\n",sum);*/
	第二种算法计算1！+2！+3！+.....+10!
	int i = 0;
	int n = 0;
	int ret = 1;
	int sum = 0;
	for(n=1;n<=10;n++)
	{
		ret = 1;
		for(i=1;i<=n;i++)
		{
			ret *= i;
		}
		sum += ret;
	}
	printf("%d\n",sum);
	return 0;
}
在一个有序数组中查找某个具体的数n（二分查找法）
int main()
{
	int arr[]={1,2,3,4,5,6,7,8,9,10};
	int k = 7;
	int i = 0;
	int sz = sizeof(arr)/sizeof(arr[0]);
	for(i=0;i<sz;i++)
	{
		if(arr[i] == k)
		{
			printf("找到了，下标为：%d\n",i);
            break;
		}
	}
	if(i == sz)
	{
		printf("找不到%\n");
	}
	return 0;
}
int main()
{
	int arr[]={1,2,3,4,5,6,7,8,9,10};
	int k = 0;
	int sz = sizeof(arr)/sizeof(arr[0]);
	int left = 0;
	int right = sz-1;
	while(left <= right)
	{
		int mid = (left+right)/2;
		if(arr[mid] > k)
		{
			right = mid-1;
		}
		else if(arr[mid] < k)
		{
			left = mid+1;
		}
		else
		{
			printf("找到了,下标为：%d\n",mid);
			break;
		}
	}
	if(left > right)
	{
		printf("找不到%\n");
	}
	return 0;
}
编写代码实现多个字符从两端向中间汇聚
#include <string.h>
#include <stdlib.h>
#include <windows.h>
int main()
{
	char arr1[]="hello bit";
	char arr2[]="#########";
	int left = 0;
	int right = strlen(arr1)-1;
	int i = 0;
	while(left<=right)
	{
		arr1[left] = arr2[left];
		arr1[right] = arr2[right];
		printf("%s\n",arr2);
		/*sleep(1000);*/
		system("cls");
		left++;
		right--;
		
	}
	printf("%s\n",arr2);
	return 0;
}
#include <string.h>
int main()
{
	int i = 0;
	char password[]={0};
	for(i=0;i<3;i++)
	{
		printf("请输入>:\n");
		scanf("%s",password);
		if(strcmp(password,"123456") == 0)//strcmp用于比较两个字符串是否相等
		{
			printf("登录成功\n");
			break;
		}
		else 
		{
			printf("密码错误\n");
		}
	}
	if(i == 3)
	{
		printf("三次均错误，退出程序\n");
	}
    return 0;
}
输出三个数，从大到小输出
int main()
{
	int a = 0;
	int b = 0;
	int c = 0;
	scanf("%d%d%d",&a,&b,&c);
	if(a<b)
	{
		int tmp = a;
		a = b;
		b = tmp;
	}
	if(a<c)
	{
		int tmp = a;
		a = c;
		c = tmp;
	}
	if(b<c)
	{
		int tmp = b;
		b = c;
		c = tmp;
	}
	printf("%d %d %d\n",a,b,c);
	return 0;
}
打印3的倍数
打印1-100之间3的倍数
int main()
{
	int i = 0;
	for(i=1;i<=100;i++)
	{
		if(i%3 == 0)
			printf("%d ",i);
	}
	return 0;
}
给定两个数，求两个数的最大公约数
int main()
{
	int a = 0;
	int b = 0;
	int ret = 0;
	scanf("%d%d",&a,&b);
	while(a%b)
	{
		ret = a%b;
		a = b;
		b = ret;
	}
	printf("%d\n",ret);
	return 0;
}
打印闰年1000-2000之间的闰年
int main()
{
	int i = 0;
	int count = 0;
	for(i=1000;i<=2000;i++)
	{
		if((i%4==0 && i%100!=0) || (i%400==0))
		{
			printf("%d ",i);
		    count++;
		}
	}
	
	printf("\ncount = %d\n",count);
	return 0;
}
打印素数（100-200）之间的素数
int main()
{
	int i = 0;
	for(i=100;i<=200;i++)
	{
		int j = 0;
		for(j=2;j<i;j++)
		{
			if(i%j == 0)
				break;
		}
		if(j == i)//只有1和其本身才能被其整除为素数
        {
		    printf("%d ",i);
	    }
	}
	
	return 0;
}
#include <math.h>
int main()
{
	int i = 0;
	int count = 0;
	for(i=100;i<=200;i++)
	{
		int j = 0;
		for(j=2;j<=sqrt(i);j++)
		{
			if(i%j == 0)
				break;
		}
		if(j>sqrt(i))
		{
			printf("%d ",i);
			count++;
		}
	}
	printf("\ncount = %d\n",count);
	return 0;
}
编写1-100中出现了多少个9
int main()
{
	int i = 0;
	int count = 0;
	for(i=1;i<=100;i++)
	{
		if(i/10 == 9)
		{
			printf("%d ",i);
			count++;
		}
		if(i%10 == 9)
		{
			printf("%d ",i);
			count++;
		}
	}
    printf("\ncount = %d\n",count);
	return 0;
}
分数求和（1/1-1/2+1/3-1/4+......+1/99-1/100）
int main()
{
	int i = 0;
	int flag = 1;
	double sum = 0;
	for(i=1;i<=100;i++)
	{
		sum += flag * 1.0/i;
		flag = -flag;
	}
	printf("%lf\n",sum);
	return 0;
}
求10个整数中的最大值
int main()
{
	int arr[]={1,2,3,4,5,6,7,8,9,10};
	int i = 0;
	int max = arr[0];
	int sz = sizeof(arr)/sizeof(arr[0]);
	for(i=0;i<sz;i++)
	{
		if(arr[i] > max)
		{
			max = arr[i];
		}
	}
	printf("max = %d\n",max);
	return 0;
}
打印乘法口诀表
int main()
{
	int i = 0;
	int j = 0;
	int n = 0;
	scanf("%d",&n);
	for(i=1;i<=n;i++)
	{
		for(j=1;j<=i;j++)
		{
			printf("%d*%d = %-2d ",i,j,i*j);
		}
		printf("\n");
	}
	return 0;
}
猜数字游戏
#include <stdlib.h>
#include <time.h>
void menu()
{
	printf("########################\n");
	printf("##### 1.play 0.exit ####\n");
	printf("########################\n");
}
void game()
{
	int ret = 0;
	ret = rand()%100+1;
	
	/*printf("%d\n",ret);*/
	while(1)
	{
		int guess = 0;
		printf("请猜数字>;\n");
		scanf("%d",&guess);
		if(guess > ret)
		{
			printf("猜大了\n");
		}
		else if(guess < ret)
		{
			printf("猜小了\n");
		}
		else
		{
			printf("猜对了\n");
		}
	}
}
int main()
{
	int input = 0;
	srand((unsigned int) time(NULL));
	do
	{
		menu();
		printf("请输入>:\n");
		scanf("%d",&input);
		switch(input)
		{
		case 1:
			game();
			break;
		case 0:
			printf("退出程序\n");
			break;
		default:
			printf("输入错误\n");
			break;
		}
	}while(input);
	return 0;
}
一个关机程序
#include <stdlib.h>
#include <string.h>
int main()
{
	char input[]={0};
	system("shutdown -s -t 60");
	again:
	printf("请注意，你的电脑将在一分钟内关机，如果输入我是猪，就取消关机，请输入：\n");
	scanf("%s",input);
	if(strcmp(input,"我是猪") == 0)
	{
		system("shutdown -a");
	}
	else
		goto again;
	return 0;
}
