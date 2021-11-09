# ExerciseCode
C
#include <stdio.h>
#include <stdlib.h>
#include <string.h>


int main(void)
{
	int arr[] = { 1,2,3,4,5,6,7,8,9,10 };
	int sz = sizeof(arr) / sizeof(arr[0]);
	int find;
	scanf("%d",&find);
	int left = 0;
	int right = sz - 1;
	
	while (left <= right)
	{
		int mid = (left+right)/2;
		if (arr[mid] > find)
		{
			right = mid - 1;
		}
		else if(arr[mid] < find)
		{
			left = mid + 1;
		}
		else
		{
			printf("找到了,下标为%d",mid);
			break;
		}
	}
	if (left > right)
	{
		printf("没找到");
	}

		
	return 0;
}
