#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<fcntl.h>
#include<sys/stat.h>
#include<sys/types.h>
#include<dirent.h>
#include<string.h>
#include<time.h>
#include<pwd.h>
#include<grp.h>

int main()
{
	char fn[50],s[500];
	struct passwd *pw;
	struct group *gr;
	struct stat s1;
	
	printf("Give File nAME");
	gets(fn);
	
	stat(fn,&s1);
	if(S_ISREG(s1.st_mode))
		printf("Regular File");
	else if(S_ISDIR(s1.st_mode))
		printf("Directory File");
	else if(S_ISFIFO(s1.st_mode))
		printf("Pipe File");
	else if(S_ISSOCK(s1.st_mode))
		printf("Scoket File");
	else if(S_ISBLK(s1.st_mode))
		printf("Block File");
	else if(S_ISCHR(s1.st_mode))
		printf("Charactre File");
	else if(S_ISLNK(s1.st_mode))
		printf(" Link File");
		
	printf("\n File permission");
	printf((s1.st_mode & S_IRUSR)?"r":"-");
	printf((s1.st_mode & S_IWUSR)?"w":"-");
	printf((s1.st_mode & S_IXUSR)?"x":"-"); // user per
	
	printf((s1.st_mode & S_IRGRP)?"r":"-");
	printf((s1.st_mode & S_IWGRP)?"w":"-");
	printf((s1.st_mode & S_IXGRP)?"x":"-");// group per
	
	printf((s1.st_mode & S_IROTH)?"r":"-");
	printf((s1.st_mode & S_IWOTH)?"w":"-");
	printf((s1.st_mode & S_IXOTH)?"x":"-");// other per
	
	printf("\n Inode Number=.%d",s1.st_ino); // inode number
	
	printf("\n Number of link=%d",s1.st_nlink); // number of link
	
	printf("\n size of file=.%d",s1.st_size); // Size
	
	strcpy(s,ctime(&s1.st_ctime));
	printf("\n Creation Time.%s",s); //  creatin time
	
	strcpy(s,ctime(&s1.st_atime));
	printf("\n A Time.%s",s); //  access time
	
	strcpy(s,ctime(&s1.st_mtime));
	printf("\n M Time.%s",s); //  modify time
	
	printf("\nUsr id:",s1.st_uid);// User id with user name
	pw=getpwuid(s1.st_uid);
	printf("User name:%s",pw->pw_name);
	
	printf("\ngroup id:",s1.st_gid);// Group id with group name
	gr=getgrgid(s1.st_gid);
	printf("Group name:%s",gr->gr_name);
	
	return 0;

}
