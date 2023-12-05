#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>
#include<string.h>
#include<signal.h>

void Sh();

int main()
{
	int n;
	n=fork();
	if(n==0)
	{
		printf("\n  Child Process");
		sleep(2);
		printf("\n Child sent msg");
		fflush(stdout);
		kill(n,SIGALRM);
		sleep(5);
		printf("\nchild Exit");
		fflush(stdout);
		sleep(2);
	}
	else
	{
		signal(SIGALRM,Sh);
		wait();
		printf("\nParent Exit");
		fflush(stdout);
	
	
	}
	return 0;
}

void Sh()
{
	printf("\n ALRM Fired");
	fflush(stdout);

}
