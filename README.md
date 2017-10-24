#include<stdio.h>
#include<stdlib.h>
#include<string.h>

#if 0
//浅拷贝
int main()
{
	char buf[100];
	char *str[3];//指针数组
	int i;
	for(i = 0;i < 3;i++)
	{
		scanf("%s",buf);
		str[i] = buf;
	}
	for(i = 0;i < 3;i++)
	{
		printf("%s\n",str[i]);
	}

	return 0;
}
#endif

//深拷贝
int main()
{
	char buf[100];
	char *str[3];
	int i;
	for(i = 0;i < sizeof(str)/sizeof(str[0]);i++)
	{
		scanf("%s",buf);
		str[i] = (char *)malloc(strlen(buf)+1);
		strcpy(str[1],buf);
	}
	for(i = 0;i < 3;i++)
	{
		printf("%s\n",str[i]);
	}

	return 0;
}
