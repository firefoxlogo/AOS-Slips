#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>
#include<string.h>
#include<signal.h>

void sh1();
void main()
{
	int n;
	signal(SIGCHLD,sh1);
	n=fork();
	if(n==0)
	{
		execlp("ls","ls","-l",NULL);
		
		
	}
	else
	{
		sleep(5);
		printf("\n child exced time");
		kill(n,SIGINT);
		fflush(stdout);
		sleep(2);
	
	}
	return 0;

}

void sh1()
{
	printf("\n child killed by parent");
	exit(0);

}
