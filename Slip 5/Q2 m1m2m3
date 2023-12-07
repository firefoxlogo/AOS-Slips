#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>
#include<string.h>

int main()
{
 int p[2];
 int n,i;
 char *m1="SK\n";
 char *m2="photographer\n";
 char *m3="pune\n";
 char s[50];
 pipe(p);
 n=fork();
 if(n==0)
 {
 	write(p[1],m1,strlen(m1));
 	write(p[1],m2,strlen(m1));
 	write(p[1],m3,strlen(m1));
 }
 else
 {
 	printf("\n In Parent!!!!");
 	for(i=0;i<3;i++)
 	{
 		read(p[0],s,100);
 		printf("%s",s);
 	}
 
 }

return 0;

}
