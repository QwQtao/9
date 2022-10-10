# 9
优化昨天的100-200素数


#include<math.h>

int main()
{
	int i = 0;
	int count = 0;
	for (i = 100; i <= 200; i++)
	{
		//判读i是否为素数
		//素数判断的规则
		//1.试除法
		//产生2->i-1
		//sqrt是库函数-开平方的库函数
		int j = 0;
		for (j = 2; j<=sqrt (i); j++)
		{
			if (i % j == 0)
			{
				break;
			}
		}
		if (j>sqrt(i))
		{
			count++;
			printf("%d ", i);
		}
	}
	printf("\ncount=%d\n", count);
	return 0;
}
