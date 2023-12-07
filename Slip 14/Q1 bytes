#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>
#include<string.h>
#include<time.h>
 int main()
 {
  char m[50];
  int n;
  DIR *d;
  struct stat s1;
  struct dirent *dr;
  
  printf("\n Enter Size:");
  scanf("%d",&n);
  d=opendir(".");
  while(dr=readdir(d))
  	{
  		stat(dr->d_name,&s1);
  		
  		if(s1.st_size>n)
  			printf("%s",dr->d_name);
  	}
 	close(d);
 	return 0;
 
 }
