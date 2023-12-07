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
  char s[500];
  DIR *d;
  struct stat s1;
  struct dirent *dr;
  
  printf("\n Enter name:");
  gets(m);
  d=opendir(".");
  while(dr=readdir(d))
  	{
  		stat(dr->d_name,&s1);
  		strcpy(s,ctime(&s1.st_ctime));
  		if(strstr(s,m))
  			printf("%s",dr->d_name);
  		else
  			printf("\nSorryyyyy Brooo kahitri Dusra Month sang!!!");  	
  	}  
 	close(d);
 	return 0;
 
 }
