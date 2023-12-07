#include<stdio.h>
#include<unistd.h>
#include<fcntl.h>
#include<signal.h>
void sh1();
void sh2();
void sh3();
int main()
{
printf("\nIn main Program");
signal(SIGTSTP,sh1);
signal(SIGCONT,sh2);
signal(SIGINT,sh3);

while(1)
{
sleep(2);
raise(SIGTSTP);
sleep(2);
raise(SIGCONT);
}
return 0;
}
void sh1()
{
printf("\nSuspend");
}
void sh2()
{
printf("\nResume");
}
void sh3()
{
printf("\nIntrupted");
exit(0);
}
