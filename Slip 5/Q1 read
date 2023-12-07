#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>

int main()
{
 DIR *d;
 struct dirent *dr; 
 int c=0;
 d=opendir(".");
 while(dr=readdir(d))
 {
 	//printf("\n %s",dr-> d_name);
 	c++;
 }

 printf("Count of file %d:",c);
  closedir(d);
 return 0;
}
