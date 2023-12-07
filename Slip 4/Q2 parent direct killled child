#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>
#include<string.h>
#include<signal.h>

void Sh1();
void Sh2();
void Sh3();

int main()
{
	int n;
	n=fork();
	if(n==0)
	{
		signal(SIGHUP,Sh1);
		signal(SIGINT,Sh2);
		signal(SIGQUIT,Sh3);
		while(1)
		{
		
		}
		
	}
	else
	{
		sleep(3);
		kill(n,SIGHUP);
		sleep(3);
		kill(n,SIGINT);
		sleep(3);
		kill(n,SIGHUP);
		sleep(3);
		kill(n,SIGINT);
		sleep(3);
		kill(n,SIGHUP);
		sleep(3);
		kill(n,SIGHUP);
		sleep(3);
		kill(n,SIGINT);
		sleep(3);
		kill(n,SIGHUP);
		sleep(3);
		kill(n,SIGINT);
		sleep(3);
		kill(n,SIGQUIT);
		exit(0);
	}
	return 0;
}

void Sh1()
{
	printf("\nSIGHUP Process");
	//fflush(stdout);
	signal(SIGHUP,Sh1);
}

void Sh2()
{
	printf("\n SIGINT Process");
	//fflush(stdout);
	signal(SIGINT,Sh2);
}

void Sh3()
{
	printf("\n My Papa Has Kill Me");
	exit(0);
}
