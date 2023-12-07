#include<sys/times.h>
#include<time.h>
#include<stdio.h>
#include<unistd.h>
#include<sys/wait.h>

int main()
{
	int n,s,c;
	c=fork();
	if(c==0)
	{
		execlp("date","date",NULL);
		
	}
	else
	{
		waitpid(c,&s,WNOHANG);
		if(WIFEXITED(s))
		{
			printf("\n Exit status=>%d",WEXITSTATUS(s));
		}
	}
	return 0;
}
