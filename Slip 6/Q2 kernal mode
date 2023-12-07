#include<sys/times.h>
#include<time.h>
#include<stdio.h>
#include<unistd.h>
#include<sys/wait.h>

int main()
{
	struct tms t;
	int c,n,s;
	long int i,j;
	double d,ut,st,cut,cst;
	
	printf("Enter Number of process:");
	scanf("%d",&n);
	
	while(n-- >0)
	{
		c=fork();
		if(c==0)
		{
			printf("\n process id=>%d",getpid());
			for(i=0,j>0;i<=10000000;i++)
			j++;
			exit(0);
		}
		else
		{
			wait(&s);
		}
	}
	d=sysconf(_SC_CLK_TCK);
	times(&t);
	ut=t.tms_utime/d;
	st=t.tms_stime/d;
	cut=t.tms_cutime/d;
	cst=t.tms_cstime/d;
	
	printf("\nuser time:-%lf",ut);
	printf("\nSystem time:-%lf",st);
	printf(" \nchild user time:-%lf",cut);
	printf(" \nchild System time:-%lf",cst);
	return 0;


}
