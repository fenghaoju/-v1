#include<stdio.h>
#include<string.h>
int main()
{
	char strExp[]="1+2+2+1+2+5+4-1-3+4-8";
	int a=strExp[0]-'0';
	int i;
	for(i=1;i<strlen(strExp);i++)
	{
	    if(strExp[i]=='+')
		{
			int x=strExp[i+1]-'0';
			a=a+x;
			i++;
		}
		else if(strExp[i]=='-')
		{
			int y=strExp[i+1]-'0';
			a=a-y;
			i++;
		}	
	}
	printf("%d",a);
	return 0; 
}
