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
